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
```python 
"""programme for linear serch
developed by: yuvabharathib
register number:22002787
"""


def linearsearch(array, n, k):

    for i in range(0, n):
        if (array [i] == k):
            return i
    return -1

array = eval(input())
k =  eval(input())
n = len(array)
array.sort()
result = linearsearch(array, n, k)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)
```


ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:  yuvabharathib
RegisterNumber:22002787
'''
def binarySearchIter(array, k, low, high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid+1
    return -1
array=eval(input())
array.sort()
print(array)
k=eval(input()) 
low=0
high= len(array)-1
result=binarySearchIter(array, k, low, high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")
```

iii)	# Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: yuvabharathib
RegisterNumber: 22002787
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr,k,mid+1,high)
        else:
            return BinarySearch(arr,k,low,mid+1)
    return -1
arr = eval(input())
#sort the array
arr.sort()
print(arr)
# k is the element to be searched for
k = eval(input()) 
low=0
high=len(arr)-1
# use the binary search function to find the result
result=BinarySearch(arr, k, low, high)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")




```
##Output
1 .Use a linear search method to match the item in a list.
![1](https://user-images.githubusercontent.com/113497406/192079627-6ebee81b-ed19-4f03-adb1-6fc65d07e2f5.png)
2.Program to find the element in a list using Binary Search(Iterative Method).
![2](https://user-images.githubusercontent.com/113497406/192079669-feef582f-7f22-459a-a382-ab86360ae148.png)
3.Program to find the element in a list using Binary Search (recursive Method).
![3](https://user-images.githubusercontent.com/113497406/192079740-7acbbbf9-d21b-423b-95d0-7d1a87ece3b6.png)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
