# Hactoberfest2021
#You are given an integer N. Consider the sequence containing the integers 1,2,…,N in increasing order (each exactly once). 
Find the length of the longest subarray in this sequence such that the bitwise AND of all elements in the subarray is positive.
#time complexity:
o(n)
#constraints:
Constraints
1≤T≤105
1≤N≤109
#python code:
t=int(input())
for i in range(t):
    n=int(input())
    count=0
    mac=0
    arr=[]
    for i in range(1,n+1):
        arr.append(i)
    if n==1:
        print(1)
    else:
        for i in range(len(arr)):
            if (arr[i] & arr[i+1])>0:
                count=arr[i] & arr[i+1]
    mac=max(mac,count)
    print(mac)



