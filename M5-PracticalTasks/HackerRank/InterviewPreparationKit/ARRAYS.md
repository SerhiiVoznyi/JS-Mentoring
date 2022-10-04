# [JavaScript Mentoring Program](../../../README.md)

[← Go back to](../README.md)

## Arrays

[Arrays →](./ARRAYS.md)

___
### [2D Array - DS](https://www.hackerrank.com/challenges/2d-array/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=arrays)

Given a 6 x 6 2D Array, :

```javascript
1 1 1 0 0 0
0 1 0 0 0 0
1 1 1 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
```

An hourglass in `A` is a subset of values with indices falling in this pattern in array's graphical representation:

```
a b c
  d
e f g
```

There are `16`  hourglasses in `arr`. An hourglass sum is the sum of an hourglass' values. Calculate the hourglass sum for every hourglass in `arr`, then print the maximum hourglass sum.

**Solution**




```javascript
function hourglassSum(arr) {
    const sums = [];
    for(let i = 0; i<= 3; i++)
    {
        for(let j = 0; j<= 3; j++)
        {
            sums.push(arr[i][j] + arr[i][j+1] + arr[i][j+2] + arr[i+1][j+1] + arr[i+2][j] + arr[i+2][j+1] + arr[i+2][j+2]);
        }
    }
    return Math.max(...sums);
}
```

___

### [Arrays: Left Rotation](https://www.hackerrank.com/challenges/ctci-array-left-rotation/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=arrays)

A left rotation operation on an array shifts each of the array's elements `1` unit to the left. For example, if `2` left rotations are performed on array `[1,2,3,4,5]`, then the array would become `[3,4,5,1,2]`. Note that the lowest index item moves to the highest index in a rotation. This is called a circular array.

Given an array `a` of `n` integers and a number, `d`, perform `d` left rotations on the array. Return the updated array to be printed as a single line of space-separated integers.

**Solution**

```javascript
function rotLeft(a, d) {
    const result = [];
    const length = a.split(' ')[0];
    console.log('length '+ length);
    const rotation = a.split(' ')[1];
    console.log('rotation '+ rotation);
    if(rotation % length === 0) {
        return d;
    }
    
    const array = d.split(' ');
    console.log('array '+ array);
    const diff = length - (Math.floor(rotation/length) * length + 1);
    
    console.log('diff '+ diff);
    let index = diff;
    for(let i = 0; i < diff; i++) {
        result.push(array[index]);
        index += 1;
    }
    
    index = 0;
    for(let i = diff; i < length; i++) {
        result.push(array[index]);
        index += 1;
    }
    
    return result.join(' ');
}
```

___