## Cosine similarity
Cosine similarity measures the cosine of the angle between two vectors in space, thereby indicating the similarity in direction between the vectors.  
```
import math

def dot_product(v1, v2):
    """计算两个向量的点积"""
    return sum(a*b for a, b in zip(v1, v2))

def magnitude(v):
    """计算向量的欧几里得范数（长度）"""
    return math.sqrt(dot_product(v, v))

def cosine_similarity(v1, v2):
    """计算两个向量的余弦相似度"""
    return dot_product(v1, v2) / (magnitude(v1) * magnitude(v2))

# 示例向量
vector1 = [1, 2, 3]
vector2 = [4, 5, 6]

# 计算余弦相似度
similarity = cosine_similarity(vector1, vector2)
print(f"The cosine similarity between the two vectors is: {similarity}")

```
这段代码首先定义了三个函数：dot_product计算两个向量的点积，magnitude计算一个向量的欧几里得范数，最后cosine_similarity利用前两个函数来计算两个向量的余弦相似度。这个方法适用于任意长度的向量，只要它们的长度相同。  
