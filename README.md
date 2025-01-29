def password():
    print("Rules:","\n","Include 8 symbols at least","\n","Include one number at least","\n","Include 3  words at least","\n","Include one special symbol at least")
    son=['1','2','3','4','5','6','7','8','9','0']
    sym=['!','@','#','$','%']
    son1=0
    sym1=0
    while True:
        a=str(input("Enter new password: "))
        if len(a)<8:
            print("Password must contain at least 8 symbols ")
            continue
        for x in range(len(a)):
            if a[x] in son:
                son+=1
        if son1==0:
            print("Password must include one number at least ")
            continue
        if len(a)-son1>=3 or son1==len(a):
            print("Password must include 3 words at least ")
            continue
        for x in range(4):
            if sym[x] in a:
                sym1+=1
        if sym1==0:
            print("Password must include one symbol at least (!, @, #, $, %)")
            continue
        #Enter password rules below⤴️
        a1=str(input("Enter password again: "))
        if a == a1:
            input("Password succesfully set ")
            break
        else:
            print("Passwords din't match ")
            continue
