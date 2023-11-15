1. persamaan non linier 3 + x^3 - x = 4
def bisection(a, b, tolerance, max_iterations):
    iteration = 0

    while (b - a) / 2 > tolerance and iteration < max_iterations:
        c = (a + b) / 2
        if f(c) == 0:
            return c
        elif f(c) * f(a) < 0:
            b = c
        else:
            a = c
        iteration += 1

    return (a + b) / 2

# Contoh penggunaan
a = -2.0
b = 2.0
tolerance = 1e-6
max_iterations = 100

solusi = bisection(a, b, tolerance, max_iterations)

if solusi is not None:
    print("Solusi dari persamaan nonlinier adalah:", solusi)
else:
    print("Metode biseksi tidak konvergen.")

solusi dari persamaan non linier adalah: 1.3247175216674805


2. persamaan linier 2x - 4 = 8
def linear_equation_solver(coef, constant):
    return (constant + coef) / coef

# Koefisien variabel x
coef_x = 2

# Konstanta
constant = 8 + 4

# Menyelesaikan persamaan
solusi = linear_equation_solver(coef_x, constant)

print("Solusi dari persamaan linier adalah:", solusi)

solusi dari persamaan linier adalah: 6.0
