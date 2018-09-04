Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string "".

Example 1:

Input: ["flower","flow","flight"]
Output: "fl"

Example 2:

Input: ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.

Note:

All given inputs are in lowercase letters a-z.


```
/**
 * @param {string[]} strs
 * @return {string}
 */
var longestCommonPrefix = function(strs) {
    if (strs.length == 0) return "";
    let first = strs[0]
    for(let i=1;i<strs.length;i++) { 
       while(strs[i].indexOf(first) != 0){
              first = first.substring(0, first.length - 1);
            if (first == '') return ''
       } 
    }
    
    return first
    
};