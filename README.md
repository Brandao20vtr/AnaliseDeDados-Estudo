# Analise De Dados - Estudo 
## Código em Python para cadastro de pessoas com Idade e Sexo, para fazer uma simples análise dos dados que iremos usar nesse estudo.

##### **DESAFIO 069:** Crie um programa que leia a IDADE e o SEXO de várias pessoas. A cada pessoa cadastrada, o programa deverá perguntar se o usuário quer ou não continuar.
##### No final, mostre:
##### **A -->** Quantas pessoas tem mais de 18 anos.
##### **B -->** Quantos homens foram cadastrados.
##### **C -->** Quantas mulheres tem menos de 20 anos.

---

```
print()

print('\t\t\tCADASTRANDO VÁRIAS PESSOAS\n#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*\n')

tot18, totH, totM = 0

while True:
    idade = int(input('Digite sua idade: '))

    sexo = ' '

    # Com esse outro WHILE ele só vai aceitar(Seguir em frente) quando o usuário digitar M ou F, se não ele irá ficar pedindo repetidamente.
    while sexo not in 'MF':
        sexo = str(input('Informe seu sexo [M/F]: ')).strip().upper()[0]

    if idade >=18:
        tot18 +=1

    if sexo == 'M':
        totH += 1

    if sexo == 'F' and idade < 20:
        totM +=1

    opcao = ' '

    # Com esse outro WHILE ele só vai aceitar(Seguir em frente) quando o usuário digitar S ou N, se não ele irá ficar pedindo repetidamente.
    while opcao not in 'SN':
        opcao = str(input('\n\033[1mVocê deseja continuar? [S/N]\033[m ')).strip().upper()[0]
        print()

    if opcao == 'N':
        break

print(f'Total de pessoas com mais de 18 anos: {tot18}')
print(f'Ao todo temos {totH} homens cadastrados.')
print(f'E temos {totM} mulheres com menos de 20 anos.')
print('\nFim do Programa! Até a próxima.')```
