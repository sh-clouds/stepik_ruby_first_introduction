В Ruby принято называть методы getter и setter теми же именами, что и переменная экземпляра, к которой они обращаются.
Предыдущий пример можно переписать как:

class Car
  def initialize(color)
    @color = color
  end
  def color
    @color
  end
  def color=(color)
    @color = color
  end
end

bmw = Car.new("Красный")
bmw.color = "Синий"
puts bmw.color

# выведет: Синий