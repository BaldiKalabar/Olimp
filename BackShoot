import random, time


class Blackshot:
    def __init__(self, HpPlayer, HpDiller, DillerHod, PlayerHod, Patron, PatronHolost, los, win):
        self.hpplayer = HpPlayer
        self.hpdiller = HpDiller
        self.dhod = DillerHod
        self.phod = PlayerHod
        self.Patron = Patron
        self.patronhol = PatronHolost
        self.los = los
        self.win = win

    def PlayerHod(self, deistvie):
        i = deistvie
        stolpl = ''
        if i == 3:
            print(f"Что ты хочеш использовать со стола?,{playerinv}")
            stolpl = input("Напиши данный предмет")
            for i in playerinv:
                if stolpl not in i:
                    pass
                else:
                    if i == 'Нож':
                        playerinv.pop(i)
                    if i == 'Сигарета':
                        self.hpplayer += 1
                        playerinv.remove(i)
                        return 'Вы получили 1 ХР'
                    if i == 'Наручники':
                        self.dhod += 1
                        playerinv.pop(i)
                    if i == 'Пиво':
                        playerinv.pop(i)

        if i == 1:
            if self.patronhol == 0:
                self.hpdiller -= 1
                self.Patron -= 1
                if self.hpdiller == 0:
                    self.win = 1
                    return 'Диллер проиграл сражение'
                return "Тут только боевые патроны"
            if self.patronhol < self.Patron:
                dd = random.randint(1, 2)
                if dd == 1:
                    self.patronhol -= 1
                    self.phod = 0
                    self.dhod = 1

                    return "Тут была холостная пуля"

                if dd == 2:
                    self.hpdiller -= 1
                    if self.hpdiller == 0:
                        self.los = 1
                        return "Диллер умер"
                    else:
                        self.Patron -= 1
                        return "В Оружие была не холостная пуля"
            else:
                dd = random.randint(1, 5)
                if dd != 2:
                    self.patronhol -= 1
                    self.phod = 0
                    self.dhod = 1
                    return "Тут была холостная пуля"

                else:
                    self.hpdiller -= 1
                    if self.hpdiller == 0:
                        self.los = 1
                        return "Диллер умер"
                    else:
                        self.Patron -= 1
                        return "В Оружие была не холостная пуля"
        if i == 2:
            if self.patronhol < self.Patron:
                dd = random.randint(1, 2)
                if dd == 1:
                    self.patronhol -= 1

                    return "Тут была холостная пуля"

                if dd == 2:
                    self.hpplayer -= 1
                    if self.hpplayer == 0:
                        self.win = 1
                        return "Player проиграл сражение"
                    else:
                        self.Patron -= 1
                        self.phod = 0
                        self.dhod = 1
                        return "В Оружие была не холостная пуля"
            else:
                dd = random.randint(1, 5)
                if dd != 2:
                    self.hpplayer -= 1
                    if self.hpplayer == 0:
                        self.win = 1
                        return "Player проиграл сражение"
                    else:
                        self.Patron -= 1
                        self.phod = 0
                        self.dhod = 1
                        return "В Оружие была не холостная пуля"
                else:
                    self.patronhol -= 1
                    return "Тут была холостная пуля"

    def DillerHod(self, Deistvie):
        i = Deistvie
        if i == 1:
            if self.patronhol == 0:
                self.hpplayer -= 1
                self.Patron -= 1
                if self.hpplayer == 0:
                    self.los = 1
                    return "Player проиграл сражение"
                return "Тут только боевые патроны"
            if self.patronhol < self.Patron:
                dd = random.randint(1, 2)
                if dd == 1:
                    self.patronhol -= 1
                    self.phod = 1
                    self.dhod = 0
                    return "Тут была холостная пуля"

                if dd == 2:
                    self.hpplayer -= 1
                    if self.hpplayer == 0:
                        self.los = 1
                        return "Вы умерли"
                    else:
                        self.Patron -= 1

                        return "В Оружие была не холостная пуля"
            else:
                dd = random.randint(1, 5)
                if dd != 2:
                    self.hpplayer -= 1
                    if self.hpplayer == 0:
                        self.los = 1
                        return "Вы Проиграли"
                    else:
                        self.Patron -= 1
                        return "В Оружие была не холостная пуля"
                else:
                    self.patronhol -= 1
                    self.phod = 1
                    self.dhod = 0
                    return "Тут была холостная пуля"
        if i == 2:
            if self.patronhol < self.Patron:
                dd = random.randint(1, 2)
                if dd == 1:
                    self.patronhol -= 1
                    return "Тут была холостная пуля"
                if dd == 2:
                    self.hpdiller -= 1
                    if self.hpdiller == 0:
                        self.win = 1
                        return "Диллер проиграл сражение"
                    else:
                        self.Patron -= 1
                        self.dhod = 0
                        self.phod = 1
                        return "В Оружие была не холостная пуля"
            else:
                dd = random.randint(1, 5)
                if dd != 2:
                    self.hpdiller -= 1
                    if self.hpdiller == 0:
                        self.win = 1
                        return "Diller проиграл сражение"
                    else:
                        self.Patron -= 1
                        self.dhod = 0
                        self.phod = 1
                        return "В Оружие была не холостная пуля"
                else:
                    self.patronhol -= 1
                    return "Тут была холостная пуля"


