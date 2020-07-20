# counting-word-in-textfile
name = input ("Enter your file name : ")
fname = (name+".txt")
fhandle = open(fname)

#new dictionary is creted so that number of words can be counted
di= dict()

for line in fhandle:
    line = line.rstrip()
    words= line.split()
    for word in words:
        # if you want to directly print dictionary run this line (di[word]= di.get(word,0)+1)
        if word in di:
            di[word] = di[word]+1
        else:
            di[word]= 1
        print(word , di[word])
        


