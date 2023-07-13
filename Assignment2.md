Q1.
```javascript
   let nums = [1, 4, 3, 2];
nums.sort((a, b) => a - b);

let sum = 0;
for (let i = 0; i < nums.length; i += 2) {
  sum += nums[i];
}
console.log(sum);
```
Q2.
```javascript
function maxCandies(candyType) {
  let uniqueCandyType = new Set(candyType);
  let maxCandiesAlice = Math.floor(candyType.length / 2);
  return Math.min(uniqueCandyType.size, maxCandiesAlice);
}

let candyType = [1, 1, 2, 2, 3, 3];
console.log(maxCandies(candyType));
```
Q3.
```javascript
function findLHS(nums) {
  const frequency = {};
  
  for (let num of nums) {
    frequency[num] = (frequency[num] || 0) + 1;
  }
  
  let maxLen = 0;
  
  for (let num in frequency) {
    num = parseInt(num);
    if (frequency[num + 1]) {
      const length = frequency[num] + frequency[num + 1];
      maxLen = Math.max(maxLen, length);
    }
  }
  
  return maxLen;
}

const nums = [1, 3, 2, 2, 5, 2, 3, 7];
console.log(findLHS(nums)); // Output: 5
```
Q4.
```javascript
  let nums=[1,0,0,0,1];
  let n=1;
  let count =0;

  for(let i=0; i<nums.length; i++)
  {
    if(nums[i]==0){
      count=count+1;
    }
  }

  if(count%2!=0 && count/2 +1>=n){
    console.log("true");
  }
  else{
    console.log("false");
  }
```
Q5.
```javascript
function maximumProduct(nums) {
  nums.sort((a, b) => a - b);

  const n = nums.length;
  const product1 = nums[n - 1] * nums[n - 2] * nums[n - 3];
  const product2 = nums[0] * nums[1] * nums[n - 1];

  return Math.max(product1, product2);
}
const nums = [1, 2, 3];
console.log(maximumProduct(nums));
```
Q6. 
```javascript
function search(nums, target) {
  let l = 0;
  let r = nums.length - 1;
  
  while (l <= r) {
    const m = Math.floor((l + r) / 2);
    
    if (nums[m] === target) {
      return m;
    } else if (nums[m] > target) {
      r = m - 1;
    } else {
      l = m + 1;
    }
  }
  
  return -1;
}


const nums = [-1, 0, 3, 5, 9, 12];
const target = 9;
console.log(search(nums, target)); // Output: 4
```
Q7. 
```javascript
function checkMonotonic(nums) {
	for (let i = 0; i < nums.length - 1; i++) {
		if (nums[i] > nums[i + 1]) {
			return false;
		}
	}
	for (let i = 0; i < nums.length - 1; i++) {
		if (nums[i] < nums[i + 1]) {
			return false;
		}
	}
	return true;
}
```
Q8.
```javascript
function minScore(nums, k) {
  let minNum = Math.min(...nums);
  let maxNum = Math.max(...nums);

  if (minNum + k >= maxNum - k) {
    return maxNum - minNum;
  } else {
    return maxNum - k - (minNum + k);
  }
}

const nums = [1];
const k = 0;
console.log(minScore(nums, k)); // Output: 0
```