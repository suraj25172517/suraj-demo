
## Problem
Valid Palindrome (LeetCode)

## Approach
Two pointer + skip non-alphanumeric characters

## Time Complexity
O(n)

## Space Complexity
O(1)

## Code
```
class Solution {
    static boolean alphanumaric(char ch){
    if((ch >= 'a' && ch<= 'z') || (ch>='0' && ch<='9') ){
      return true;
    }
    return false;
  }
    public boolean isPalindrome(String s) {
  int i = 0;
  int j = s.length() -1;
   s = s.toLowerCase();
  while(i<j){
    
    if(!alphanumaric(s.charAt(i))){
      i++;
      continue;
    }
    if(!alphanumaric(s.charAt(j))){
      j--;
      continue;
    }

    if(s.charAt(i) != s.charAt(j)){
      return false;
    }
    i++;
    j--;
  }

  return true;
    }
}
```
