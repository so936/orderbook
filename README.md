# orderbookorders = [{'type' : 'limit',
                   'side' : 'ask',
                    'quantity' : 5,
                    'price' : 101,
                    'trade_id' : 100},
                    {'type' : 'limit',
                    'side' : 'bid',
                    'quantity' : 5,
                    'price' : 100,
                    'trade_id' : 101},
                   {'type' : 'market',
                    'side' : 'ask',
                    'quantity' : 5,
                    'price' : 103,
                    'trade_id' : 102},
                   {'type' : 'market',
                    'side' : 'bid',
                    'quantity' : 5,
                    'price' : 101,
                    'trade_id' : 103},
                   {'type' : 'stop',
                    'side' : 'ask',
                    'quantity' : 5,
                    'price' : 101,
                    'trade_id' : 104},
                   {'type' : 'stop',
                    'side' : 'bid',
                    'quantity' : 5,
                    'price' : 99,
                    'trade_id' : 105},
                   ]
print("\n---------------------------Order----------------------------")
print("\n")
print("Enter option for Type of Orders \n 1 Limit \n 2 Market  \n 3 Stock")
a=int(input("Enter the option\t=>\t"))
if(a==1):
    for i in range(0,2):
        print(orders[i])
if(a==2):
    for i in range(2,4):
        print(orders[i])
if(a==3):
    for i in range(4,6):
        print(orders[i])

if(a==1):
    cprice=int(input("Enter your limit price =>\t"))
    orders[0]['price']=cprice
    orders[1]['price']=cprice
    print(orders[0:2])
    tradeprice = int(input("Enter your trade price =>\t"))
    if(tradeprice<=cprice and tradeprice<=cprice):
        b = int(input("Enter the option\n 1 buy \n 2 sell =>\t"))
        if (b == 1):
            c = int(input("Enter the quantity between 1 to 5 "))
            if (c <= 5):
                orders[0]['quantity'] = orders[0]['quantity'] - c
                print(orders[0])
            else:
                print("Sorry limit is exceed")
        else:
            print("Sorry Trade is less than limit price")

        if (b == 2):
            c = int(input("Enter the quantity between 1 to 5 "))
            if (c <= 5):
                orders[1]['quantity'] = orders[1]['quantity'] + c
                print(orders[1])
            else:
                print("Sorry limit is exceed")

    else:
        print("Sorry Trade is less than limit price")
if(a==2):
    b = int(input("Enter the option\n 1 buy \n 2 sell =>\t"))
    if (b == 1):
        c = int(input("Enter the quantity between 1 to 5 "))
        if(c<=5):
            orders[2]['quantity'] = orders[2]['quantity'] - c
            print(orders[2])
        else:
            print("Sorry limit is exceed")

    if (b == 2):
        c = int(input("Enter the quantity between 1 to 5 "))
        if (c <= 5):
            orders[3]['quantity'] = orders[3]['quantity'] + c
            print(orders[3])
        else:
             print("Sorry limit is exceed")
if(a==3):
    activationprice = int(input('enter activation price =>\t '))
    print(activationprice)
    cprice = int(input("Enter your limit price =>\t"))
    orders[4]['price'] = cprice
    orders[5]['price'] = cprice
    if (activationprice==cprice):
        b = int(input("Enter the option\n 1 buy \n 2 sell =>\t"))
        if (b == 1):
            c = int(input("Enter the quantity between 1 to 5 "))
            if (c <= 5):
                orders[0]['quantity'] = orders[0]['quantity'] - c
                print(orders[0])
            else:
                print("Sorry limit is exceed")
        else:
            print("Sorry Trade is not possible")






