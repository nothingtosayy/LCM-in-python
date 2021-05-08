# HCF-in-python
To find out the Hihest Common Factor of any 2 numbers. The code could be modified to 3 numbers with some changes. 
def hcf(x,y):
    list_of_factors_of_x = []
    list_of_factors_of_y = []
    for i in range(1,x+1):
        rem = x%i
        if rem == 0:
            print("%d is one of the factor for %d" %(i,x))
            list_of_factors_of_x.append(i)
    for j in range(1,y+1):
        rem = y%j
        if rem == 0:
            print("%d is one of the factor for %d" %(j,y))
            list_of_factors_of_y.append(j)
            
    set_of_x = set(list_of_factors_of_x)   
    set_of_y = set(list_of_factors_of_y)
    commonfact = set_of_x&set_of_y     #set_of_x.intersection(set_of_y)
    print("Common factors between %d and %d are: " %(x,y),commonfact)
    commonfact = list(commonfact)
    hcf = max(commonfact)
    return hcf
    
x = int(input()) #12
y = int(input()) #18
print("HCF of %d and %d:"%(x,y),hcf(x,y))


