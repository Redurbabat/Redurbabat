
import random

def main():
    oyuncu_can = 100
    bilgisayar_can = 100

    while oyuncu_can > 0 and bilgisayar_can > 0:
        print("Oyuncu Can: " + str(oyuncu_can))
        print("Bilgisayar Can: " + str(bilgisayar_can))
        print("Saldır veya Savun:")
        hamle = input()

        oyuncu_saldiri = random.randint(0, 20)
        bilgisayar_saldiri = random.randint(0, 20)

        if hamle.lower() == "saldır":
            print("Oyuncu " + str(oyuncu_saldiri) + " puan hasar verdi.")
            bilgisayar_can -= oyuncu_saldiri
        elif hamle.lower() == "savun":
            print("Oyuncu savunuyor.")
        else:
            print("Geçersiz hamle. Saldır veya Savun seçin.")

        print("Bilgisayar " + str(bilgisayar_saldiri) + " puan hasar verdi.")
        oyuncu_can -= bilgisayar_saldiri

    if oyuncu_can <= 0:
        print("Oyuncu kaybetti. Bilgisayar kazandı!")
    else:
        print("Bilgisayar kaybetti. Oyuncu kazandı!")

if __name__ == "__main__":
    main()
