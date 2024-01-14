___
# COPY() VS. DEEPCOPY()
Links: [[Python]]
Status: #🌳 
Tags: [[PyTorch]]

<!--- Created on: 2023.12.06, 18:36 --->

- `copy()` creates a new object with references to the same nested elements as the original object; (only!) changes to nested mutable elements affect both the original and copied objects
- `deepcopy()` creates a new object with completely duplicated nested elements; changes made to the copied object's nested elements don't affect the original object (at all!)
___

# Changing a Nested List
```python
import copy

original_list = [1, [2, 3], 4]

# Shallow copy - references to nested elements are shared
shallow_copied_list = original_list.copy()

# Deep copy - all elements and their contents are duplicated
deep_copied_list = copy.deepcopy(original_list)

# Modifying the nested list in the shallow copy affects the original list
shallow_copied_list[1].append(100)
print(original_list)  # Output: [1, [2, 3, 100], 4]

# Modifying the nested list in the deep copy doesn't affect the original list
deep_copied_list[1].append(200)
print(original_list)  # Output: [1, [2, 3], 4]
```

# Changing a Simple Element
```python
original_list = [1, [2, 3], 4]
shallow_copied_list = original_list.copy()

# Modifying the first element in the shallow copy
shallow_copied_list[0] = 2

print(original_list)  # Output: [1, [2, 3], 4]
print(shallow_copied_list)  # Output: [2, [2, 3], 4]
```