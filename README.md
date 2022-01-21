# 2138-divide_string_k_parts
java
import java.util.*;
class Solution {
    public String[] divideString(String s, int k, char fill) {
        while(s.length()%k!=0){
            s=s+fill;
        }
        int j=0,n=s.length()/k;
        String[] ans = new String[n];
        String temp="";
        for(int i=0;i<s.length();i++){
           temp=temp+s.charAt(i);
            if(temp.length()==k){
                ans[j]=temp;
                temp="";
                j++;
            }  
        }
    return ans;
    }
}
