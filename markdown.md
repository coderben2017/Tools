# 优雅的程序员文档编辑语言 —— Markdown

### 常用标记符号整理

1. 标题
- 一级标题 #...
- 二级标题 ##...
- 三级标题 ###...
- 四级标题 ####...
- 五级标题 #####...
- 六级标题 ######...

2. 斜体（一对 * 或 _ 包裹）
- *斜体文字*

3. 粗体（两对 * 或 _ 包裹）
- __粗体文字__

4.无序列表（由 * 、 - 或 + 开头，与文字内容之间空一个格）
- 列表项1
- 列表项2
- 列表项3

5.有序列表（数字 + . + 空格 + 文字）
- 1.(空格)列表项1
- 2.(空格)列表项2
- 3.(空格)列表项3

6.块注释（若干个> + 空格 + 文字）
> 一级块注释
>> 二级块注释
>>> 三级块注释

7.文字超链接
- 内联方式： [文字](链接地址)
- 引用方式： [1]:http://www.baidu.com/ "引用1"

8.图片超链接
- 内联方式： ! + [替换文字] + (图片地址) + {:width="400" height="300"}
- 引用方式： ! + [替换文字] + (图片地址)

9.下划线
- 使用html语法解决：< span style="border-bottom:2px dashed yellow;"> 所添加的需要加下划线的行内文字 </span>
