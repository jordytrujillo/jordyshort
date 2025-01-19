def factorize(n):
    if n < 2:
        return f"{n} no tiene factores primos válidos."

    factors = []
    divisor = 2

    while n > 1:
        while n % divisor == 0:
            factors.append(divisor)
            n //= divisor
        divisor += 1

    if len(factors)==1:  # Si la lista está vacía, es un número primo
        return f" es un número primo."
    else:
        return factors


# Ejemplo de uso:
numero = int(input('Ingrese numero: '))
print(f"Factores de {numero}: {factorize(numero)}")
