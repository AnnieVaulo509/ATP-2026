# Corrida ao 100 - TPC3

Nome: Annie Santos

ID: A113007



<img width="693" height="946" alt="WhatsApp Image 2026-09-22 at 15 23 12" src="https://github.com/user-attachments/assets/476b4528-8731-4fe1-9ba0-327fd06d5d60" />










# Código jogo corrida ao 100

```python
print("Olá, vamos ao jogo?")
a = input("Responda com s ou n")

def jogada_pc(jh):
  return 11 - jh

chaves = [1,12,23,34,45,56,67,78,89,100]

import random 

while a!= "n":
  print("Escolha a modalidade desejada:")
  print("1 - pc inicia")
  print("0 - utilizador inicia")
  b = int(input("Introduza 1 ou 0"))

  if b == 1:
   total = 1
   print("O pc iniciou e jogou 1")
   while total!= 100:
     jh = int(input("Introduza um numero de 1 a 10"))
     total = total + jh
     print(f"Jogou {jh} e o saldo atual é {total} ")
     pc = jogada_pc(jh)
     total = total + pc
     print(f"O pc jogou {pc} e o saldo atual é {total}")
   else:
    print("O pc atingiu 100 e venceu! Não foi desta vez, tente na proxima!")


  if b == 0:
   total = 0
   while total!=100:
     jh = int(input("Introduza um numero de 1 a 10"))
     total = total + jh
     print(f"Jogou {jh} e o saldo atual é {total}")

     if total == 100:
       print("Você atingiu 100! Parabéns")
     else:
       if total in chaves:
        pc = random.randint(1,10)
        total = total + pc
        print(f"O pc jogou {pc} e o saldo atual é {total}")
       elif total not in chaves:
         pc = 11 - jh
         total = total + pc
         print(f"O pc jogou {pc} e o saldo atual é {total}")
       if total == 100:
         print("O pc atingiu 100! não foi dessa vez")
      

  print("Olá, vamos ao jogo?")
  a = input("Responda com s ou n")

else:
 print("Até a proxima!")
  ```
     
