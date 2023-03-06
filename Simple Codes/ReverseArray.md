# Reverse an Array

**Swapping**

``` java
class HelloWorld {
    
    static void reverseArray(int arr[], int start, int end) {
        while(start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            
            start++;
            end--;
        }
    } 
    
    public static void main(String[] args) {
        int arr1[] = {1, 3, 4, 5, 8};
        int n = arr1.length;

        for(int i=0; i<n; i++) {
            System.out.print(arr1[i] + " ");
        }
        
        System.out.println("");
        
        reverseArray(arr1, 0, n-1);
        
        for(int i=0; i<n; i++) {
            System.out.print(arr1[i] + " ");
        }
    }
}
```

Output: 

```
1 3 4 5 8 
8 5 4 3 1 
```

<br>

**Using Recursion**

``` java
class HelloWorld {
    
    static void recursiveReverse(int arr[], int start, int end) {
        if(start >= end) {
            return;
        }
        
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        recursiveReverse(arr, start+1, end-1);
    }

    public static void main(String[] args) {
        int arr1[] = {1, 3, 4, 5, 8};
        int n = arr1.length;

        for(int i=0; i<n; i++) {
            System.out.print(arr1[i] + " ");
        }
        
        System.out.println("");
        
        recursiveReverse(arr1, 0, n-1);
        
        for(int i=0; i<n; i++) {
            System.out.print(arr1[i] + " ");
        }
    }
}
```

<br>

Using Recursion - Single Pointer

``` java
class HelloWorld {
    
    static void recursiveReverse(int arr[], int i) {
        if(i >= (arr.length/2)) {
            return;
        }
        
        int temp = arr[i];
        arr[i] = arr[arr.length-i-1];
        arr[arr.length-i-1] = temp;
        
        recursiveReverse(arr, i+1);
    }
    
    public static void main(String[] args) {
        int arr1[] = {1, 3, 4, 5, 8};
        int n = arr1.length;

        for(int i=0; i<n; i++) {
            System.out.print(arr1[i] + " ");
        }
        
        System.out.println("");
        
        recursiveReverse(arr1, 0);
        
        for(int i=0; i<n; i++) {
            System.out.print(arr1[i] + " ");
        }
    }
}
```