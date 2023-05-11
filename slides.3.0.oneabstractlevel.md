---
layout: center
---

# Rule 3 - One Level of Abstraction per Function
1. Do not mix different level of abstraction within a function
2. Led you to the next in the compelling order

<!--
1. 第一点不要混合多层级在一个方法中，我们在刚才的例子中已经一起介绍了。
2. 如果每个方法都能保证它只是完成子节点，子层级的工作，那从纵向上看，所有的方法就可以自然而然地实现一个自顶向下地阅读顺序，也是由浅入深地一种阅读顺序。
-->
---

To include the setups and teardowns, we include setups, then we include the test page content, and then we include the teardowns.
<br>
<br>
To include the setups, we include the suite setup if this is a suite, then we include the
regular setup.
<br>
<br>
To include the suite setup, we search the parent hierarchy for the “SuiteSetUp” page
and add an include statement with the path of that page.
<br>
<br>
To search the parent. . 

<!--

在方法实现了自顶向下的这种阅读顺序后，对应读者是非常友好的，读代码就像是在读一个小故事。当我们阅读这些代码时，甚至时不假思索的就可以理解这些代码的意图及所在做的事情。

打开fitness code 结构图 - 那我们在自定向下的逐一层级的阅读这些代码的时候， 就和阅读一段段 To 起头的段落是一样的轻松。 所及即所得，不需要我们自己在加工一遍。

打开书中原始样例代码 - 而回过头，看书中最开始的一版代码，这个过程首先是我们自己绞尽脑汁的先去猜测和理解代码所表达的内容，最后通过我们自己的加工整理后，才能的出来这样的段落内容.

-->

---

US TV Series: 
- https://frankie-talks-thinking.netlify.app/19
- https://frankie-talks-thinking.netlify.app/20

<!--

那这个自定向下的阅读顺序，也和我之前分享的结构化思考里的纵向思考是一样的， 这个纵向思考的过程就好比是一个看美剧的过程。

第一集抛出一个大的悬念，吸引着你往下看，每一集在揭开一层面纱之后再抛出它的悬念，直到最后才把所有谜底解开。

就跟现在比较火的悬疑剧，漫长的季节， 范伟和秦昊主演的，如果上来就告诉人全是沈墨杀的， 王阳是自杀，就很难吸引你一集集的看下去。
-->
