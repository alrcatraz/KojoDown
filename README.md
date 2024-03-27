# KojoDown
 KojoDown，一款基于MarkDown的语法，用于编写ERA游戏口上
 A series of rules based on MarkDown, aiming at writing Kojo for ERA games

# 书写语法 / Rules
大部分的语法与MarkDown相同，但添加了部分新的规则，用以提供口上文件需要的功能，或根据口上制作的需要对既有功能进行强化。
Most of the rules are same as MarkDown, while there are some new rules added to provide features needed for Kojo files, or to enhance the existing features according to the needs of Kojo making.

总的来说，KojoDown的语法基于commonmark，但吸收了GFM的表格功能，然后再增加了一些新的规则。
In general, the syntax of KojoDown is based on commonmark, but absorbs the table feature of GFM, and then adds some new rules.

## 标题层级 / Headings
使用\#来标志标题层级，一个\#代表一级标题，两个\#代表二级标题，以此类推，**最多到六级标题**。
Use \# to indicate the heading level, one \# represents level 1 heading, two \# represents level 2 heading, and so on, **up to level 6 heading**.

使用\#来设置标题时，后面**紧跟一个空格**，然后是标题内容。
When using \# to set the heading, there should be a **space immediately following** the \#, then the heading content.

使用\{ \}来标志当前标题下所涵盖的文本范围，这一功能用于强化MarkDown的标题层级，从而满足口上事件经常出现一个事件中间包含一个小事件，在其后又有原事件的文本的情况。
Use \{ \} to indicate the range of text covered by the current heading, this feature is used to enhance the heading level of MarkDown, so as to meet the situation that a kojo event often contains a small event in the middle, and then has the text of the original event.

## 列表 / Lists
无序列表使用\*或\-来表示，**后面紧跟一个空格**，然后是列表项的内容。
Unordered lists are indicated by \* or \-, **followed by a space**, then the content of the list item.

有序列表使用数字和\.来表示，**后面紧跟一个空格**，然后是列表项的内容。
Ordered lists are indicated by numbers and \., **followed by a space**, then the content of the list item.

## 表格 / Tables
表格的书写方式和GFM规则的MarkDown相同，不同栏之间用\|分隔，表格左右边界均标记\|。首先先写一行表头，然后写一行用一组短横代替内容的分隔行，然后写表格内容。
The writing style of tables is the same as GFM rules of MarkDown, different columns are separated by \|, and the left and right boundaries of the table are marked with \|. First write a line of table header, then write a line of separator line replaced by a group of short lines, then write the content of the table.

## 文本格式控制 / Text Formatting
### 使用MarkDown语法的文本格式控制 / Text Formatting with MarkDown Syntax
KojoDown支持MarkDown中的文本格式控制，包括粗体、斜体、删除线等。
KojoDown supports text formatting controls in MarkDown, including bold, italic, strikethrough, etc.

使用\*\*表示粗体，使用\*表示斜体，使用\~\~表示删除线。**这些标记与文字之间不需要空格**。
Use \*\* for bold, \* for italic, and \~\~ for strikethrough. **No spaces are needed between the markers and the text**.

### 转义字符 / Escape Characters
使用\来转义特殊字符，如下表：
Use \ to escape special characters, as shown in the table above.
|显示字符|名称|书写方式|
|-------|------|-------|
| \\ |反斜杠 backslash| \ \ |
| \| |竖线 pipe| \\ \| |
| \` |反引号 backtick| \\ `|
| \* |星号 asterisk| \\ \*|
| \_ |下划线 underscore| \\ \_|
| \{ |左花括号 left brace| \\ \{|
| \} |右花括号 right brace| \\ \}|
| \# |井号 hash| \\ \#|
| \+ |加号 plus| \\ \+|
| \- |减号 minus| \\ \-|
| \. |英文句号 period| \\ \.|
| \! |感叹号 exclamation| \\ \!|

### 新增加的文本格式控制方式 / New Method of Text Formatting Control

## 引用 / Quotations
使用\>来表示引用，**后面紧跟一个空格**，然后是引用内容。
Use \> to indicate quotations, **followed by a space**, then the quotation content.

引用可以嵌套，即**在引用内容中再使用\>来表示更内层的引用**。
Quotations can be nested, that is, **use \> within the quotation content to indicate a deeper level of quotation**.

引用中也可以包含其他KojoDown格式的元素，如标题、列表等。
Quotations can also contain other KojoDown format elements, such as headings, lists, etc.

## 代码块 / Code Blocks
使用三个反引号（\`\`\`）来表示代码块，并注明程序语言名称，随后再书写代码。由于kojodown的代码块功能很少用于程序语言的代码书写，因此程序语言名称往往不做标记。
Use three backticks (\`\`\`) to indicate a code block, followed by the programming language name (which is often omitted), then the code.

如果在一段文本里需要插入代码，可以使用一对单个反引号（\`）来表示代码。
If you need to insert code within a text, use a single backtick (\`) to indicate the code.

## 选择支 / Choices
选择支的的写法类似于GFM的待办事项列表，与无序列表类似，使用“\- [ 跳转地址 ] 事项名称”的方式来表示。

## 跳转 / Links
使用 [ 链接地址 ] ( 显示文本 ) 来表示跳转。
Use [link address] (display text) to indicate a link.

## 分隔线 / Horizontal Rules
使用**三个或更多星号（\*）或减号（\-）来表示分隔线**。
Use **three or more asterisks (\*) or hyphens (\-) to indicate a horizontal rule**.

# 文件结构 / File Structure
在书写口上文件时，对于一些书写语法及其具体用途，有特殊的约定。
There are special conventions for some writing grammars and their specific uses when writing on the KojoDown file.

## 标题分级规则 / Heading Level Rules
在口上文件中，对各个标题层级的用途约定如下：
In the KojoDown file, the usage conventions for various heading levels are as follows:

- H1 用于文件结构 / File Structure
  > 文件结构标题主要包括标题、文件附注、文件(模块)导入几部分
  > File structure headings mainly include title, file notes, file (module) import, etc.
- H2 用于标志角色或地点 / Character or Place
  > 角色或地点等数据，往往是口上的主要单位
  > Data such as characters or places is often the main unit of the KojoDown file.
- H3 角色/地点口上中的结构 / File Structure in Charater or Place
  > 记录元数据（如作者、版本等，以及事件列表）、事件、内容文本、附注
  > Record metadata (such as author, version, etc., and event list), events, content text, and notes.
- H4 事件
  > 事件是口上中最重要的结构，事件是口上的核心，事件也是口上的基本单位。
  > Events are the most important structure in the KojoDown file. Events are the core of the KojoDown file, and events are also the basic units of the KojoDown file.
- H5 子事件
  > 凡从属于某一事件的子事件、分支事件等均使用H5
  > Any sub-events or branch events that belong to a certain event are all used with H5.