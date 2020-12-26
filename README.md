# algorithm
算法/笔试博客
## 每天一道算法题 --2020.12.20
### 排序
冒泡排序

选择排序

插入排序

快速排序

### 两数之和
    给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。
    你可以假设每种输入只会对应一个答案。但是，数组中同一个元素不能使用两遍。

    示例:
    给定 nums = [2, 7, 11, 15], target = 9

    因为 nums[0] + nums[1] = 2 + 7 = 9
    所以返回 [0, 1]

####解法一：暴力解法
利用for循环，两个数相加 === target
```js
const twoSum = function(nums, target) {
    for(let i = 0; i < nums.length-1; i++) {
        for(let j=i+1;j<nums.length;j++){
            if(nums[i]+nums[j] === target){
                return [i,j]
            }
        }
    }
}
console.log(twoSum([2, 7, 11, 15],18))
```
