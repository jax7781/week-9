# week-9
Scripts for week 9
def isSorted(lst):
    if len(lst) < 2:
        return True  # An empty list or a list with one element is considered sorted
    else:
        for i in range(len(lst) - 1):
            if lst[i] > lst[i + 1]:
                return False
        return True

# Test the function with example lists
test_list_1 = []
test_list_2 = [1]
test_list_3 = [1, 2, 3, 4, 5]
test_list_4 = [10, 5, 8, 12, 3]

print(isSorted(test_list_1))  # Output: True
print(isSorted(test_list_2))  # Output: True
print(isSorted(test_list_3))  # Output: True
print(isSorted(test_list_4))  # Output: False

def printall(seq):
    print("Call with argument:", seq)  # Trace the argument on each call
    if seq:
        print(seq[0])
        printall(seq[1:])

# Test the function with different sequences
sequence_1 = "Hello, World!"
sequence_2 = (1, 2, 3, 4, 5)
sequence_3 = ["apple", "banana", "cherry", "date"]

printall(sequence_1)
print("---")
printall(sequence_2)
print("---")
printall(sequence_3)

def read_numbers(filename):
    with open(filename, "r") as file:
        numbers = [float(line.strip()) for line in file]
    return numbers

def compute_average(numbers):
    total = sum(numbers)
    average = total / len(numbers)
    return average

def print_average(filename):
    numbers = read_numbers(filename)
    average = compute_average(numbers)
    print("Average:", average)

# Example usage
filename = "numbers.txt"
print_average(filename)
