---
layout: center
---

# Rule 1 - Small
1. It's transparently obvious and a story.
2. 2-4 lines
3. The indent level of a function should not be greater than one or two

<!--
1. 短小这个原则，已经存在了几十年了，SOLID当中的第一个单一职责原则，也是在强调，一个函数只应该做一件事情。
2. 如何做到短小，这三点是书中的所表达的重点内容。
-->
---

<img src="/images/Listing33.PNG" class="m-1 h-40 rounded shadow" />

- new method: includeSetupAndTeardownPage()

<!--
1. 作者在书中又对之前已经重构过的代码，又进一步地重构了一版。 将具体include setup和teardown的操作都封装到一个"includeSetupAndTeardownPage"方法中，最后这个方法只有4行代码，只有两层缩进。
2. 我认为这真的是一种极致地追求， 从我个人的角度并不是100%认同这种极致的追求，我当然认同方法应该短小，但是，物极必反，真的每一个方法都严格的短小到这种程度，一个类中的方法数量不会小了，反而也会增加阅读的负担。 个人想法而已，并不是在强制输出哈，实践中欢迎大家交换不同的想法。
-->

---

# Bad Code Smell

```ts
 public void method() {
    if(condition1){
        while(true){
            if(condition2){
                try{
                    ***
                    ***
                }catch(){

                }
                
            }
        }
    }
    ***
    ***
    ***
    ***
    ***
    ***
 }


```
<!--
1. 基于短小的原则， 当我们审视自己的代码发现，表达意图不清晰，代码行数过多，缩进层级过多的时候，那就应该这是不是坏代码的味道。
2. 样例中这些事伪代码，if while for 甚至try catch 每一个都是一个代码缩进块。
-->