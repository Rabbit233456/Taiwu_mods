这个mod对游戏的影响只有两处：一是添加了一门神一品内功；二是在时节变化时根据这门内功的状态和mod界面的相关设置进行操作
只有在切换时节的时候代码才会运转，理论上玩家的任何操作(传剑、入魔等)都不会导致bug，因为mod只对结束当前时节时的状态做相应的反馈
增加的内功可以看作沛然决全面强化版，除了没有对应的书之外和普通功法没区别

未习得[天长地久不老长春功]时结束当前时节，若满足以下条件，会习得相应进度的功法
	1.总内力达到500，且内功造诣100：获得[天长地久不老长春功]，初始修习进度+50%，研读进度+0
	2.沛然决大成：获得[天长地久不老长春功]，初始修习进度+0%，研读进度+1
两个条件的奖励是可叠加的

已习得[天长地久不老长春功]时结束当前时节，若年龄大于等于设置中的触发年龄，则触发返老还童

根据功法修习进度，可以调整返老还童的触发年龄：
	0%~24%，不会触发返老还童
	25%~49%，可选不触发、≥36岁
	50%~74%，可选不触发、≥36岁、≥66岁
	75%~100%，可选不触发、≥36岁、≥66岁、≥96岁
这里选择36岁不是指等于36才会触发，而是大于等于36岁都会触发，其他选项同理
若当前年龄大于可选的最大年龄时选择不触发，则每时节修习进度-1%，直到降至24%
	例：35%修习进度时选择不触发，则从37岁开始每时节修习进度-1%，直到降至24%
100%修习进度时不受上一条的影响

触发返老还童后的年龄，其可调整范围为6~[6+研读进度]

正逆练特效同沛然决，可调整下一次返老还童后的正逆练比例

所有设置项都依赖于当前的状态，面板上显示多少就是多少，而不是“应该”有多少，那是返老还童之后才会有的不是立刻就有的

触发返老还童时，根据功法修习进度，角色属性会有所增长：
	六维判定6次，技艺资质判定16次，武学资质判定14次，随机选取判定条目，判定成功率等于修习进度，判定成功则该项+1

触发返老还童后，修习进度归零

触发返老还童时，根据内功造诣计算研读进度：
	除去不老长春功增加的造诣后，造诣10/30/60/100/150/210/280/360/450对应研读进度1~9，沛然决大成额外+1
	研读进度只会在返老还童时计算，游戏过程中造诣增长不会导致研读进度变化
	研读进度增加时，增量会加到正练进度上

每次需要30枚血露，不足的话按照突破内功走火入魔对应步数的0.04倍增加内伤和内息紊乱
会优先使用低品血露

触发返老还童或修习进度下降时，'天长地久不老长春功'会自动卸载，注意检查功法装载状态
存档中只写入了功法修习进度和研读进度数据，mod设置没有保存到存档内，在多个存档之间切换时请注意检查mod设置

使用了功法id150369，如果和其他添加功法的mod冲突纯属意外，请回帖报告冲突情况以便及时修正
id冲突不会导致坏档，只会出现功法数据互相覆盖的情况，请放心使用

卸载MOD：在设置页面中关闭MOD后，会出现相应提示，在结束当前时节后清除存档中所有mod写入的内容，之后移除mod即可
ps：虽然做了对应的处理，但没有实际测试npc学会这个内功时(通过偷学、请教等)是否能正确移除 没有村民来请教我这个功法orz ，因此移除mod前请备份存档以避免坏档

http://bbs.nga.cn/read.php?&tid=15547796