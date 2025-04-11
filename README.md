import os
player=input("Введите имя персонажа")
save_file = os.path.join('save.txt')
with open(save_file, 'r+') as f:
    if player in f.read():
        print(f'Добро пожаловать {player}')
    else:
        f.write(player)
        print(*f)
        f.write(' ')

