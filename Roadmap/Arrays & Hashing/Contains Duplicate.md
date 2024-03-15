
Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

**Example 1:**

**Input:** nums = [1,2,3,1]
**Output:** true

**Example 2:**

**Input:** nums = [1,2,3,4]
**Output:** false

**Example 3:**

**Input:** nums = [1,1,1,3,3,4,3,2,4,2]
**Output:** true


**Constraints:**

- `1 <= nums.length <= 105`
- `-109 <= nums[i] <= 109`

The easiest approach would be to for each number combine it if it's the same as the rest in the array.
Implementation will have O(n^2) Time complexity and O(1) space complexity

Python
```run-python
def containsDuplicate(nums):
	for idx, x in enumerate(nums):
		for idy, y in enumerate(nums):
			if x == y & idx != idy:
				return True

	return False


print(containsDuplicate([1, 2, 3, 1]))
print(containsDuplicate([1, 2, 3, 4]))
print(containsDuplicate([1,1,1,3,3,4,3,2,4,2]))
```

Typescript
```run-typescript

function containsDuplicate(nums: number[]): boolean {
	for(let i=0; i< nums.length; i++){
		for(let y=0; y < nums.length; y++){
			if(i !== y && nums[i] === nums[y]){
				return true;
			}
		}
	}
	return false;
}

console.log(containsDuplicate([1,2,3,4]))
console.log(containsDuplicate([1,2,3,1]))
```

If we sort the input any duplicates that exist in the array will be adjacent. We would have time complexity of O(nlogn) because we need extra time for sorting, space complexity is O(1)

Python
```run-python
def containsDuplicate(nums):


print(containsDuplicate([1, 2, 3, 1]))
print(containsDuplicate([1, 2, 3, 4]))
print(containsDuplicate([1,1,1,3,3,4,3,2,4,2]))
		    
```

Typescript
```run-typescript

function containsDuplicate(nums: number[]): boolean {

}

console.log(containsDuplicate([1,2,3,4]))
console.log(containsDuplicate([1,2,3,1]))
```

Suppose we don't solve our inputs but we use extra memory using HashSet. This way we achieve time complexity of O(n) but we need to create HashSet so we sacrifise some of the space complexity which becomes O(n)

Python
```run-python
def containsDuplicate(nums):


print(containsDuplicate([1, 2, 3, 1]))
print(containsDuplicate([1, 2, 3, 4]))
print(containsDuplicate([1,1,1,3,3,4,3,2,4,2]))
		    
```

Typescript
```run-typescript

function containsDuplicate(nums: number[]): boolean {

}

console.log(containsDuplicate([1,2,3,4]))
console.log(containsDuplicate([1,2,3,1]))
```
