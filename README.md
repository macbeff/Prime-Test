def singletest(prime, factor):
    if prime%factor==0:
        return(True)
    else:
        return(False)
neverending=True
while neverending==True:
    constant=float(input("Select a number, and I will tell you if it is prime: "))
    x=2
    while singletest(constant, x)!=True:
        if x>=constant/2:
            break
        else:
            x= 1+x
    if singletest(constant, x)==True:
        print(constant, "is not a prime number.")
    else:
        print(constant, "is a prime number.")
    neverending=False
    while neverending!=True:
        yesno=input("Type 'yes' to continue or 'no' to quit: ")
        if yesno=="yes":
            neverending=True
        elif yesno=="no":
            neverending=False
            break

