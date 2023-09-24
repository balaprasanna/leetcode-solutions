# leetcode-solutions

## LC75 Problems

1. 1768 https://leetcode.com/problems/merge-strings-alternately/
```py3
class Solution:
    def mergeAlternately(self, word1: str, word2: str) -> str:
        wc1 = len(word1)
        wc2 = len(word2)
        final_word = ""
        for i in range(min(wc1, wc2)):
            final_word += word1[i] + word2[i]
        final_word += word1[i+1:] + word2[i+1:]
        return final_word
```

