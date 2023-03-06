# Palindrome

**Normal Approach**

``` java
class HelloWorld {
    public static void main(String[] args) {
        String str1 = "MADAM";
        int n = str1.length();
        
        boolean isPalindrome = true;
        
        for(int i=0; i<(n/2); i++) {
            if(str1.charAt(i) != str1.charAt(n-i-1)) {
                isPalindrome = false;
            }
        }
        
        if(isPalindrome) {
            System.out.println("It is a Palindrome");
        } else {
            System.out.println("It is not a Palindrome");
        }
    }
}
```

<br>

**Recursive Approach**

``` java
class HelloWorld {
    
    static boolean isPalindrome(String str, int i) {
        if(i >= (str.length()/2)) {
            return true;
        }
        
        if(str.charAt(i) != str.charAt(str.length()-i-1)) {
            return false;
        }
        
        return isPalindrome(str, i+1);
    }
    
    
    public static void main(String[] args) {
        String str1 = "MADAM";
        
        if(isPalindrome(str1, 0)) {
            System.out.println("It is a Palindrome.");
        } else {
            System.out.println("It is not a Palindrome.");
        }
    
    }
}

// Time & Space Complexity - O(n/2)
```