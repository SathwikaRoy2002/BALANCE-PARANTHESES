def getMin(s):

    # Write your code here
    bal =0
    ans=0
    for i in range(0,len(s)):
        if(s[i]=='(' or s[i]=='{' or s[i]=='['):
            bal +=1
        else:
            bal += -1
        if(bal == -1):
            ans +=1
            bal+=1
    return bal+ans


if _name_ == '_main_':
    
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    s = input()

    result = getMin(s)

    fptr.write(str(result) + '\n')

    fptr.close()
