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

# -- sol2
class Solution:
    def mergeAlternately(self, word1: str, word2: str) -> str:
        wc1, wc2 = len(word1),  len(word2)
        final_word = ""
        i = 0
        while (i < wc1 or i < wc2):
            if i < wc1:
                final_word += word1[i]
            if i < wc2:
                final_word += word2[i]
            i += 1
        return final_word

```

2. 1431 https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/
```py3
class Solution:
    def kidsWithCandies(self, candies: List[int], extraCandies: int) -> List[bool]:
        n = len(candies)
        currMax = max(candies)
        return [candies[idx] + extraCandies >= currMax for idx in range(n)]
            
```