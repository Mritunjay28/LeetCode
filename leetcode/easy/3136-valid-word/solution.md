# 3136. Valid Word

**Link:** https://leetcode.com/problems/valid-word/submissions/1698335672/

A word is considered valid if: It contains a minimum of 3 characters. It contains only digits (0-9), and English letters (uppercase and lowercase). It includes at least one vowel. It includes at least one consonant. You are given a string word. Return true if word is valid, otherwise, return false. Notes: 'a', 'e', 'i', 'o', 'u', and their uppercases are vowels. A consonant is an English letter that is not a vowel.

```java
            if(Character.isLetterOrDigit(ch)){
                if(ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U'||ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u') vowel++;
                else if(ch >= '0' && ch <= '9') digit++;
                else consonant++;
            }
            else return false ;
        }

        if(vowel+consonant+digit<3) return false;
        if(vowel<1) return false;
        if(consonant<1) return false ;

        return true;

    }
}

        for(char ch :word.toCharArray()){
        int vowel =0,consonant=0,digit=0;
    public boolean isValid(String word) {
```
