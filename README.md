# def S(n):
    return n + 1

def A(n):
    return n - 1 if n > 0 else 0

def suma(a, b):
    while b > 0:
        a = S(a)
        b = A(b)
    return a

def multiplicacion(a, b):
    resultado = 0
    while b > 0:
        resultado = suma(resultado, a)
        b = A(b)
    return resultado

def resta(a, b):
    while b > 0 and a > 0:
        a = A(a)
        b = A(b)
    return a

def division(a, b):
    if b == 0:
        raise ValueError("No se puede dividir por cero.")
    cociente = 0
    while a >= b:
        a = resta(a, b)
        cociente = S(cociente)
    return cociente

# Pruebas de ejemplo
print(suma(3, 4))
print(multiplicacion(3, 4))
print(resta(7, 4))
print(division(8, 2))
