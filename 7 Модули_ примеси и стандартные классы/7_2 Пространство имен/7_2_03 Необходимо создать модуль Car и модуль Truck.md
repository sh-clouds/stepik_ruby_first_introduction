Необходимо создать модуль Car и модуль Truck. В обоих модулях реализовать класс Volvo. В модуле Car этот класс должен содержать переменную класса wheels равную 4, а в модуле Truck этот класс должен содержать переменную класса wheels равную 6. Также в каждом классе реализовать метод how_many_wheels, который будет выводить переменную класса wheels.

После этого необходимо создать по экземпляру каждого класса (сначала Car, затем Truck). И использовать метод how_many_wheels на каждом из объектов.

Напишите программу. Тестируется через stdin → stdout
Верно решили 886 учащихся
Из всех попыток 21% верных


# put your ruby code here
module Car
    class Volvo 
        @@wheels = 4
        def how_many_wheels
            puts @@wheels
        end                
    end      
end

module Truck
    class Volvo  
        @@wheels = 6        
        def how_many_wheels
            puts @@wheels
        end    
    end      
end

nissan = Car::Volvo.new
laz = Truck::Volvo.new

nissan.how_many_wheels
laz.how_many_wheels




