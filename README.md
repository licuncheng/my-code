# my-code
def rec(coinvaluelist,change):
    mincoins=change
    if change in coinvaluelist:
        return 1
    else:
        for i in [c for c in coinvaluelist if c<=change]:
            numcoins=1+rec(coinvaluelist,change-i)
            if numcoins<mincoins:
                mincoins=numcoins
        return mincoins
print(rec([1,5,10,25],63))
