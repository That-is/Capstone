---------------------------------------------------------------------------------April 9
1. UNION ALL & UNION
 - union all 是简单地拼接所有的行，并不进行重复值的筛选
 - union是要筛除重复行的拼接
 
 2. STRING_SPLIT
 - 只能用在from语句之后
 - 例子：
 SELECT Value FROM STRING_SPLIT('this, is, very, important', ',')
 
 3.进行分组排序的时候
 SELECT *, row_num() OVER (partition by id order by quantity) as rank 
 FROM student
- (1)dense_rank的排列序数会减少 比如 1 1 2
- (2)rank的排列序数不会减少 比如 1 1 3
- (3)row_number的排列序号不会重复 比如1 2 3 

4.PERCENTILE_CONT(0.9) WITHIN GROUP(ORDER BY score ASC) OVER (partition by [Month])
    上面是针对连续性数值 给出的是一个近似的结果
   PERCENTILE_DISC(0.5) WITHIN GROUP(ORDER BY score  ASC) OVER (partition by [Month]) 
    上面的是针对离散的数值 给出的是一个精确的实际存在的数值结果
    
 5.主要的DATE函数
 6.python文件在写出的时候加上index = None就可以避免输出index
    插入csv文件的命令：
    BULK INSERT Weather
    FROM '路径'
    WITH(
    FIELDTERMINATOR =  ',',
    ROWTERMINATOR = '0x0a',
    FIRSTROW = 2
    KEEPNULLS
    )
    
 7. 命令行删除指定的列
 删除
 awk '{$1=""; print $0}' original_root, new_root
 保留
 awk '{print $1, $2}' original_root, new_root
 
 8.docker的命令
 从本地上传文件到docker里面
 docker cp '本地文件路径' 容器名：新的存储路径/文件名.csv
 
  