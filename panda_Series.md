# 使用列表list、数组或者字典创建默认索引的Series
import pandas as pd
# 使用列表创建Series
s = pd.Series([1,2,3,4])

# 使用数组创建Series
s = pd.Series(np.array([1,2,3,4]))

# 使用字典创建Series
s = pd.Series({'a':1, 'b':2, 'c':3, 'd':4})

# 指定索引创建 Series
s = pd.Series([1,2,3,4]), index = ['a','b','c','d']

# 获取值
value = s[2]  # 获取索引为2的值
print(s['a'])  # 返回索引标签 'a' 对应的元素

# 获取多个值
value = s[1:3]  # 获取索引为1到3的值

# 使用自定义索引
index = s['b'] # 获取索引为'b'的值

# 索引和值的对应关系
for index,value in s.items():
    print(f"index:{index}, value:{value}")

# 使用切片语法来访问 Series 的一部分
print(s['a':'c'])  # 返回索引标签 'a' 到 'c' 之间的元素
print(s[:3])  # 返回前三个元素

# 为特定的索引标签赋值
s['a'] = 10  # 将索引标签 'a' 对应的元素修改为 10

# 通过赋值给新的索引标签来添加元素
s['4'] = 5 # 在 Series 中添加一个新的元素，索引标签为 'e'

# 使用 del 删除指定索引标签的元素。
del s['a']  # 删除索引标签 'a' 对应的元素

# 使用 drop 方法删除一个或多个索引标签，并返回一个新的 Series。
s_dropped = s.drop(['b'])  # 返回一个删除了索引标签 'b' 的新 Series


# 基本操作：
# 算术运算
result = series*2  # 所有元素乘以2

# 过滤
filtered_series = series[series > 2]  # 选择大于2的元素

# 数学函数
import numpy as np
    result = np.sqrt(series)  # 对每个元素取平方根
# 计算统计数据
print(s.sum())  # 输出 Series 的总和
print(s.mean())  # 输出 Series 的平均值
print(s.max())  # 输出 Series 的最大值
print(s.min())  # 输出 Series 的最小值

# 获取索引
index = s.index

# 获取值数组
values = s.values

# 获取描述统计信息
stats = s.describe()

# 获取最大值和最小值的索引
max_index = s.idxmax()
min_index = s.idxmin()

# 其他属性和方法
print(s.dtype)   # 数据类型
print(s.shape)   # 形状
print(s.size)    # 元素个数
print(s.head())  # 前几个元素，默认是前 5 个
print(s.tail())  # 后几个元素，默认是后 5 个
print(s.sum())   # 求和
print(s.mead())  # 平均值
print(s.std())   # 标准差
print(s.min())  # 最小值
print(s.max())   # 最大值

