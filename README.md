print("VALID PET ARGUMENTS: cat, dog, fish, bird, hamster, guinea pig, rabbit, ferret, hedgehog, rat, turtle, lizard, snake, frog ")
pettype = input("What is your pet? ").lower()

pet_multipliers = {
    "cat": 1.0,
    "dog": 1.2,
    "fish": 0.1,
    "bird": 0.1,
    "hamster": 0.2,
    "guinea pig": 0.4,
    "rabbit": 0.6,
    "ferret": 2.4,
    "hedgehog": 0.25,
    "rat": 0.1,
    "turtle": 0.09,
    "lizard": 0.1,
    "snake": 0.2,
    "frog": 0.1
}

# Handling invalid pet type
if pettype not in pet_multipliers:
    print("Invalid pet type entered.")
    quit()

pet_bw = int(input("How heavy is your pet in pounds? "))

if pet_bw <= 5:
    food_recommendation = 0.03
elif pet_bw <= 10:
    food_recommendation = 0.04
elif pet_bw <= 20:
    food_recommendation = 0.05
else:
    food_recommendation = 0.06

if pet_bw >= 90:
    print("Your pet is too fat.")
    quit()

pet_calc = food_recommendation * pet_multipliers[pettype]

print(f"Your {pettype} should eat approximately {pet_calc:.2f} pounds of food a day.")
print("This program is just an approximation, please consult a veterinarian for accurate feeding guidelines.")
