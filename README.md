# Bingo-Game-2
I contruct more efficient Bingo Game algorithm  than version 1

import numpy as np

bingolist=np.arange(1,26).reshape(5,5)
bingo=0

while bingo!=1:
  n=int(input())
  for i in range(5):
    for j in range(5):
      if n==bingolist[i][j]==0:
        bingolist[i][j]=0
   c,d=0,0
   for i in range(5):
      a,b=0,0
      for j in range(5):
        if bingolist[i][j]==0:
          a+=1
        if bingolist[j][i]==0:
          b+=1
      if a==5 or b==5:
        bingo=1
      if bingolist[i][i]==0:
        c+=1
       if bingolist[4-i][i]==0:
        d+=1
       if c==5 or d==5:
        bingo=1
 print("Bingo")       
          
