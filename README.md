121.

class Solution 
public:
    int maxProfit(vector<int>& prices) {
        int minprice = ::numeric_limits<int>::max();
        int maxProfit = 0 ;
        for(int j = 0; j < prices.size() ;j++ ){
            if(prices[j] < minprice)
                minprice = prices[j];
            
            else
                maxProfit = max(maxProfit,prices[j]-minprice);
        }
        //cout << max(j - i)<< endl;
        return (maxProfit);
    }
};
