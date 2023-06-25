# Cat-Generation-Calculator
def calculate_cats(generation):
    if generation == 0:
        return 1
    elif generation == 1:
        return 2
    else:
        return calculate_cats(generation - 1) + calculate_cats(generation - 2)

generation = int(input("Введите поколение кошек: "))

if generation < 0:
    print("Некорректный ввод")
else:
    cats_count = calculate_cats(generation)
    print("Количество кошек в поколении", generation, ":", cats_count)
