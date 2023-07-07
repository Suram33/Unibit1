def find_pairs(nums, target):
    # Step 2: Create an empty list called `pairs`
    pairs = []
    num_dict = {}

    for num in nums:
        complement = target - num
        # Step 6: Check if the complement exists in `num_dict`
        if complement in num_dict:
            # Step 7: Append the pair [num, complement] to the `pairs` list
            pairs.append([num, complement])
        # Step 8: Add the current number `num` as a key in `num_dict`
        num_dict[num] = True

    # Step 9: Return the `pairs` list
    return pairs

def merge_and_sort(nums):
    # Step 11: Sort the `nums` array in ascending order
    nums.sort()
    # Step 12: Return the sorted `nums` array
    return nums

def find_combinations(nums, target):
    # Step 14: Create an empty list called `combinations`
    combinations = []
    num_dict = {}

    for num in nums:
        complement = target - num
        # Step 17: Check if the complement exists in `num_dict`
        if complement in num_dict:
            # Step 18: Append the combination [num, complement] to the `combinations` list
            combinations.append([num, complement])
        # Step 19: Add the current number `num` as a key in `num_dict`
        num_dict[num] = True

    # Step 20: Return the `combinations` list
    return combinations

# Sample input
nums = [1, 3, 2, 2, -4, -6, -2, 8]
target = 4

# Find pairs that sum up to the target
pairs = find_pairs(nums, target)
print("First Combination for", target, ":", pairs)

# Merge into a single array and sort
merged_nums = merge_and_sort(nums)
print("Merged and Sorted Array:", merged_nums)

# Double the target and find combinations
doubled_target = target * 2
combinations = find_combinations(merged_nums, doubled_target)
print("Second Combination for", doubled_target, ":", combinations)
