# orangeFinancialCupCompetition
[Sweet Orange Financial Cup Big Data Modeling Competition](http://www.dcjingsai.com/common/cmpt/2018%E5%B9%B4%E7%94%9C%E6%A9%99%E9%87%91%E8%9E%8D%E6%9D%AF%E5%A4%A7%E6%95%B0%E6%8D%AE%E5%BB%BA%E6%A8%A1%E5%A4%A7%E8%B5%9B_%E8%B5%9B%E4%BD%93%E4%B8%8E%E6%95%B0%E6%8D%AE.html)

### 1. 数据集
分为训练数据集、初赛测试数据集、复赛测试数据集。


- #### 读取使用
通过 `pandas` 可以直接读取已压缩为 `xz` 的 `csv` 文件内容
eg:
```python
operation_train = pd.read_csv('data/operation_train_new.csv.xz', compression='xz')
```

- #### 训练数据集
训练数据集中的文件包含黑白样本标签、用户交易详单、用户操作详单。    
初赛和复赛的测试集数据中则只包含用户交易详单、用户操作详单。    
以下先简介数据集的文件名，然后再详述每个数据的所有字段。    
1. operation_train_new.csv为训练集操作详情表单，共1460843条数据；
2. transaction_train_new.csv为训练集交易详情表单，共264654条数据；
3. tag_train_new.csv为训练集黑白样本标签，共31179 条数据。

- #### 测试数据集

测试集初赛数据集：
1. operation_round1_new.csv为初赛测试集操作详情表单，共1769049条数据；
2. transaction_round1_new.csv为初赛测试集交易详情表单，共168981条数据；
> 注意：初赛测试集的日期数据（day）也是从1开始，但这里的日期1和训练集中的日期1不是同一天，而是指初赛测试集中的第一天的数据。
  （同理，请区分复赛测试集中的日期与其他数据集中的日期）
  
 详细字段如下:
 ![detail_description](/images/1.png)
