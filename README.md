# KojoDown
 ***KojoDown，一款基于MarkDown的语法，用于编写ERA游戏口上***
 ***KojoDown, a series of rules based on MarkDown, aiming at writing Kojo for ERA games***

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

## 列表 / Lists
无序列表使用\*或\-来表示，**后面紧跟一个空格**，然后是列表项的内容。
Unordered lists are indicated by \* or \-, **followed by a space**, then the content of the list item.

有序列表使用数字和\.来表示，**后面紧跟一个空格**，然后是列表项的内容。
Ordered lists are indicated by numbers and \., **followed by a space**, then the content of the list item.

## 注释 / Comments
使用//来表示注释。注释符号仅作用于一行。

## 表格 / Tables
表格的书写方式和GFM规则的MarkDown相同，**不同栏之间用\|分隔，表格左右边界均标记\|。首先先写一行表头，然后写一行用一组短横代替内容的分隔行，然后写表格内容**。
The writing style of tables is the same as GFM rules of MarkDown, **different columns are separated by \|, and the left and right boundaries of the table are marked with \|. First write a line of table header, then write a line of separator line replaced by a group of short lines, then write the content of the table**.

## 文本格式控制 / Text Formatting
### 使用MarkDown语法的文本格式控制 / Text Formatting with MarkDown Syntax
KojoDown支持MarkDown中的文本格式控制，包括粗体、斜体、删除线等。
KojoDown supports text formatting controls in MarkDown, including bold, italic, strikethrough, etc.

使用\*\*表示粗体，使用\*表示斜体，使用\~\~表示删除线。**这些标记与文字之间不需要空格**。
Use \*\* for bold, \* for italic, and \~\~ for strikethrough. **No spaces are needed between the markers and the text**.

### 转义字符 / Escape Characters
**使用\来转义特殊字符**，如下表：
**Use \ to escape special characters**, as shown in the table above.
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
| & | 与符号 and mark| \\ &|

### 新增加的文本格式控制方式 / New Method of Text Formatting Control
新增加了一组文本格式控制方式如下表：
A new set of text formatting controls is added as shown in the table above:

|控制内容|书写方式|
|-------|-------|
|粗细 / weight|Weight( )|
|斜体 / italic|Italic( )|
|删除线 / strikethrough|Delete( )|
|颜色 / color|Color( )|
|字号 / size|Size( )|
|字体 / font|Font( )|
|恢复默认/restore default|Defatult|

字重可以用字重名称或数值表示，斜体和删除线的参数为是或否，颜色可使用颜色名或十六进制颜色值，字号可使用数值，字体使用字体族名称。
Weight can be represented by weight name or value, italic and strikethrough parameters are True or False, color can be represented by color name or hexadecimal color value, font size can be represented by value, and font can be represented by font family name.

除此之外，还有表示爱心、文字颤抖等的命令(函数)，具体列表会另行列出。
In addition, there are commands (functions) representing love, text trembling, etc. The specific list will be listed separately.

以上命令有两种使用方法：当在文本中使用时，使用行内代码块括住指令和应用指令的文本，指令和文本间用空格分隔；用于格式化大段或端文字时，用代码块包括文字，并在表示代码块开始的三个反引号后不换行使用这些指令风格化文本。
There are two ways to use these commands: when used in text, use inline code blocks to enclose the instructions and the text applying the instructions, separated by spaces between the instructions and the text; when used to format large or end text, use code blocks to include the text, and use these instruction styles after the three backticks indicating the start of the code block without a line break.

可以用**代码块嵌套**来完成大段文本中部分大段文本的再次风格化，这时内部代码块的文本会先继承外部代码块文本的格式，再添加新的格式。风格化的指令是**顺序执行**的，因此允许在代码块中嵌套使用代码块进行风格化时，先使用Default移除所有格式，然后重新设置新的格式。在大段格式化文本中使用markdown语法的加粗、斜体、删除线格式，会修改文本的格式，如已经加粗的文本再次加粗会取消加粗。如果要更改粗细而非移除加粗，可以使用行内代码块来重设字重。
**Code blocks can be nested** to style parts of the text in large blocks of text again. The styled instructions are **executed in sequence**, so it is allowed to nest code blocks for styling in code blocks, first use Default to remove all formats, and then set new formats. Using bold, italic, and strikethrough formats in markdown syntax in large formatted text will modify the text format. If the text is already bold and bolded again, it will be unbolded. If you want to change the boldness instead of removing the bold, you can use inline code blocks to reset the font weight.

