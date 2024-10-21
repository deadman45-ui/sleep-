class Character:
    def __init__(self, name, is_awake=False):
        self.name = name
        self.is_awake = is_awake

    def wake_up(self):
        self.is_awake = True
        print(f"{self.name} is now awake and ready to fight for justice!")

    def fight_for_justice(self):
        if self.is_awake:
            print(f"{self.name} stands up for everyone who needs help!")
        else:
            print(f"{self.name} needs to wake up first!")

class World:
    def __init__(self):
        self.people = []

    def add_person(self, person):
        self.people.append(person)

    def call_for_justice(self):
        print("It's time for everyone to wake up and stand for justice!")
        for person in self.people:
            person.wake_up()

# Create a world and add people
our_world = World()
alice = Character("Alice")
bob = Character("Bob")
charlie = Character("Charlie")

our_world.add_person(alice)
our_world.add_person(bob)
our_world.add_person(charlie)

# Call for justice
our_world.call_for_justice()

# Each person fights for justice
for person in our_world.people:
    person.fight_for_justice()
# sleep-
