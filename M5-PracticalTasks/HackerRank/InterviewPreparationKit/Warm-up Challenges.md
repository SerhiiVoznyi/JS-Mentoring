# [JavaScript Mentoring Program](../../../README.md)

[← Go back to](../README.md)

## Warm-up Challenges

[Arrays →](./ARRAYS.md)

___

### Sales by Match

There is a large pile of socks that must be paired by color. Given an array of integers representing the color of each sock, determine how many pairs of socks with matching colors there are.

**Example**

```javascript
n = 7
array = [1,2,1,2,1,3]
```

There is one pair of color **1** and one of color **2** There are three odd socks left, one of each color. The number of pairs is **2**.

**Function Description**

Complete the sockMerchant function in the editor below.

sockMerchant has the following parameter(s):

* int n: the number of socks in the pile
* int ar[n]: the colors of each sock

**Returns**

* int: the number of pairs

**Solution**

The general idea is to group array by its values. In javascript there are no `groupBy` function for array, but there are [reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)  function. We can use it to create array with count for each value. Then sum whole part of division by **2** without fractional part.

```javascript

function sockMerchant(n, ar) {
    // Define empty array for counts of values.
    const groups = [];

    // Using the 'reduce' function to update 'counts'.
    ar.reduce((groups, value) => {
        // This verification needed to set initial value of 0 to count. 
        // Otherwise we will have to sum undefined with a number, the result of such operation will be NaN - not a number.
        if(groups[value] === undefined)
        {
            groups[value] = 0;
        }
        // Increasing count of particular value on 1.
        groups[value] = groups[value] + 1;
        // Returning array of 'counts' as execution of 'reduce' function.
        return groups;
    }, groups);
 
    // Using the 'reduce' to summarize all counts divided by 2 without fractional part.
   return groups.reduce((partialSum, value) => partialSum + Math.trunc(value / 2), 0);
}

```

___

### Jumping on the Clouds

There is a new mobile game that starts with consecutively numbered clouds. Some of the clouds are thunderheads and others are cumulus. The player can jump on any cumulus cloud having a number that is equal to the number of the current cloud plus 1 or 2. The player must avoid the thunderheads. Determine the minimum number of jumps it will take to jump from the starting postion to the last cloud. It is always possible to win the game.

For each game, you will get an array of clouds numbered 0 if they are safe or 1 if they must be avoided.

**Example**

```javascript
c = [0,1,0,0,0,1,0]
```

Index the array from `0...6`. The number on each cloud is its index in the list so the player must avoid the clouds at indices `1` and `5`. They could follow these two paths: 
`0 → 2 → 4 → 6` or `0 → 2 → 3 → 4 → 6`. The first path takes `3` jumps while the second takes `4`. Return `3`.

**Function Description**

Complete the jumpingOnClouds function in the editor below.

jumpingOnClouds has the following parameter(s):

* int c[n]: an array of binary integers

**Returns**

* int: the minimum number of jumps required

**Solution**

As it is not possible to lose in this game we basically just need to check if we can always jump on `+2`. If not just increase index on `+1`, and repeat.

```javascript
function jumpingOnClouds(c) {
    const winCondition = c.length - 1;
    let jumps = 0;
    let index = 0;
    while(index < winCondition) {
        if(c[index+2] === 0) {
            index = index + 2;
        }
        else {
            index = index + 1;
        }
        jumps = jumps + 1;
    }    
    return jumps;    
}
```

___

### Counting Valleys

An avid hiker keeps meticulous records of their hikes. During the last hike that took exactly steps, for every step it was noted if it was an uphill, `U`, or a downhill, `D` step. Hikes always start and end at sea level, and each step up or down represents a `1` unit change in altitude. We define the following terms:

* A mountain is a sequence of consecutive steps above sea level, starting with a step up from sea level and ending with a step down to sea level.
* A valley is a sequence of consecutive steps below sea level, starting with a step down from sea level and ending with a step up to sea level.

Given the sequence of up and down steps during a hike, find and print the number of valleys walked through.

**Example**

```javascript
const steps = 8;
const path = 'DDUUUUDD';
```

**Function Description**

Complete the countingValleys function in the editor below.

countingValleys has the following parameter(s):

* int steps: the number of steps on the hike
* string path: a string describing the path

**Returns**

* int: the number of valleys traversed

**Input Format**

The first line contains an integer `steps`, the number of steps in the hike.
The second line contains a single string `path`, of `steps` characters that describe the path.

**Solution**


```javascript
function countingValleys(steps, path) {
    let result = 0;
    let currentLevel = 0;
    for (let step of path) {
        currentLevel += step === 'D' ? -1 : 1;
        if(currentLevel === 0 && step === 'U') {
            result += 1;
        }
    }
    return result;
}
```

___

### Counting Valleys

There is a string, `s`, of lowercase English letters that is repeated infinitely many times. Given an integer, `n`, find and print the number of letter **a**'s in the first `n` letters of the infinite string.

**Example**

```javascript
const s = 'abcac';
const n = 10;
```

The string `abcacabcac` contains `4` 'a's response should be `4`.

**Solution**


```javascript
function repeatedString(s, n) {
    // We not need to deal with chars we need to deal with values, where a is 1, everything else is 0.
    const values = s.split('').map(v => v === 'a' ? 1 : 0);
    
    // We will need to compare length os string many times so, better to have it as a constant.
    const valuesLength = s.length;
    
    // We can count initial sum of 'a's use reduce function.
    const initialSum = values.reduce((sum, v) => sum + v, 0);
    
    // In case if we have string with all 'a's we just need to return 'n'
    if(initialSum === valuesLength) {
        return n;
    }
    
    // In case if we have string where no 'a's we just need to return '0'
    if(initialSum === 0) {
        return 0;
    }
    
    // We need to find the last index of 'a' in the string.
    const lastIndexOfA = values.lastIndexOf(1);
    
    // We need to find the amount of repeats a string.
    const amountOfRepeats = Math.floor(n / valuesLength);

    let result = 0;
    
    // If Amount of repeats > 0 we can find sum just by multiplication amountOfRepeats on initialSum
    if(amountOfRepeats > 0)
    {
        result = amountOfRepeats * initialSum;
    }
    
    // Only thing is left to find the amount of characters we need to count.
    const leftToCount = n - amountOfRepeats * valuesLength;   
    for(let i = 0; i < leftToCount; i++) {
        result += values[i];
    }
    return result;
}
```
