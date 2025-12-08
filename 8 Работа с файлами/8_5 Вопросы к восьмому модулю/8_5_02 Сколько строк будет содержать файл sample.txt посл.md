Сколько строк будет содержать файл sample.txt после выполнения следующего кода:

file = File.new("sample.txt", "w+")
file.write("Начало текста")
10.times do
  file.puts("Очень важная информация")
end
file.write("Завершение текста")
file.close

                  
Введите численный ответ
Верно решили 938 учащихся
Из всех попыток 36% верных


# put your ruby code here
11