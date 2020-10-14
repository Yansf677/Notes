# Simple Markdown 

## ++1. 标题++
### 1.1 写法：
    一级标题: # Text
    二级标题: ## Text
    三级标题: ### Text
    四级标题: #### Text
    五级标题: ##### Text
    六级标题: ######Text

### 1.2 效果：
# Text
## Text
### Text
#### Text
##### Text
###### Text

## ++2. 字体调整++
### 2.1 写法：
    字体: <font face="黑体" color=green size=5>Text</font>
    加粗: **Text** 
    斜体: *Text*
    删除线: ~~Text~~
    下划线: ++Text++
    高亮文本: ==Text==

### 2.2 效果：
<font face="STCAIYUN" color=blue size=5>Text</font>  
**Text**  
*Text*  
~~Text~~  
++Text++  
==Text==

## ++3. 特殊符号++
### 3.1 写法：
    水平线: --- or ***
    引用文本: > Text
    复选框未选中状态: - [ ] Text
    复选框选中状态: - [x] Text

### 3.2 效果：
---
> Text
- [ ] Text
- [x] Text

## ++4. 各类链接++
### 4.1 写法：
    超链接: [](url)
    图片: ![caption](url)
    图片格式: <img src="http://static.runoob.com/images/runoob-logo.png" width="50%">
    公式: ```math E = mc^2 ```
    代码块: ``` Text ```

### 4.2 效果：
[Baidu](www.baidu.com)  
![Youdao](https://note.youdao.com/favicon.ico)  

```math
E = mc^2 
```
```
 Code 
```

## ++5. 列表表格++
### 5.1 写法：
    无序列表: - Text or * Text or + Text
    有序列表: 1. Text
    嵌套列表: 另起一行空三/四格
    表格: 如下
    header 1 | header 2
    ---|--- (---居中；:--左偏；--:右偏)
    row 1 col 1 | row 1 col 2
    row 2 col 1 | row 2 col 2

### 5.2 效果：
- Main Text   
   - Sub Text 
      1. Text

header 1 | header 2 | 
:--|--:
row 1 col 1 | row 1 col 2
row 2 col 1 | row 2 col 2

## ++6. 流程图++
### 6.1 横向流程图
    ```
    graph LR
    A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1]
    C -->|a=2| E[结果2]
    ```
```
graph LR
A[方形] -->B(圆角)
B --> C{条件a}
C -->|a=1| D[结果1]
C -->|a=2| E[结果2]
```
### 6.2 纵向流程图
    ```
    graph TD
    A[方形] --> B(圆角)
    B --> C{条件a}
    C --> |a=1| D[结果1]
    C --> |a=2| E[结果2]
    ```
```
graph TD
A[方形] --> B(圆角)
B --> C{条件a}
C --> |a=1| D[结果1]
C --> |a=2| E[结果2]
```
### 6.3 标准横向流程图
    ```flow
    st=>start: 开始框
    op=>operation: 处理框
    cond=>condition: 判断框(是或否?)
    sub1=>subroutine: 子流程
    io=>inputoutput: 输入输出框
    e=>end: 结束框
    st(right)->op(right)->cond
    cond(yes)->io(bottom)->e
    cond(no)->sub1(right)->op
    ```
```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st(right)->op(right)->cond
cond(yes)->io(bottom)->e
cond(no)->sub1(right)->op
```
### 6.4 标准纵向流程图
    ```flow
    st=>start: 开始框
    op=>operation: 处理框
    cond=>condition: 判断框(是或否?)
    sub1=>subroutine: 子流程
    io=>inputoutput: 输入输出框
    e=>end: 结束框
    st->op->cond
    cond(yes)->io->e
    cond(no)->sub1(right)->op
    ```
```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st->op->cond
cond(yes)->io->e
cond(no)->sub1(right)->op
```
### 6.5 时序图
    ```
    sequenceDiagram
    %% 时序图例子,-> 直线，-->虚线，->>实线箭头
    participant 张三
    participant 李四
    张三->王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 按行顺序
    李四-->>张三: 很好!
    王五->李四: 你怎么样?
    李四-->王五: 很好!
    ```
```
sequenceDiagram
%% 时序图例子,-> 直线，-->虚线，->>实线箭头
participant 张三
participant 李四
张三->王五: 王五你好吗？
loop 健康检查
    王五->王五: 与疾病战斗
end
Note right of 王五: 按行顺序
李四-->>张三: 很好!
王五->李四: 你怎么样?
李四-->王五: 很好!
```
### 6.6 甘特图
    ```
    gantt
    dateFormat  YYYY-MM-DD
    title 软件开发甘特图
    section 设计
        需求             :done,    des1, 2014-01-06,2014-01-08
        原型             :active,  des2, 2014-01-09, 3d
        UI设计           :         des3, after des2, 5d
        未来任务         :         des4, after des3, 5d
    section 开发
        学习准备理解需求 :crit, done, 2014-01-06, 24h
        设计框架         :crit, done, after des2, 2d
        开发             :crit, active, 3d
        未来任务         :crit, 5d
        耍               :2d
    section 测试
        功能测试         :active, a1, after des3, 3d
        压力测试         :after a1  , 20h
        测试报告         :48h
    ```
```
gantt
dateFormat  YYYY-MM-DD
title 软件开发甘特图
section 设计
    需求             :done,    des1, 2014-01-06,2014-01-08
    原型             :active,  des2, 2014-01-09, 3d
    UI设计           :         des3, after des2, 5d
    未来任务         :         des4, after des3, 5d
section 开发
    学习准备理解需求 :crit, done, 2014-01-06, 24h
    设计框架         :crit, done, after des2, 2d
    开发             :crit, active, 3d
    未来任务         :crit, 5d
    耍               :2d
section 测试
    功能测试         :active, a1, after des3, 3d
    压力测试         :after a1  , 20h
    测试报告         :48h
```

