🚀 接口说明文档 - 障碍物地图输入格式
📌 文件功能说明
本文件用于提供三维障碍物地图数据，用于路径规划系统读取环境信息。
地图将以 20×20×20 三维栅格的形式表示，值为：

0：表示该位置为空，可通行

1：表示该位置为障碍物，不可通行

📂 文件格式要求
文件类型：.txt 或 .csv

内容结构：共包含 20 × 20 × 20 = 8000 个整数值（0 或 1）

排列方式：建议采用 Z-Y-X 顺序展开为一维数组，或如下三种常见格式之一：

✅ 推荐格式一：平面切片形式（每层一个 20x20）
txt
复制
编辑
# 第1层（Z=1）
0 0 1 0 0 1 ... 共20列
...
# 共20行

# 第2层（Z=2）
...
✅ 推荐格式二：JSON数组（三维数组结构）
json
复制
编辑
[
  [  [0,0,1,...], ..., [0,1,0,...]  ],  // Z = 1层（20×20）
  [  [...], ..., [...] ],              // Z = 2层
  ...
]
✅ 推荐格式三：逗号分隔值（CSV，Z-Y-X顺序，展开为一维）
csv
复制
编辑
0,0,1,0,0,1,... 共8000个值
📌 数据示例（格式一，Z=1层举例）
txt
复制
编辑
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0  
0 1 1 1 0 0 0 0 0 0 0 0 1 1 1 0 0 0 0 0  
...
# 共20行
