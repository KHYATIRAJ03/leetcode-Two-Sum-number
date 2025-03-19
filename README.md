Two Sum Solution
📝 Problem Description
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to the target.

Example 1
makefile
Copy
Edit
Input: nums = [2,7,11,15], target = 9  
Output: [0,1]  
Explanation: nums[0] + nums[1] == 9 → [0, 1]
Example 2
makefile
Copy
Edit
Input: nums = [3,2,4], target = 6  
Output: [1,2]  
Example 3
makefile
Copy
Edit
Input: nums = [3,3], target = 6  
Output: [0,1]  
🚀 Solution Approach
Brute Force Method (O(n²) time complexity):
Use nested loops to iterate through all pairs and check if their sum equals the target.
Optimized Method (O(n) time complexity):
Use a dictionary (hash map) to store visited numbers and their indices.
For each number num at index i, calculate complement = target - num.
Check if the complement exists in the dictionary.
If yes, return the indices of num and its complement.
🛠️ Code
python
Copy
Edit
def two_sum(nums, target):
    num_map = {}  # Dictionary to store the index of each number
    
    for i, num in enumerate(nums):
        complement = target - num
        
        if complement in num_map:
            return [num_map[complement], i]
        
        num_map[num] = i

# Example usage
nums = [2, 7, 11, 15]
target = 9
print("Output:", two_sum(nums, target))  # Output: [0, 1]
⚙️ How to Run
Save the code in a file, e.g., two_sum.py
Open a terminal or command prompt.
Run the command:
nginx
Copy
Edit
python two_sum.py
✅ Complexity Analysis
Time Complexity: 
𝑂
(
𝑛
)
O(n)
Space Complexity: 
𝑂
(
𝑛
)
O(n)
🛠️ Test Cases
yaml
Copy
Edit
Input: [2, 7, 11, 15], Target: 9 → Output: [0, 1]  
Input: [3, 2, 4], Target: 6 → Output: [1, 2]  
Input: [3, 3], Target: 6 → Output: [0, 1]  
