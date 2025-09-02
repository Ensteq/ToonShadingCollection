# Toon Shading Collection 

## CH01 - Overview of stylelized Art

![CH01_01_卡通渲染分类](../imgs/CH01_01_ToonShadingStyles.jpg)

Toon-shading is a type of stylelized rendering (or non-photorealistic rendering (NPR)), which favours artistic expression by emulating hand drawn art. It's counterpart is PBR (physically based rendering) which attempts to simulate (or approximate) Light in the real world.

Lets begin by categorizing different styles:

 <br>

------

 **Western cartoons：**

![CH01_02_美式卡通示例](../imgs/CH01_02_WesternStyle.jpg)

Example: "Team Fortress 2"

Shading:

- The light and shadow shapes prefer soft edges and gradients.
- Highlights and Shadows are often exaggerated.
- The style is heavily dependent on artist authored colors.
TN: Soft edge = gradient. Hard edge = clear cutoff between shapes of color.

Modelling:

- The characters proportions are highly exaggerated.
TN: The western tradition grew cartoon in part out of (political) carricature and generally favours extreme expressions over conventionally attractive characters. Or in other words, maximize expression not maximize appeal.

<br>

------

**Anime (Easter cartoon):**

![CH01_03_日式卡通示例](../imgs/CH01_03_EasternStyle.jpg)

Example: "Honkai Impact 3rd"

Shading:

- Favours large shapes of solid color (celshading)
- Little to no gradiations between tones. All edges are hard.

Modeling:

- Proportions are more realistic than western Styles. 

 <br>

 <br>

------

### Discussing the Implementation for stylelized rendering

 <br>

> As CGI technology develops, computer animation techniques are increasingly being applied to games and 3D animations. However, there are still many awkward inconsistencies in the visual presentation. This is due to the technical focus of (graphics) engineers, who often lack the knowledge and experience to understand what artists actually want to express. Instead, they focus on the technical implementation of the effects. As a result, while game visuals contain all the necessary elements, they fail to achieve the desired emotional impact.
>
> To achive good results, graphics engineers need a solid understanding of Art in Manga and Anime. However, knowledge in Anime is more immediately useful than Manga. With this in mind, we can look at different examples to understand how they create their appeal and then use computer graphics technologies to recreate them. This is in contrast to simply implementing surface level features while failing to capture the essence.
>
> Wheter it's Mangaka, a masterful artist or animation company, generally they all have strong styles which Fans immediately recognize, unlike the cookie-cutter cartoon rendering commonly present in recent games. at current date, there is a lot of room for improvement with many underdeveloped visual effects for anime style rendering.
>> TN: I am using Manga/mangaka and Anime over the more general terms of Comic and Animation as the text discusses the eastern comic tradition.
>
> If you are working in the animation or games industry as an artist, consider how you express emotion through animation. How can 3D rendering produce the lines of the mouth? How to use lighting to create a strong Atmosphere? Does a retro color scheme with celshading still look appealing? Have you considered this approach during production?
> 
> ![CH01_06_AnimeReference](../imgs/CH01_06_AnimeReference.jpg)
>
> While there are only a few important techniques to know, it's crucial to use them well in order to recreate the original art and capture the appropriate atmosphere.
>
> As photorealistic rendering technology develops and becomes more established, non-photorealistic rendering (NPR) also gains more attention. One of the most important styles is celshading. This style requires a comprehensive understanding of traditional cel animation as well as 3D technology. Pure technical expertise cannot produce a high quality cel shading effect.
>
> To achieve the highest quality possible it's not only important to master traditional art techniques, but also have experience with concept art, in-between drawings (or at least understanding the underlying principles) and a sense for composition and layout, but also able to utilize 3D rendering techniques to recreate the style faithfully while streamlining the workflow. Maintaining visual consistency using computer graphics is challenging.
>
> In chinese and international forums, some core fans are averse to photorealistic artstyles and don't want a japanese pixar. This sentiment stems from the fact, that achieving cel-shaded effects with 3D technology remains challenging.
>
> An example where the artdirection collapsed can be seen in the 3D adaptation of "Berserk".
>
> Compare this to "Land of the Lustrous" which managed to capture the handdrawn appeal of traditional cel animation much more faithfully. 
>
> I think there is still a lot of room for improvement for cel shading in games. For example: 
>
> I would create a more retro style rendering for a hypothetical "Saint Seiya" game.
>
> Interestingly, this retro style has gradually become a popular subculture trend. For example, Vaporwave videos often play clips from Sailor Moon or Neon Genesis Evangelion combined with Lofi-Hiphop music, creating a strong cyberpunk feel. Classic works of art remain timeless for hundreds of years; after all, anime itself has only existed for several decades.
>
> One netizen commented: "CGI technology isn't necessarily good or bad; it's how the production company uses it that determines whether it's good or bad." What's your opinion?

 <br>

