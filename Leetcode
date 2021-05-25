//Two Sum

#include<bits/stdc++.h>
using namespace std;

class Solution {
public:
    
      vector<int> twoSum(vector<int>& nums, int target) {
                map<int,int> m;
                vector<int> v;
                int n= nums.size();
                for(int i=0;i<n;i++)
                {
                    
                        int diff = target - nums[i];
                        if(m.find(diff) != m.end())
                        {
                        auto p = m.find(diff);        
                        v.push_back(p->second);
                        v.push_back(i);
                        }
                        m.insert(make_pair(nums[i],i));
                }
          
                return v;
}
};

//Maximum 69 Number

class Solution {
public:
    int maximum69Number (int num) {
        int i{1000};
        while(i != 0 && (num / i) % 10 != 6)
            i /= 10;
        return num + 3*i;
    }
};

//Count of Matches in a tournament

class Solution {
public:
    int numberOfMatches(int n) {
        int ans = 0;
        while(n>0)
        {
            ans = ans + n/2;
            n = (n+1)/2;
            if (n==1)
                break;
        }
        
        return ans;
    }
};

//Design Parking System

class ParkingSystem {
public:
    
    int big, medium, small;
    
    ParkingSystem(int big, int medium, int small) {
        this->big = big;
        this->medium = medium;
        this->small = small;
    }
    
    bool addCar(int c) {
        if(c == 1) {
            if(big > 0 ) { 
                big--;
                return 1;
            }else return 0;
        }
        
        if(c == 2) {
            if(medium > 0 ) { 
                medium--;
                return 1;
            }else return 0;
        }
        
        if(c == 3) {
            if(small > 0 ) { 
                small--;
                return 1;
            }else return 0;
        }
        
        return 0;
    }
};

//Min Stack

class MinStack {
    int stack[10000];
    int min[10000];
    int topPtr;
    int minPtr;
public:
    /** initialize your data structure here. */
    MinStack() {
        topPtr = -1;
        minPtr = -1;
    }
    
    void push(int x) {
        if(topPtr >= 10000)
            return;
        
        stack[++topPtr] = x;
        
        if(minPtr >= 0)
        {
            if(min[minPtr] > x)
                min[++minPtr] = x;
            else
            {
                min[minPtr+1] = min[minPtr];
                minPtr += 1;
            }
        }
        else
            min[++minPtr] = x;
                
    }
    
    void pop() {
        if(topPtr < 0)      //Underflow
            return;
        
        topPtr -= 1;
        minPtr -= 1;
    }
    
    int top() {        
        return stack[topPtr];
    }
    
    int getMin() {
        return min[minPtr];
    }
};


//Can place flowers

class Solution {
public:
    bool canPlaceFlowers(vector<int>& flowerbed, int n) {
        flowerbed.insert(flowerbed.begin(),0);
        flowerbed.push_back(0);
        for(int i = 1; i < flowerbed.size()-1; ++i)
        {
            if(flowerbed[i-1] + flowerbed[i] + flowerbed[i+1] == 0)
            {
                --n;
                ++i;
            }
                
        }
        return n <=0;
    }
};

//Contains Duplicate

class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        map <int, int> countMap;
        for (int i = 0; i < nums.size(); i++)
        {
            if(countMap[nums[i]])
            {
                return true;
            }
            countMap[nums[i]]++;
        }
        return false;
    }
};

//Move zeroes

class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        
        int n = nums.size();
        if(n==0 || n==1)
            return;
        
        int left=0, right=0;
        int temp;
        //Rearrangement
        while(right < n)
        {
            if(nums[right]==0)
                ++right;
            else
            {
                temp = nums[left];
                nums[left] = nums[right];
                nums[right] = temp;
                ++left;
                ++right;
            }
        }
    }
};

//Check if Two String Arrays are Equivalent

class Solution {
public:
    bool arrayStringsAreEqual(vector<string>& word1, vector<string>& word2) {
        string s1, s2;
        for (string str: word1)
        {
            s1 += str;
        }
        for (string str: word2)
        {
             s2 += str;
        }
        return s1==s2;
  }
};

//Find all duplicates in an Array

class Solution {
public:
    vector<int> findDuplicates(vector<int>& nums) {
        vector<int> result;
        for(int n : nums){
            n = abs(n);
            if(nums[n-1] > 0) nums[n-1] *= -1;
            else result.push_back(n);
        }
        return result;
    }
};
