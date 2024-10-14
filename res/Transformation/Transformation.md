# 題目：Transformation

## Description

I wonder what this really is... [enc](./enc) ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

## Hint

1. You may find some decoders online

## SOLUTION 1

根據他的提示可以使用線上工具，我使用的是Cyberchef我們可以先猜開看他是怎麼加密的  
''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])  
  
1. for i in range(0, len(flag), 2)
2. chr(ord(flag[i]) << 8 + ord(flag[i + 1]))

第一步：  
i從0每次跳過一格(0,2,4,6...)到最後(如果len(flag)是偶數的話則跳到倒數第二個字元)  
第二步：  
把flag[i]變成Unicode並且shift 8 bits

![alt text](image.png)