------

### Discussing Trends in Art-Styles

 <br>

> Productions for Animation work with a different methodology from Games. Animation often works with specific camera angles and manually adjusts the images to maximize the appeal and fix errors, where Games favour consistency accross different environments and viewing angles.
>
> Handdrawn characters are often not consistent 3D objects. In order to recreate the appeal this inherent "brokenness" needs to be intentionally reintroduced. In the meantime, PBR remains one of the major trends. 
>
> Since Arc System Works shared it's toon rendering approach for Guilty Gear on GDC 2015, toon shading has developed very rapidly. There are productions attempting to recreate cel-shaded animation such as Guilty Gear or Uma Musume, stylelized PBR productions like Infinity Nikki or 鹿鸣(TN: Lumi? seems to be a CN only thing). There are also productions leaning more towards PBR like Granblue Fantasy, Blue Protocol and other explorations like Tales of Arise.
>
> ![CH01_07_GameArtStyles](../imgs/CH01_07_GameArtStyles.png)
> (TL-BR 鹿鸣, GFL2: Excillium, Infinity Nikki, Granblue Fantasy Versus, ?, Guilty Gear Xrd, Tales of Arise, Scarlet Nexus, Genshin Impact, TLoZ: Breath of the wild/tears of the kingdom, uma musume.)
> 
> The ability to create distinct styles with 3D rendering is becoming stronger. For Toonshading, unlike PBR, there are no standards to compare to in order to judge it's quality. Toonshading heavily relies on modeling and texturing, as such artdirection is particularly important.
>
> Additionally, toonshading combines the artists aesthetic preferences with an abstraction of the real world. Different artists have approaches to their art, resulting in a large variety in rendering styles. Even so, they still share some common elements. Let us take a closer look at what efforts gamedevelopers took to create high quality anime style visuals. 
>
> ![CH01_08_BasicToonShadingFeatures](../imgs/CH01_08_BasicToonShadingFeatures.png)
>
> Lets first list the basic concepts. There are two common names for toonshading. Celshading as an abbrevation of Celulloid Shading and Toon from Cartoon Shading. The most basic type of Toonshading only needs outlines, hightlights and flat shapes for light and shadow. 
>
> However, as mentioned before, strictly following this approach isn't necessarily required to create a stylelized/anime feel as styles in handdrawn art have also diversified. It's important to apply the underlying principles to create the desired appeal.
>
> <br>
>
> When the artists are creating their work, they place their reference images on a scale from stylelized to realistic, to determine how much they lean towards one or the other.
>
> Although there are many tricks in toon rendering, they are used to restore the unique effects of the original illustration. 
>
> ![CH01_09_ArtStyleAxis](../imgs/CH01_09_ArtStyleAxis.png)
>
> There are four elements universal to all variations of anime style art, regardless if they lean towards realistic or stylelized.
>
> ![CH01_10_CommonToonShadingFeatures](../imgs/CH01_10_CommonToonShadingFeatures.png)
>
> First is to reduce the number of unique colors. The fewer colors there are, the more carton-y the appeal.
>
> Secondly the separation of light and dark tones. Usually warm lights are paired with cold darks. By creating a strong contrast between these a more stylelized look can be achieved while also creating a stronger sense of light and dark.
>
> Thirdly, controlling shadows. In Manga, the neck of a character is often cast in shadow, even if it should be lit by placement of the lightsource. This is done to achieve an attractive aesthetic, even if it is at odds with the actual 3d form. To recreate this, we need manual control over shadows.
>
> Lastly, lineart is important for the appeal of anime style rendering. 

