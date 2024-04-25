import random

def jokempo():
    while True:
        escolhas = ['pedra', 'papel', 'tesoura']

        escolha_robo = random.choice(escolhas)

        escolha_jogador = input('Pedra, papel ou tesoura (ou "sair" para encerrar o jogo): ').lower()

        if escolha_jogador in escolhas:
            print('O Robo escolheu {}'.format(escolha_robo))
            print('Voce escolheu {}'.format(escolha_jogador))

            if escolha_jogador == escolha_robo:
                print('O jogo empatou!')
            elif (escolha_robo == 'pedra' and escolha_jogador == 'tesoura') or \
                 (escolha_robo == 'tesoura' and escolha_jogador == 'papel') or \
                 (escolha_robo == 'papel' and escolha_jogador == 'pedra'):
                print('Você perdeu!!')
            else:
                print('Você ganhou!!')

        elif escolha_jogador == 'sair':
            print('Obrigado por jogar! Até a próxima.')
            break

        else:
            print('Você digitou algo inválido. Digite apenas pedra, papel ou tesoura.')


jokempo()

