from random import randint


class Druid:
    def __init__(self):
        self.hp = 150
        self.power = 50
        self.agility = 0
        self.intelligence = 50
        self.armor = 100
        self.wisdom = 125
        self.charisma = 0

    def attack(self):
        damage = random.randint(1, self.attack_power)
        other.health -= damage
        print(f"{self.name} атакует {other.name} и наносит {damage} урона!")    

    def move(self):
        print(f'Вы можете двинуться на {randint(1, 40)}')

    def wild_form_bear(self):
        print(f"Вы превратись в медведя сила увеличена на 125, броня увеличена 180%, очки здоровья увеличены на 25%")
        self.hp = 125
        self.power = 225
        self.armor = int(150 * 1.8)

    def wild_form_back(self):
        print(f"Вы превратились обратно в человека , все баффы пропали")
        self.hp = 100
        self.power = 100
        self.armor = 150

    def wooden_skin(self):
        print(f"Ваша кожа превращается в кору дерева, телосложение увеличивается в 2 раза")
        self.armor *= 2

    def animal_language(self):
        print(f"вы говорите животному {input()}")

        

    def is_alive(self):
        return self.health > 0


class Player(Druid):
    def init(self, name):
        super().init(name, health=100, attack_power=20)


class Monster(Druid):
    def init(self, name):
        super().init(name, health=50, attack_power=15)


def battle(player, monster):
    while player.is_alive() and monster.is_alive():
        player.attack(monster)
        if monster.is_alive():
            monster.attack(player)
        print(f"Здоровье {player.name}: {player.health}, Здоровье {monster.name}: {monster.health}")

    if player.is_alive():
        print(f"{player.name} победил {monster.name}!")
    else:
        print(f"{monster.name} победил {player.name}...")


def main():
    player_name = input("Введите имя вашего персонажа: ")
    player = Player(player_name)
    monster = Monster("Гоблин")

    print(f"{player.name} вступает в бой с {monster.name}!")
    battle(player, monster)
class player():    
    def class_switch_to_druid():
        print(f"вы выбрали персонажа Чародей")
            
