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