// Question-1. Two sum
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int>ans;
        for(int i=0;i<nums.size();i++){
            for(int j=i+1;j<nums.size();j++){
                if(nums[i]+nums[j]==target){
                    ans.push_back(i);
                    ans.push_back(j);
                    return ans;
                }
            }
        }
        return ans;
    }
};


// Question-2 Remove duplicates

class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int k=1;
        for(int i=1;i<nums.size();i++){
            if(nums[i]!=nums[k-1]){
                nums[k]=nums[i];
                k++;
            }
        }
       return k;
    }
};



// Question-3. Best time to buy and sell


class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int i,minx=INT_MAX,maxx=0;
        for( i=0;i<prices.size();i++){
            minx=min(minx,prices[i]);
           int  profit= prices[i]-minx;
           maxx=max(maxx,profit);
        }
        return maxx;    
    }

};

