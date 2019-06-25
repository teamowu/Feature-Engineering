# Data Types
数据可以是定性的或定量的。
- **定性数据**：描述性信息（它描述某事物）
    - Categorical

**例如**：['它是黑色的', '它的毛很长', '它是好动的']

- **定量数据**：数值信息（Numeric）。
    - 离散数据：只可以是某些既定的值（例如整数）
        - 特点：可数（countable）
    - 连续数据：可以是在一个范围内的任何值
        - 特点：可测量（measurable）

**例如**：{'离散'：['它有4条腿','它有两个兄弟'], '连续':['它的体重是25.5kg','它的身高是565mm']}

---
## Common dtypes in DataSet
### 1.Numeric
- Discrete: Count; Rating; Grade
- Continuous: Revenue; Distance; Home Value

**Watch OUT:** data range!
### 2.Binary(Dummy)
只用0和1记数。
- Special case of numeric

**Watch OUT:** IsMale ; HasHair ; Pass/Fail
### 3.Categorical
- Usually contains characters : Gender, Product, Geo, etc.
- Can be consist of pure numbers : SSN, Zipcode, Phone Number

**Watch OUT:** Valid Values
### 4.Dates and Time
- Date, Time, Datetime, Timestamp

**Watch OUT:** Time Zone!
### 5.Missing
- Null
    - Absence of everything; missing ; empty
- Blank
    - ""or"" or anything invisible character
    - Can mean missing
    - Can mean "N/A"
- N/A
    - Can mean "not available" : e.g.Age
    - Can mean "not applicable" : e.g.Middle Name
    - Can mean "no answer" : e.g.Customer Satisfaction Rating on a Questionnaire.
    
---
## Data quality issue
数据集中可能包含部分数据是无效/无用的。
- 不合理的记数：Incorrect / Invalid Entry
    - age = 203; gender = 'X'; price = -100; weekday = 8
- 缺失值：Missing Data
    - N/A; Null; “ ” ；Unknown
- 非结构化数据：Unstructured Data
    - merged cell ; double header; html
- 歧义数据：Conflicting Data
    - revenue = 1000 ; unit = 0
- 重复数据：Duplicates
    - double loading; double counting

---

## Data Preparation Step
1.Data Access\
2.Data Cleansing
- 合并数据(integrate): integrate various data sources; integrate multiple columns
    - Merge sales units; sales revenue; price into one DataSet;
    - Combine year, month and date
- 数据一致化(Conform): Conform the inconsistent values.
    - Na,n/a => missing
    - Los Angeles, L.A. => LA
- 筛选(Filter): Filter out the columns and rows not needed for modeling
- 组合(Group): Group many categorical values into a few buckets
- 聚合(Aggregate): Aggregate/Disaggregate date to the desired dimensions.
- 延申(Derive): Extract or Calculate new metrics based on existing metrics.
    - Price = Revenue/Units
    - Extract seasonality from sales
    - Regex
    
3.Handling Missing Data
- 删除缺失值
- 数据补全
- 忽略缺失值

4.Identity Outlier\
5.Transform Data(data preprocessing)
- 无量纲化
    - 正则化(Normalization)
    - 标准化(Standardization)
    - 区间缩放法(MinMaxScaler)
- 特征二元化
- 独热编码
- 对数变换
