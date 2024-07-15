def product_recursive(numbers, index):
    if index == len(numbers):
        return 1
    else:
        return numbers[index] * product_recursive(numbers, index + 1)

def get_numbers_recursive(count, numbers=[]):
    if count == 0:
        return numbers
    else:
        number = float(input(f"Enter number {6 - count}: "))
        numbers.append(number)
        return get_numbers_recursive(count - 1, numbers)

def main():
    print("Please enter five numbers:")
    numbers = get_numbers_recursive(5)
    result = product_recursive(numbers, 0)
    print(f"The product of the numbers is: {result}")

if __name__ == "__main__":
    main()
