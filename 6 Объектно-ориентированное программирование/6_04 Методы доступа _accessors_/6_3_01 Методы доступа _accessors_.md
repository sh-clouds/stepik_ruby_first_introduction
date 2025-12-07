Методы доступа (accessors)

Представьте себе, что у вас много переменных экземпляров и соответственно много методов getter и setter для них. Код будет очень длинным и громоздким.

Однако в Ruby есть встроенный способ для автоматического создания getter и setter методов с помощью метода attr_accessor. Метод attr_accessor принимает в качестве аргумента символ имени переменной экземпляра, который он использует для создания методов getter и setter. Например:

class Car

  attr_accessor :color
  
  def initialize(color)
    @color = color
  end
end

ford = Car.new("Красный")
ford.color = "Синий"
puts ford.color

# выведет: Синий

                  
В этом примере строка attr_accessor :color заменила два определения методов доступа (getter и setter).

Также в Ruby есть методы attr_reader и attr_writer, если для переменной экземпляра нужно создать только метод getter или только метод setter соответственно.

Мы можем передавать в методы attr_accessor, attr_reader и attr_writer несколько символов. Например:
attr_accessor :name, :height, :weight 