print("Предусловие-\nИгрок не видит сколько холостных во время и после выстрела бота(Чисто небольшое усложнение)")
time.sleep(2)
player = input("Добро Пожаловать в Игру введите имя -->")
holpatron = 0
holpatroningame = 0
patronvisyal = []
playerinv = []
Dillerinv = []
print("Давайте начнём игру")
time.sleep(0.5)
round = 2
while round != 4:
    rr = random.randint(1, 1)
    for i in range(rr):
        print("Загружаем патроны.")
        print('\n\n\n\n\n\n')
        time.sleep(0.5)
        print("Загружаем патроны..")
        print('\n\n\n\n\n\n')
        time.sleep(0.5)
        print("Загружаем патроны...")
        print('\n\n\n\n\n\n')
        time.sleep(0.5)
    time.sleep(0.5)
    colpatron = random.randint(3, 6)
    holpatron = random.randint(1, 5)
    while colpatron < holpatron:
        holpatron = random.randint(1, 5)
    holpatroningame = holpatron
    Gamesetting = Blackshot(3, 3, 0, 0, colpatron, holpatroningame, 0, 0)
    if round == 2:
        Gamesetting = Blackshot(6, 6, 0, 0, colpatron, holpatroningame, 0, 0)
        time.sleep(1)
        print("Пришло время добавить что то новое в игру")
        time.sleep(1)
        for i in range(2):
            randomitem = random.randint(1, 1)
            if randomitem == 1:
                playerinv.append("Нож")
            if randomitem == 2:
                playerinv.append("Сигарета")
            if randomitem == 3:
                playerinv.append("Наручники")
            if randomitem == 4:
                playerinv.append("Пиво")

    if round == 3:
        Gamesetting = Blackshot(9, 9, 0, 0, colpatron, holpatroningame, 0, 0)
    while Gamesetting.win != 1 and Gamesetting.los != 1:
        patronvisyal = []
        for i in range(colpatron):
            while holpatron != 0:
                patronvisyal.append('🟩')
                holpatron -= 1
            else:
                patronvisyal.append("🟥")
        time.sleep(0.3)
        print(patronvisyal)
        print(f"Жизни у {player},{Gamesetting.hpplayer},Жизни у Диллера {Gamesetting.hpdiller}")
        if round != 1:
            print(f"Ваш стол", playerinv)
        if Gamesetting.dhod == 0:
            if round == 1:
                deistvie = int(input(f'Что ты будеш делать?\n1-Стрелять в диллера\n2-Стрелять в себя'))
                while deistvie != 1 and deistvie != 2:
                    deistvie = int(input(f'Что ты будеш делать?\n1-Стрелять в диллера\n2-Стрелять в себя'))
            else:
                deistvie = int(input(
                    f'Что ты будеш делать?\n1-Стрелять в диллера\n2-Стрелять в себя\n3-Использовать предмет со стола'))
                while deistvie != 1 and deistvie != 2 and deistvie != 3:
                    deistvie = int(input(
                        f'Что ты будеш делать?\n1-Стрелять в диллера\n2-Стрелять в себя\n3-Использовать предмет со стола'))
            print(Gamesetting.PlayerHod(deistvie))
            holpatron = Gamesetting.patronhol
            colpatron = Gamesetting.Patron

        else:
            print('\n\n\n')
            print("Диллер делает ход")
            time.sleep(5)
            if Gamesetting.patronhol == 0:
                deistvieDillera = 1
                print(Gamesetting.DillerHod(deistvieDillera))
            else:
                if Gamesetting.Patron < Gamesetting.patronhol:
                    if random.randint(1, 10) in [1, 2, 3, 4, 5, 6, 7, 8]:
                        deistvieDillera = 2
                        print(Gamesetting.DillerHod(deistvieDillera))
                    else:
                        deistvieDillera = 1
                        print(Gamesetting.DillerHod(deistvieDillera))
                else:
                    if random.randint(1, 10) in [1, 2, 3, 4, 5, 6, 7, 8]:
                        deistvieDillera = 1
                        print(Gamesetting.DillerHod(deistvieDillera))
                    else:
                        deistvieDillera = 2
                        print(Gamesetting.DillerHod(deistvieDillera))
            if deistvieDillera == 1:
                print("Диллер выстрелил в тебя")
            else:
                print("Диллер выстрелил в себя")
        if Gamesetting.patronhol == 0 and Gamesetting.Patron == 0:
            print("Пришло время заного добавить потронов")
            time.sleep(4)
            rr = random.randint(1, 1)
            for i in range(rr):
                print("Загружаем патроны.")
                print('\n\n\n\n\n\n')
                time.sleep(0.5)
                print("Загружаем патроны..")
                print('\n\n\n\n\n\n')
                time.sleep(0.5)
                print("Загружаем патроны...")
                print('\n\n\n\n\n\n')
                time.sleep(0.5)
            time.sleep(0.5)
            colpatron = random.randint(3, 6)
            holpatron = random.randint(1, 5)
            while colpatron < holpatron:
                holpatron = random.randint(1, 5)
            holpatroningame = holpatron
    if Gamesetting.win == 1:
        print("Ты победил")
        time.sleep(3)
        print('Но пора начать слудещий раунд')
        time.sleep(2)
        round += 1
    else:
        print("АЪХХАХХАХАХАХАХХАХАХАХХАА")
        break
frend=[['🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔲', '🔳', '🔲', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔲', '🔳', '🔲', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔲', '🔳', '🔲', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔲', '🔳', '🔲', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔲', '🔳', '🔲', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔲', '🔳', '🔳', '🔳', '🔳', '🔳', '🔲', '🔳', '🔳'],
                           ['🔳', '🔳', '🔲', '🔳', '🔳', '🔳', '🔲', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔲', '🔲', '🔲', '🔳', '🔳', '🔳', '🔳'],
                           ['🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳', '🔳']]
print("Ты правда сделал это?")
for i in frend:
    for j in i:
        print(j, end=' ')
    print('')
time.sleep(2)


