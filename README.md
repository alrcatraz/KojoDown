# KojoDown
 KojoDown，一款基于MarkDown的语法，用于编写ERA游戏口上
 A series of rules based on MarkDown, aiming at writing Kojo for ERA games

# 书写语法 / Rules
大部分的语法与MarkDown相同，但添加了部分新的规则，用以提供口上文件需要的功能，或根据口上制作的需要对既有功能进行强化。
Most of the rules are same as MarkDown, while there are some new rules added to provide features needed for Kojo files, or to enhance the existing features according to the needs of Kojo making.
## 标题层级 / Headings
使用\#来标志标题层级，一个\#代表一级标题，两个\#代表二级标题，以此类推，**最多到六级标题**。
Use \# to indicate the heading level, one \# represents level 1 heading, two \# represents level 2 heading, and so on, **up to level 6 heading**.

使用\#来设置标题时，后面**紧跟一个空格**，然后是标题内容。
When using \# to set the heading, there should be a **space immediately following** the \#, then the heading content.

## 列表 / Lists
无序列表使用\*、\+或\-来表示，**后面紧跟一个空格**，然后是列表项的内容。
Unordered lists are indicated by \*, \+ or \-, **followed by a space**, then the content of the list item.

有序列表使用数字和\.来表示，**后面紧跟一个空格**，然后是列表项的内容。
Ordered lists are indicated by numbers and \., **followed by a space**, then the content of the list item.

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
使用三个反引号（\`\`\`）来表示代码块，后面紧跟代码。
Use three backticks (\`\`\`) to indicate a code block, followed by the code.

## 链接 / Links
使用 [ 链接文本 ] ( 链接地址 ) 来表示链接。
Use [link text](link address) to indicate a link.

## 分隔线 / Horizontal Rules
使用**三个或更多星号（\*）、减号（\-）或下划线（\_）**来表示分隔线。
Use **three or more asterisks (\*), hyphens (\-) or underscores (\_)** to indicate a horizontal rule.



# 文件结构 / File Structure
