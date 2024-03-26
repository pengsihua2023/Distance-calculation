## Hamming distance
计算汉明距离通常是指计算两个字符串或两个相同长度的二进制数之间的差异，即它们对应位置上不同字符的数量。在信息理论中，汉明距离用于测量两个等长字符串之间的差异程度。  

下面是一个简单的Python函数，用于计算两个等长字符串的汉明距离：  
```
def hamming_distance(str1, str2):
    """计算并返回两个等长字符串之间的汉明距离"""
    if len(str1) != len(str2):
        raise ValueError("The two strings must be of equal length.")
    
    return sum(c1 != c2 for c1, c2 in zip(str1, str2))

# 示例
str1 = "karolin"
str2 = "kathrin"

distance = hamming_distance(str1, str2)
print(f"The Hamming distance between '{str1}' and '{str2}' is: {distance}")
```
此代码首先检查两个字符串长度是否相等，如果不等，则抛出一个ValueError。接着，使用zip函数将两个字符串合并为一个元组序列，其中每个元组包含来自两个字符串的相应字符。最后，通过遍历这些元组并计算字符不同的位置数量来确定汉明距离。使用列表推导式和sum函数，可以简洁地计算出汉明距离。  

如果你想计算两个二进制数之间的汉明距离，可以先将它们转换为等长的二进制字符串，然后使用上述函数计算汉明距离。  
