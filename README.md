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
```
''' 
Program for linear search method to match the item in a list
Developed by: Vanitha S
RegisterNumber: 212222100057
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
n=len(array)# get the length of array and store in the variable n
array.sort()
result = linearSearch(array,n,k)# use the function for linear search
print(array)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)     
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result




```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Vanitha S
RegisterNumber: 212222100057
'''
def binarySearchIter(array, k, low, high):
    mid=0
    while low<=high:
        mid=(high+low)//2
        if(array[mid]<k):
            low=mid+1
        elif(array[mid]>k):
            high=mid-1
        else:
            return mid
    return -1

array = eval(input())
array.sort()# sort the array
k = eval(input()) #k-item to be searched
res=binarySearchIter(array, k, 0,len(array)-1)
# use the binary search function to find the item in the list
print(array)
if(res==-1):
    print("Element not found")
else:
    print("Element found at index: ",res)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Vanitha S
RegisterNumber: 212222100057
'''
def BinarySearch(arr, k, low, high):
    if(high>=low):
        mid=(low+high)//2
        if(arr[mid]<k):
            return BinarySearch(arr, k, mid+1, high)
        elif(arr[mid]>k):
            return BinarySearch(arr, k, low, mid-1)
        else:
            return mid
    else:
        return -1
arr = eval(input())
arr.sort()#sort the array
k = eval(input()) # k is the element to be searched for
res=BinarySearch(arr, k, 0, len(arr)-1)
print(arr)
if(res==-1):
    print("Element not found")
else:
    print("Element found at index: ",res)
# use the binary search function to find the result

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```

## Output

![3b1](https://github.com/Vanitha-SM/Search-Algorithm/assets/119557985/5fbadea7-4b4e-4f3d-85c1-b25bdd3cb46a)

![3b2](https://github.com/Vanitha-SM/Search-Algorithm/assets/119557985/6dd6cbb2-8d66-4c72-b91c-4f635acd85d2)

![Screenshot 2023-05-24 221747](https://github.com/Vanitha-SM/Search-Algorithm/assets/119557985/fa1e6499-4274-4724-99f7-668351bdcbad)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
