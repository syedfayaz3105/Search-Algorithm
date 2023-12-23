# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```''' 
Program for linear search method to match the item in a list
Developed by:Farhana H
RegisterNumber:23012987 
'''
def linearSearch(array,n,k):
    for i in range(n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
array.sort()
k = eval(input())
n=len(array)
print(array)
result = linearSearch(array,n,k)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Farhana H
RegisterNumber: 23012987
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
           low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k=eval(input()) 
result=binarySearchIter(array,k,0,len(array)-1)
if (result==-1):
    print(array)
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Farhana H
RegisterNumber: 23012987
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
            return -1
arr=eval(input())
arr.sort()
k=eval(input())
result=BinarySearch(arr,k,0,len(arr)-1)
if(result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
## Sample Input and Output
1.input
![image](https://github.com/syedfayaz3105/Search-Algorithm/assets/147144126/2b8cc6db-5674-4f46-82d2-fae632e2ea81)
output
![image](https://github.com/syedfayaz3105/Search-Algorithm/assets/147144126/ca9f313e-f395-436f-85a8-09a2e12b82ce)
2.input
![image](https://github.com/syedfayaz3105/Search-Algorithm/assets/147144126/aab4919b-7a33-4306-9c3d-085e1158ad20)
output
![image](https://github.com/syedfayaz3105/Search-Algorithm/assets/147144126/805519e0-492a-48d0-bcdb-ab6b7b26adae)
3.input
![image](https://github.com/syedfayaz3105/Search-Algorithm/assets/147144126/74ca772a-3f99-411f-95d5-af4845f30504)
![image](https://github.com/syedfayaz3105/Search-Algorithm/assets/147144126/a09d05b0-b952-483c-abe4-9d11a9702808)
## Result
Thus the linear search and binary search algorithm is implemented using python programming.
