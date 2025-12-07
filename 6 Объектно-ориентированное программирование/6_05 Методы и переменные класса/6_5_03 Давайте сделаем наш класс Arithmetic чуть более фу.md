Давайте сделаем наш класс Arithmetic чуть более функциональным. Добавим метод plus, который будет принимать два числа в виде параметров и выводить их сумму:

class Arithmetic
    def self.info
        puts "Класс арифметики"
    end
    def self.plus(x, y)
        puts x + y
    end
end
Arithmetic.plus(2, 5)

# выведет: 7