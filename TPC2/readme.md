# Adivinha o número
# Solução pc adivinha o numero do utilizador

print("Olá, vamos ao jogo?")
a = input("Responda com s ou n")
while a!= "n":
    def numero_secreto(minimo,maximo):
        return (minimo + maximo) // 2
    minimo = int(1)
    maximo = int(100)
    i = 0
    print("Pense em um numero de 1 a 100")
    palpite = numero_secreto(minimo,maximo)
    print(f"É {palpite}?")
    resposta = input("Responda com Acertou, O numero que pensei é maior, O numero que pensei é menor ")
    while resposta!= "Acertou":
        i = i + 1
        if resposta == "O numero que pensei é maior":
            minimo = palpite + int(1)
            palpite = numero_secreto(minimo,maximo)
            print(f"É {palpite}?")
            resposta = input("Responda com Acertou, O numero que pensei é maior, O numero que pensei é menor ")
        elif resposta == "O numero que pensei é menor":
            maximo = palpite - int(1)
            palpite = numero_secreto(minimo,maximo)
            print(f"É {palpite}?")
            resposta = input("Responda com Acertou, O numero que pensei é maior, O numero que pensei é menor ")
          
    print("Aha! Sabia que acertaria")
    print(f"Número de tentativas:{i}")
    print("Olá, vamos ao jogo?")
    a = input("Responda com s ou n")
 
else:
    print("Até uma proxima!")