## 引用 / Quotations
使用\>来表示引用，**后面紧跟一个空格**，然后是引用内容。
Use \> to indicate quotations, **followed by a space**, then the quotation content.

引用可以嵌套，即**在引用内容中再使用\>来表示更内层的引用**。
Quotations can be nested, that is, **use \> within the quotation content to indicate a deeper level of quotation**.

引用中也可以包含其他KojoDown格式的元素，如标题、列表等。
Quotations can also contain other KojoDown format elements, such as headings, lists, etc.

## 代码块 / Code Blocks
使用三个反引号（\`\`\`）来表示代码块，随后换行书写内部内容。原本MarkDown的代码块语法中，**反引号后不换行可以标注程序语言名称，KojoDown则根据口上文件的使用需要更改为了记录文本的格式化指令**。
Use three backticks (\`\`\`) to indicate a code block, followed by a line break and the internal content. In the original MarkDown code block syntax, **the language name can be annotated after the backtick without a line break. KojoDown changes this to record the formatting instructions for the text according to the needs of the Kojo file**.

如果在一段文本里需要插入代码，可以使用一对单个反引号（\`）来表示代码。
If you need to insert code within a text, use a single backtick (\`) to indicate the code.

## 选择支 / Choices
选择支的的写法类似于GFM的待办事项列表，与无序列表类似，使用“\- [->跳转地址] 事项名称”的方式来表示。

## 逻辑判断 / Logic
|判断符号|含义|
|---|---|
| ！ |非 not|
| /> |大于 bigger than|
| < |小于 smaller than|
| >= |大于等于 bigger/equal|
| <= |小于等于 smaller/equal|
| == |等于 equal|
| != |不等于 not equal|
| ? \| | 表达式?表达式为真执行\|表达式为假执行|

## 引用外部数值/函数 / External Values/Functions
**使用@引用外部数值/函数**。一般来说，引用外部数值函数的目的是输出文本，因此往往以{{@value}}或{{@function()}}的形式出现。
**Use the @ symbol to reference external values/functions**. In general, the purpose of referencing external values/functions is to output text, so it often appears in the form of {{@value}} or {{@function()}}.

## 锚点、跳转和链接 / Anchor, Jump and Links
所有跳转地址都使用被叫做锚点的标识符来表示。**在事件标题中，使用&anchor_name来表示锚点**。
All jump addresses are represented by identifiers called anchors. **In the event title, use &anchor_name to represent the anchor**.

使用 [逻辑判断？->链接地址|->链接地址] {{显示文本|显示文本}} 来表示跳转。第一个地址和文本是判断值为真时的跳转，第二个地址和文本是判断值为假时的跳转，当不需要判断为假的跳转时，|和后面的部分可以省略。
Use [logical judgment?->link address|->link address] {{display text|display text}} to indicate a jump. The first address and text are the jump when the logical judgment is true, and the second address and text are the jump when the logical judgment is false. When a false jump is not needed, | and the following part can be omitted.

使用 [URL]{{显示文本}} 来表示超链接。对于逻辑判断，也和上文对跳转的语法相同。
Use [URL] (display text) to create a hyperlink. For logical judgments, it is also the same as the syntax for jumps mentioned above.

## 插入内容
在口上文件中，时常遇到插入诸如角色对主角的称呼、角色自称、细微文本差分等内容。为实现这一功能，提供插入内容的语法。
In Kojo files, it is often encountered that the protagonist is addressed by the role, the role claims itself, and the subtle text difference. To achieve this function, the syntax for inserting content is provided.

**使用 {{内容}} 来表示插入的内容**。
**Use {{content}} to insert content**.

插入内容也支持简单的逻辑判断输出，此时的结构为{{逻辑判断? 文本1 | 文本2}}，当逻辑判断为真时，输出文本1，否则输出文本2。在不需要文本2时，|和后面的部分可以省略。
Inserted content also supports simple logical judgment output. At this time, the structure is {{logical judgment? text1 | text2}}, when the logical judgment is true, the text1 is output, otherwise the text2 is output. When text2 is not needed, | and the following part can be omitted.

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