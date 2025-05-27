#TWO SUMS
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        ht = {}

        for i, num in enumerate(nums):
            if target - num in ht:
                return [ht[target - num], i]
                
            ht[num] = i
            
        return []

#coin change


        class Solution {
    public int coinChange(int[] coins, int amount) {
        int dp []=new int [amount+1];
        Arrays.fill(dp,amount+1);
        dp[0]=0;
        for(int i=1;i<=amount;i++){
            for(int coin:coins){
                if(coin<=i){
                    dp[i]=Math.min(dp[i],dp[i-coin]+1);
                }
            }
        }
        return dp[amount]!=amount+1 ? dp[amount]:-1;
    }
}
