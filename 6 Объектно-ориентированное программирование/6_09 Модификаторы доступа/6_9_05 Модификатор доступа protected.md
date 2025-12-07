Модификатор доступа protected

Важно отметить, что методы с модификатором private в Ruby не могут быть вызваны на объекте класса. Даже если мы попытаемся вызвать метод с модификатором private используя self, все равно получим ошибку.

Это может понадобиться, например, при перегрузке оператора для сравнения двух объектов. Создадим класс Food и перезагрузим оператор сравнения, чтобы иметь возможность сравнивать имена объектов этого класса :

class Food
  def initialize(name)
    @name = name
  end
  
  def ==(other)
    name == other.name
  end
  
  private
  attr_reader :name
end

orange = Food.new("Апельсин")
banana = Food.new("Банан")
puts orange == banana

# выведет ошибку

                  
Этот код вызовет ошибку, так как мы пытались вызвать приватный метод getter для переменной name.
Чтобы иметь возможность сделать это, не делая метод публичным, в Ruby есть модификатор доступа protected.
И если мы изменим модификатор доступа метода getter с private на protected, код будет работать без ошибки:

class Food
  def initialize(name)
    @name = name
  end
  
  def ==(other)
    name == other.name
  end
  
  protected
  attr_reader :name
end

orange = Food.new("Апельсин")
banana = Food.new("Банан")
puts orange == banana

# выведет: false

                  
Модификаторы private и protected очень похожи. Второй из них используется крайне редко в случаях подобных перегрузке оператора, как в нашем примере. Более того, документация Ruby рекомендует использовать модификатор private вместо protected всегда, когда это возможно.