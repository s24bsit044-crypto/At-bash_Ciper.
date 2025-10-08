# Atbash Cipher by Irfan, Amjid Faraz,And Balach

def reverse_letter(char):
    if char.isalpha():
        if char.islower():
            return chr(ord('z') - (ord(char) - ord('a')))
        else:
            return chr(ord('Z') - (ord(char) - ord('A')))
    else:
        return char

def atbash_process(ManiGap):
    converted = ""
    for ch in ManiGap:
        converted += reverse_letter(ch)
    return converted

def atbash_encrypt(ManiGap):
    return atbash_process(ManiGap)

def atbash_decrypt(ManiGap):
    return atbash_process(ManiGap)


Plaintext = input (" Wati Plaintext Aha Bilik Ida ")
print("Plaintext :", Plaintext)

Cheerdatagain_Pagham = atbash_encrypt(Plaintext)
print("\nCheerdatagain_Pagham   :", Cheerdatagain_Pagham)

Ne_Zanag_Boo = atbash_decrypt(Cheerdatagain_Pagham)
print("\nNe_Zanag_Boo:", Ne_Zanag_Boo)
