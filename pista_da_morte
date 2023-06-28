import random
#o player que tirar o maior numero avança um passo na pista
nome_anterior = str(input('Me informe seu nome: '))
pista = [
    [0, 0],
    [0, 0],
    [0, 0],
    [0, 0],
    [0, 0]
]

for linha in pista:
    print("|", linha[0], "|", linha[1], "|")

while True:
    mesma_pessoa = input("Tem certeza? (Sim/Não): ")
    mesma_pessoa = mesma_pessoa.lower()

    if mesma_pessoa == "sim":
        if nome_anterior == "":
            nome_anterior = str(input("Digite seu nome: "))
        jogador = nome_anterior
        break
    elif mesma_pessoa == "não":
        print("Desculpe, mas é necessário ser a mesma pessoa para continuar.")
        continue
    else:
        print("Resposta inválida. Por favor, responda com 'Sim' ou 'Não'.")

jogador_numero = 0
numeros_escolhidos = []
while jogador_numero < 1 or jogador_numero > 10 or jogador_numero in numeros_escolhidos:
    jogador_numero = int(input("Digite seu número da sorte (entre 1 e 10): "))
    if jogador_numero < 1 or jogador_numero > 10:
        print("Número inválido. Digite um número entre 1 e 10.")
    elif jogador_numero in numeros_escolhidos:
        print("Você já escolheu esse número. Escolha outro.")

numeros_escolhidos.append(jogador_numero)

adversario_numero = random.randint(1, 10) 
print(f"O número que o adversário escolheu foi: {adversario_numero}")

if jogador_numero > adversario_numero:
    print("Parabéns, você tirou o maior número!")
    for i in range(len(pista)):
        if pista[i][0] == 0:
            pista[i][0] = jogador
            break
elif jogador_numero < adversario_numero:
    print("Que pena, o adversário tirou o maior número!")
    for i in range(len(pista)):
        if pista[i][1] == 0:
            pista[i][1] = adversario_numero
            break
else:
    print("Números empatados, ponto para os dois!")
    for i in range(len(pista)):
        if pista[i][0] == 0:
            pista[i][0] = jogador
            pista[i][1] = adversario_numero
            break

contador = 0
while contador < 10:
    contador += 1
    print(f"\n--- Jogada {contador} ---")
    for linha in pista:
        print("|", linha[0], "|", linha[1], "|")
    # Realize a jogada
    jogador_numero = 0
    while jogador_numero < 1 or jogador_numero > 10 or jogador_numero in numeros_escolhidos:
        jogador_numero = int(input("Digite seu número da sorte (entre 1 e 10): "))
        if jogador_numero < 1 or jogador_numero > 10:
            print("Número inválido. Digite um número entre 1 e 10")
