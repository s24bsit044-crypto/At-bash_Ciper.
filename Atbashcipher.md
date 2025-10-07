import string

def atbash_encrypt(ManiMessage):
    lowercase = string.ascii_lowercase
    uppercase = string.ascii_uppercase
    result = ""

    for char in ManiMessage:
        if char.islower():  
            result += lowercase[25 - lowercase.index(char)]
        elif char.isupper():  
            result += uppercase[25 - uppercase.index(char)]
        else:  
            result += char
    return result

def atbash_decrypt(ManiMessage):
    return atbash_encrypt(ManiMessage)

ManiMessage = "Amjid Faraz , Irfan Ali Balach And Hussain are Friends And Group Members"

encrypted = atbash_encrypt(ManiMessage)
print("Encrypted :", encrypted)

decrypted = atbash_decrypt(encrypted)
print("Decrypted :", decrypted)