There are several directions that cartoon rendering can continue to advance in the future (personal opinion of a Goose Factory boss): TN: I really do not know how to properly translate "某鹅厂大佬个人观点" so have the literal meaning.
>
> For one, lean into cel shaded anime style. Ignore the 3D structure and exaggerate the mesh deformations in order to recreate the 2D appeal.
>
> Secondly, combinations of toon-shading and PBR in order to better define different materials are also worth exploring. Here approaches vary with no unified solutions dominating yet. However, because of this lack of uniformity this approach has the greatest potential in the future.
>
> Lastly, applying post production effects from anime to game rendering pipelines. This approach would be something of a cross industry collaboration, by applying knowledge and experience from one field to another. 

 <br>

------

### 画风选择探讨

全文照抄大佬警世恒言，作为参考：

> ![CH01_04_ToonShadingDeath](../imgs/CH01_04_ToonShadingDeath.jpg)
>
>  之所以提出“赛璐璐已死”这样的暴论，当然不是“赛璐璐”这个风格有什么问题，而是因为单纯的赛璐璐风格在即时渲染方面已经到了一个再难提升表现力的程度，接下来要解决的每个问题都比较困难而且收效甚微。
>
> 在有米哈游这家财大气粗的公司存在的现况下，要在画面方面对它的产品产生竞争力，相同水平是不行的，还需要有比较大的视觉上的提升。而赛璐璐风格剩下的所有提升空间可能都不足以拉开足够的差距，这还是建立在对方止步不前的前提下。
>
> 所以对于所有米哈游的竞争厂商来讲，单纯的赛璐璐确实已经死了。严格的说，即使是原神，其实也已经不是纯粹的赛璐璐了。这也证明死守赛璐璐路线基本死路一条。
>
> <br>
>
>   #### **生路何在？**
>
> NPR本身是一个巨大的体系，断然不是只有一种风格可供选择。
>
> 但是作为一部商业作品，风格选择自然不能根据个人喜好，而应该考虑广泛接受度。那么实际就需要遵循下述标准：
>
> - 这种风格应该被市场证实确实具有竞争力。不仅仅要有成功作品，还必须有大量成功作品。单一成功作品很可能仅仅是不可复制的偶然结果，也可能成功要素并不包括画面。另外，成功的趋势还要延续到现在。如果一种风格以前大量存在，现在不复存在，则很可能是因为它已经被市场竞争所淘汰，反而属于绝对不能进行的选择。
>
> - 即使是有市场竞争力的风格，也还要考虑这个风格和载体的兼容程度。如果你做的是一个自由视角的3D游戏，这个画风就必须在所有可能的视角下都能够做到美观，而许多基于2D/静态的画风其实是做不到这点的。此外，也存在一些只能表现人物，甚至只能表现少量人物的画风，使用这样的风格就只能做做简单场景和低人物数量的箱庭解密或者换装游戏什么的，无法用来塑造一个正常的，有大量NPC和风貌的完整世界。为了满足这些要求，除了从已有游戏取材外，最合适的临近载体是**影视**。静态画册的美术风格许多都不太符合这个要求，或者不确定是否可以符合要求。
>
>   <br>
>
> 大体上，可以将现有美术风格分为基于PBR技术手段的，代表者为迪斯尼动画的3D体系，以及基于用3D模拟2D手绘风格的三渲二体系。
>
> （当然，还有纯写实，这是非常有价值的分类，但不在此次讨论范围内。写实的问题是“卷”。）
>
> 迪斯尼的动画风格，由于作品一直都保持着合家欢的低龄特征，不太适合成人向作品。但其技术手段其实是可以应用于成人向作品的，典型的例子便是守望先锋，所以除了作品数量偏低外倒没什么问题。
>
> 它的问题其实在于：它的绝大部分作品都是针对欧美的，亚洲较少使用这种风格的作品，因此创造符合亚洲人审美的作品的时候，参考就极少。最终幻想本来属于这个路线，但显然，他们自己都已经陷入了迷茫的死局之中，恰恰让人们对这个方向缺乏信心。
>
> 中国自己探索的结果在我看也是基本失败的。就一句话：一个npr风格的作品，如果改成写实效果会更好，它就应该直接做成写实的，那它自身就失去了意义。国产许多游戏其实都更适合仿照电视剧风格做成纯写实的，一半写实一半不写实终究只是妥协后的中间阶段。
>
> 当然，欧美风格亚洲人也是可以接受的，比如某大圣哪吒，况且如果全球发行这也不算劣势。但始终还是存在水土不服的问题，可参考的成人化作品不多也算是个缺点。
>
>   <br>
>
> 而另一个所谓的三渲二方向，大体来讲，基本就已经可以说成是日本卡通风格了。
>
> 当然，2D动画并不是只有这样一个风格。就算不提欧美2D动画，一些类似简笔画的风格化作品也常常出现在游戏中。但问题是，那些并非主流，只进行少量传播的个人画风，我们很难确定它是否有着足够的广泛接受度，而更关键的是，它们往往缺乏影视方面的参考物。
>
> 日式卡通风格在市场上经过了长时间的迭代，旧世代画风和现世代有着很大的“品质”上的区别，这种迭代的成果很难被认为是没有竞争力的。更关键的是，它的主要载体漫画和动画，都可以作为良好的游戏化参考，目前也有不少游戏化的例子可供参考。
>
> 日式卡通风格有着它独立的受众群，在其受众中自然是极好的。可问题是，即使你不打算针对这部分受众，考虑到参考物的多寡导致的创作难度，选择其他风格未必是优解。即使这个风格并不是为他们设计的，只要确实做的好，也不会觉得难看。而即使你针对用户选择画面风格，由于参考少，做出效果很难，未必能讨得欢心。
>
> 总之，即使是针对非受众，日式卡通风格也都有它独有的优势。因此，对于受众，那还有什么可讨论的余地
>
> <br>
>
> #### **“借物”的重要性**
>
> 我上面这样强调“大量参考”这个概念，多半会让一些人觉得不适。他们可能会觉得：
>
> 做没做过的事，虽然难，但那不是理所当然应该做的事吗？
>
> 甚至高喊：**“抄袭”是不道德的！**
>
> 那我可得说：这个游戏界“不道德”的事或许远比你想到的要更多。
>
>    <br>
>
> 最近流行的PBR，“基于物理真实的渲染，”它的优势是什么？
>
> 是**产能**。同样的量和质，PBR的成本远低于原始方案，而且创作速度也更快。因此，在同样的成本和限定的工期下，可以做到更高的数量和质量。
>
> 为什么成本低，速度快？
>
> 因为可以直接从现实中取材，而不需要靠人脑去创造。
>
> 刺客信条复原历史建筑，复原真实地形风貌，你认为它成本增加了吗？
>
> 从绝对值上，确实可能增加了。
>
> 但是假如对比物是：完全不参考现实，从零开始重新创作出和现在产品相同质量的成果。那成本毫无疑问是降低了，而且降低的不是一点半点。
>
>   <br>
>
> 所以说，PBR而能够降低成本，增加产能的根本原因，通俗来讲，其实就是**抄袭现实**。
>
> “抄”这个词是避不开的。不通过“抄”，你就只能无限堆叠人力进行推量。而一个游戏实际成本其实基本是固定的，工期也没得商量，所以并不存在这个方法。
>
> 你在固定成本下还想进行高质量的创作，其实只有两个方法：
>
> 1. 天降猛男。指望招募到几个实际价值能够以一顶百的高水平的创作者，然后只用三千块钱就帮你干活。这样你就能省下钱和时间来，去生产更多的内容。
>2. 抄。
> 
>   <br>
>
> NPR领域自然无法“抄袭”现实，而最接近的代替方案，就是找已有的成体系的作品来代替现实锚点。所以，你选择的方向，可“抄”的内容数量越多，质量越高，你同样条件下创作出的内容就会越好。
>
> 这还没有考虑人才市场的问题。
>
> 这里再强调一次，并不是说日式卡通比其他风格要好，也很可能并不符合你的目标受众的喜好。确实可能有很多人喜欢那些半写实半卡通的奇怪玩意儿，也可能它确实才是你的受众“审美”的终点。
>
> 可问题是，如果你真的要做那些，世界上基本就没出现过的全新的“先端”风格。你怎么证明自己做的是对的？即使你能够做到正确的判断，具体实现中所需要付出的探索成本，也会计入到你的总成本内，最终拖累产出，影响质量。质量如果低了，甚至干脆做不出来，就算方向正确又能如何？
>
> 而且，日式卡通还有个非常重要的优势：它本身就有大量现成的影视作品可供参考，而影视是最容易转移到游戏里来的形式。PBR之所以能够大幅降低成本，也和它无脑沿用影视行业的现成成果有非常大的关系。
>
> 这方面能够和日式卡通相比的也就迪士尼3D动画了。
>
> 其他没有影视作品背书的作品，首先就要解决“影视化”问题，需要将这个探索过程重新走一遍。而游戏化其实还需要解决实时渲染的问题。这些问题，没有一个是容易完成的，甚至，有可能是无法完成的。
>
>   <br>
>
> #### **赛璐璐，死不掉**
>
> 所以我上面说那么多是为了证实选择“日式卡通”这个方向的合理性吗？
>
> 不，如果你已经选择了要做这方面的产品，这本来就是一个不需要讨论的问题。
>
> 我要表达的是，如果按上面的逻辑，考虑到参考物的多寡，考虑到影视化，乃至游戏化的程度。
>
> **你好像只能做赛璐璐。**
>
> 毕竟动画都是赛璐璐的啊。不做赛璐璐，说不定还不如选择所谓的国产3D呢，起码有过影视作品。
>
>   <br>
>
> 然后你说，干嘛纠结影视呢？直接一步到位到游戏不好吗？不也有好多没有对应风格的影视作品，效果也还不错的游戏出现了吗？
>
> 然后你回想下，这些游戏里，是不是有很多都是固定视角或者俯视角的游戏，而且人物距离摄像机的距离都特远。
>
> 它们存在自由视角，电影式过场吗？
>
> 里面有人类吗？有不同年龄层的人吗？有不同性别的人吗？
>
> 有室外吗？有白天吗？有正常的场景吗？
>
> 而你要做的游戏是否需要这样的东西？
>
>   <br>
>
> 当然，认真想一下的话，其实还是有的。但这些作品的画风，也完全可以做出一部合格的动画了。他们确实凭借自己的能力，独自完成了画风的影视化和游戏化，是值得尊敬的。
>
> 但是你打算抄那个画风吗？（是否觉得能达到你的要求？）
>
> 不想抄的话，你能自己做到吗？
>
>  <br>
>
> #### **猎魔人选择**
>
> 但是赛璐璐又不行。
>
> 也就是说，现在我们面前的是一个双坏选择。你需要在里面随便选一个。
>
> 要不就选择赛璐璐赛道，和米哈游和将来必定会出现的100个幻塔竞争。为了生存，你需要拥有足够的实力。有实力，一切都不是问题。
>
> 无非，就是退回写实的“终极卷”状态罢了。那么多公司，不一样活下来了。决定游戏的又不光是画风。画风和别人一样，靠其他方面进行竞争不就好了。
>
> 当前，前提是，你得有实力，还要有其他可竞争的方面。通常你是没有的。
>
>   <br>
>
> 而另一个选择就是去探索新的风格。毕竟赛璐璐的缺陷是同质化，只要做到“不完全相似”就好了。只是做少量的改动，其附加探索成本还在可控范围内。
>
> 也就是说，不重新去游戏化“厚涂”风格，而只是选择一些比较接近赛璐璐的插画画风作为参考，并对先有的赛璐璐风格做出改进，就和日本动画这些年来通过CG技术不断在进行的改进类似。
>
> 这在我看是相对比较“风险均衡”的方案。
>
>   <br>
>
> 然而，这样做的实际结果很可能只是从4到5的转变。
>
> ![CH01_05_ArtStyleComparism](../imgs/CH01_05_ArtStyleComparism.jpg)
>
> 其实除此之外还是可以做出不少改变的。但是改变越多，探索成本越高。
>
> 动画现在的很多技法也可以搬运到游戏里来，但这个大家都在做，你本来就也要跟着做，这依然还是在赛璐璐里卷。
>
> 我只能说，卷就卷吧。
>
> 赛璐璐死不死得了另说，模拟“剧场动画”这条路大家都在走的路，你恐怕还真的跑不掉。









