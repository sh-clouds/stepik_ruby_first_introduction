Теперь давайте определим (создадим) классы Automobile и Ferrari:

class Automobile
  def initialize(model, year)
    @model = model
    @year = year
  end
  def info
    puts "Модель #{@model} #{@year} года выпуска"
  end
end

class Ferrari < Automobile
end

                  
Ferrari является подклассом Automobile, поэтому он наследует свойства и методы класса Automobile. И далее мы можем написать такое продолжение кода:

f50 = Ferrari.new("F50", 1995)
f50.info

# выведет: Модель F50 1995 года выпуска

                  
Теперь у Ferrari есть все методы и атрибуты класса Automobile, поэтому мы можем создать новый объект и вызвать метод info из суперкласса (но на самом деле теперь это уже и метод подкласса Ferrari, который его унаследовал от своего предка).