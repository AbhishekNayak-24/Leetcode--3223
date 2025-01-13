# Leetcode--3223
Minimum Length Of String After Operations
// code in java
public class Solution {
    public int minimumLength(String s) {
        int[] count = new int[26];
        // Count occurrences of each character
        for (char c : s.toCharArray()) {
            count[c - 'a']++;
        }
        int minLength = 0;
        // Calculate the minimum length
        for (int cnt : count) {
            if (cnt > 0) {
                minLength += (cnt % 2 == 1) ? 1 : 2;
            }
        }
        return minLength;
    }
}
