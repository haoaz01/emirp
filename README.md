# emirp
import random

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def reverse_number(n):
    return int(str(n)[::-1])

def get_emirp():
    while True:
        num = random.randint(10, 1000)
        if is_prime(num) and is_prime(reverse_number(num)) and num != reverse_number(num):
            return num

emirp = get_emirp()
print("Số emirp ngẫu nhiên là:", emirp)
