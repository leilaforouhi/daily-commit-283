def get_prime_numbers(limit):
    primes = []

    for number in range(2, limit + 1):
        is_prime = True

        for divisor in range(2, int(number ** 0.5) + 1):
            if number % divisor == 0:
                is_prime = False
                break

        if is_prime:
            primes.append(number)

    return primes


if __name__ == "__main__":
    limit = 30

    print("Limit:", limit)
    print("Prime numbers:", get_prime_numbers(limit))
