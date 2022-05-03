class Solution {
   public static ArrayList<String> findPath(int[][] m, int n) {
      if(m[0][0]==0) return new ArrayList<>();
      ArrayList<String> ans = solve(m,"",0,0,n);
      return ans;
      
   }
   
   static ArrayList<String> solve(int[][] m,String ans,int r ,int c,int n){
       if(r== n-1  && c == n-1 && m[r][c] == 1){
           ArrayList<String> temp = new ArrayList<>();
           temp.add(ans);
           return temp;
       }
       m[r][c] = -1;
       ArrayList<String> temp1 = new ArrayList<>();
       if(r+1 < n && m[r+1][c] == 1){
           temp1.addAll(solve(m,ans+"D",r+1,c,n));
           m[r][c]=0;
       }
       if(c-1 >=0 && m[r][c-1] == 1){
           temp1.addAll(solve(m,ans+"L",r,c-1,n));
            m[r][c]=0;
       }
       if(c+1 < n && m[r][c+1] == 1){
           temp1.addAll(solve(m,ans+"R",r,c+1,n));
            m[r][c]=0;
       }
       if(r-1 >=0 && m[r-1][c] == 1){
           temp1.addAll(solve(m,ans+"U",r-1,c,n));
            m[r][c]=0;
       }
       m[r][c] = 1;
       return temp1;
   }
   
}