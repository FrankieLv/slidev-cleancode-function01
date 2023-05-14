---
layout: center
---

# Rule 1 - Small
1. It's transparently obvious and a story.
2. 2-4 lines
3. The indent level of a function should not be greater than one or two

<!--
1. 第一条规则就是短小，看着很好理解，那如何做到短小呢。
2. 这三点是书中的所表达的重点内容。
    - 1. 它就像是清晰地在讲一个小故事，这个小故事是给人看的，是给在座的我们看的。我们应该意识到代码不仅仅是能被机器正确运行就可以的， 代码写成什么样子，机器都可以运行，但是，我们还要考虑人与人之间的沟通。 如果代码可以清晰的讲述一个故事，就会让我们的沟通更加顺畅。
    - 2. 2-4 行代码，一个函数中越多的代码行，就会带来更多的阅读负担
-->
---

<img src="/images/Listing33.png" class="m-1 h-40 rounded shadow" />

- new method: includeSetupAndTeardownPages()
    - includeSetupPages()
    - newPageContent.append(pageData.getContent())
    - includeTeardownPages()

<!--
1. 基于短小的原则，作者对书中的重构后的代码，又进一步的重构了一次。
2. 作者在书中又对之前已经重构过的代码，又进一步地重构了一版。 将具体include setup和teardown的操作都封装到一个"includeSetupAndTeardownPage"方法中，最后这个方法只有4行代码，只有两层缩进。
3. 我认为这真的是一种极致地追求， 从我个人的角度并不是100%认同这种极致的追求，我当然认同方法应该短小，但是，物极必反，真的每一个方法都严格的短小到这种程度，一个类中的方法数量不会小了，反而也会增加阅读的负担。 个人想法而已，并不是在强制输出哈，实践中欢迎大家交换不同的想法。
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
1. 基于短小的原则， 我们应该从旁观者的角度去审视自己的代码发现，表达意图不清晰，代码行数过多，缩进层级过多的时候，那就应该这是不是坏代码的味道。
2. 样例中这些事伪代码，if while for 甚至try catch 每一个都是一个代码缩进块。
-->