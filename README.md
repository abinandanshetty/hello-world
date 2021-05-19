def cipher_enc_dec(txt,s):
    res=" "
    if(choice==0):

        for i in range(len(txt)):#traverse the input
            character=txt[i]
            if(character==' '):
                res=res+' '
            elif(character.isupper()):#for upper case
               res=res+chr((ord(character)+(s) - 65)%26 +65)
            else:#for lower case entries
               res=res+chr((ord(character)+(s) - 97)%26 +97)
        return res
    else:

        for i in range(len(txt)):#traverse the input 
            character=txt[i]
            if(character==' '):
                res=res+' '
            elif(character.isupper()):#for upper case
              res=res+chr((ord(character)-(s) - 65)%26 +65)
            else:#for lower case entries
               res=res+chr((ord(character)-(s) - 97)%26 +97)
        return res

    
     
#give the input and check

txt=input("Enter the text : " )
s=int(input("Enter the number of shifts :"))
choice=int(input("enter 0 for encryption and 1 for decryption : "))
print(cipher_enc_dec(txt,s))


