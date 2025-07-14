# 79. Word Search

**Link:** https://leetcode.com/problems/word-search/submissions/1697202825/

AmazonTwitterUberKaratMicrosoftGiven an m x n grid of characters board and a string word, return true if word exists in the grid. The word can be constructed from letters of sequentially adjacent cells, where adjacent cells are horizontally or vertically neighboring. The same letter cell may not be used more than once.

```java
                if(dfs(i,j,board,visited,0,word)) return true;
            }
        }

        return false;
    }

    public boolean dfs(int r,int c,char[][] board,boolean[][] visited , int k, String word){
        if(k==word.length()) return true;


        if(r<0 || r>=row || c<0 || c>=col || visited[r][c]==true || board[r][c]!=word.charAt(k)) return 
false;

        visited[r][c]=true;

        boolean ans = dfs(r+1,c,board,visited,k+1,word) ||dfs(r-1,c,board,visited,k+1,word) ||dfs(r,c+1,
board,visited,k+1,word) || dfs(r,c-1,board,visited,k+1,word) ;

        visited[r][c]=false;

        return ans;

    }




}
```
