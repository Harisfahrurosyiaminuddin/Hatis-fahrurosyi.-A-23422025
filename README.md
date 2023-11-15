Carilah solusi dua persamaan berikut

3 + x^3 - x = 4
2x - 4 = 8
Solusi :

Untuk mencari solusi persamaan non-linear 3 + x^3 - x = 4 kita dapat menggunakan metode iteratif seperti metode Newton-Raphson. Metode ini melibatkan iterasi untuk mendekati solusi persamaan. Berikut adalah implementasinya dalam Python:
def fungsi(x):
    return x**3 - x + 3 - 4

def turunan_fungsi(x):
    return 3*x**2 - 1

def metode_newton_raphson(x0, toleransi, maks_iter):
    iterasi = 1
    while iterasi <= maks_iter:
        x1 = x0 - fungsi(x0) / turunan_fungsi(x0)
        print(f'Iterasi {iterasi}: x = {x1}')

        if abs(x1 - x0) < toleransi:
            print(f'Solusi ditemukan setelah {iterasi} iterasi: x = {x1}')
            return x1

        x0 = x1
        iterasi += 1

    print('Iterasi maksimum tercapai. Metode Newton-Raphson tidak konvergen.')
    return None

# Tentukan nilai awal, toleransi, dan maksimum iterasi
x0 = 1.0
toleransi = 1e-6
maks_iter = 100

# Panggil fungsi untuk metode Newton-Raphson
solusi = metode_newton_raphson(x0, toleransi, maks_iter)
