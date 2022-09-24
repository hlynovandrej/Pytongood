
import random 




try:
                while True:
                    u_bal = int(input("Стартовый капитал = "))
                    if u_bal > 0:
                        break
                    else:
                        print("Балланс должен быть больше чем 0")
except ValueError:
    print("Только цифры")
while u_bal != 0:
                    try:
                        
                            u_pay = int(input("Ваша ставка = "))
                            if u_pay > 0 and u_pay <= u_bal:
u_bal = u_bal - u_pay
u_shoose = int(input("На что ставим \n1.Цифра \n2.Цвет\n"))
                                if u_shoose == 1:
while True:
     u_number = int(input("Введите цифру от 0 до 36:\n"))
     if u_number >= 0 and u_number <= 36:
     r_numb = random.randint(0,36)
if r_numb == u_number:
     u_bal = u_bal + u_pay * 7
     print(f"Выпала цифра{r_numb}")
     print(f"ваша ставка выйграла\nваш баланс{u_bal} ")
     break
else:
     print(f"Выпала цифра{r_numb}")
     print(f"ваша ставка не выйграла\nваш баланс{u_bal} ")  
     break        
else:
     print("От 0 до 36") 
                                
elif u_shoose == 2:
     while True:
     u_color = int(input("1.Красный\n 2.Черный\n"))
     if u_color == 1 or u_color == 2:
     r_numb = random.randint(0,36)
     if r_numb > 0:  
if 0 == r_numb % 2:
     color = 1
if color == u_color:
     u_bal = u_bal + u_pay * 2
     print(f"ваша ставка выйграла\nваш баланс{u_bal} ")
else:
     print(f"ваша ставка не выйграла\nваш баланс{u_bal} ") 
else:
      color = 2
      if color == u_color:
      u_bal = u_bal + u_pay * 2
      print(f"Выпала цвет{color}")
      print(f"ваша ставка выйграла\nваш баланс{u_bal} ") 
      break
      else:
      print(f"Выпала цвет{color}")
      print(f"ваша ставка не выйграла\nваш баланс{u_bal} ")  
      break
else:
      print("1 или 2")          
else:
      print("ошибка только 1 или 2")


                    except ValueError:
                        print("Только цифры")
print("Игра окончена")
