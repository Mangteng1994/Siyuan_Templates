.action{/*获取文档的基本信息*/}
.action{$notebox :=" "}
.action{$docid:=.id}
.action{$getdocInfo := (queryBlocks "SELECT * FROM blocks WHERE id='?' and type='d' " $docid )}
.action{range $v:= $getdocInfo}
	.action{$notebox =$v.Box}	
.action{end}

.action{ $anchorSunday := "2022-12-25" }
.action{ $yearStartDate := now.Year | printf "%d-01-01" | toDate "2006-01-02" }
.action{ $ysDateDuration := div ($yearStartDate.Sub (toDate "2006-01-02" $anchorSunday)).Hours 24 }
.action{ $ysWeekDay := mod $ysDateDuration 7 }
.action{ $yearStartWeek := add (div (sub $ysDateDuration 1) 7) 1 }
.action{ if or (eq $ysWeekDay 0) (gt $ysWeekDay 4) }
    .action{ $yearStartWeek := add $yearStartWeek 1 }
.action{ end }

.action{ $nowWeek := add (div (div (now.Sub (toDate "2006-01-02" $anchorSunday)).Hours 24) 7) 1 }
.action{ $weeks := add (sub $nowWeek $yearStartWeek) 1 }

.action{$today:= (now | date "2006-01")}
.action{$weekResult:= (list $today "Week" $weeks| join " ")}



.action{ $nextYear := now.Year | add 1 }
.action{ $nextYearStart := $nextYear | printf "%d-01-01" | toDate "2006-01-02" }
.action{ $dayleft := (div (($nextYearStart).Sub now).Hours 24) }
.action{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}

{{{col
{{{row
🕐 创建时间：.action{now | date "2006-01-02 15:04"}
}}}
{{{row
距离 `.action{now.Year}-12-31` 还剩 `.action{$dayleft}` 天
}}}
{: style="color: var(--b3-card-info-color); background-color: var(--b3-card-info-background);"}
}}}


{{{row

快捷入口：<span data-type="a" data-href="siyuan://blocks/20250203032522-01guhtk">2025周计划周复盘</span>丨 <span data-type="a" data-href="siyuan://blocks/20250203133059-nswdojw">人生改善计划！</span> 丨<span data-type="a" data-href="siyuan://blocks/20250123143941-vws64xt">生活记录</span>
{: id="20250107095926-bdkh89u" style="text-align: center;"}

## <span data-type="text">🌱微习惯</span>{: style="background-color: var(--b3-card-success-background); color: var(--b3-card-success-color);"}
{: id="20250206113633-v7gj0r2"}

> 💡我们的生活很大程度上不是由某几个重大的决定左右的，而是由每一天那些细微而重复的行为来决定的。你想成为什么样的人，就努力按照对应的模式去生活。尽管你的生活方式离「想要的样子」可能还有一点距离，但你每天所做出的行为、习惯、判断，都是在推动着大脑，让大脑离它更近一步。
> {: id="20250206113633-a7tv7gr"}
>
> 所有期待养成的微习惯，见<span data-type="a" data-href="siyuan://blocks/20250203133059-nswdojw">人生改善计划！</span>
> {: id="20250206113633-h6hiq89"}
{: id="20250206113633-uoy1030"}

* {: id="20250206113633-s1qwbb4"}[ ] 早上7点10起床，不赖床，不躺在床上玩手机
  {: id="20250206113633-4rz1nzl"}
* {: id="20250206113633-nlsp2s7"}[ ] 白天努力做事，晚上适当充电
  {: id="20250206113633-ee2qnsg"}
* {: id="20250206113633-i80y8lj"}[ ] 晚上写日记
  {: id="20250206113633-vewcvzo"}
* {: id="20250206113633-g7rxhmt"}[ ] 晚上23点30前睡觉
  {: id="20250206113633-d0cc0e8"}
* {: id="20250206113633-3vuhm9k"}[ ] 控制信息摄取，可以先解决自己滴答清单收集箱的信息，而不要总是想着要摄取新的信息造成信息过载，导致过去的信息没处理，反而增加焦虑感
  {: id="20250206113633-2ie6nq6"}
  {: id="20250206113633-1rmbghr"}

## <span data-type="text">✅ Aim: 今天的打怪目标</span>{: style="background-color: var(--b3-font-background1); color: var(--b3-font-color1);"}
{: id="20250206113633-dm4j5k9"}

> 💡每日行动清单应基于<span data-type="strong">核心任务笔记</span>制定。传统从杂事、资讯和想法直接建立行动清单的方式，易导致清单混乱、缺乏重点、难以执行。防弹笔记法主张先完成核心任务笔记的拆解与复盘修正，提取关键下一步行动，再纳入每日待办清单，确保每日行动目标明确，与核心任务紧密相连。
> {: id="20250206113633-fjk0ba0"}
>
> 模板
> {: id="20250206113633-onwsrxq"}
>
> * {: id="20250206113633-vwxnk7k"}[ ] 核心任务1
>   {: id="20250206113633-wizelsp"}
>
>   * {: id="20250206113633-s9rg99e"}[ ] 子任务
>     {: id="20250206113633-9hqaxql"}
>     {: id="20250206113633-vaitvbw"}
> * {: id="20250206113633-799gfmv"}[ ] 核心任务2
>   {: id="20250206113633-78xvavp"}
>
>   * {: id="20250206113633-uqo181g"}[ ] 子任务
>     {: id="20250206113633-2zunnv1"}
>     {: id="20250206113633-p4yuz4z"}
>     {: id="20250206113633-c92h1uz"}
      {: id="20250206113633-d5i9wiy"}

* {: id="20250206113633-33cl1c3"}[ ] 
  {: id="20250206113633-2984e31"}
  {: id="20250206113633-rutwkbt"}

## <span data-type="text">🕰 时间线</span>{: style="color: var(--b3-font-color5); background-color: var(--b3-font-background5);"}
{: id="20250206113633-n0ymobs"}

> * {: id="20250206113700-qu4mih4"}7:10 起床
>   {: id="20250206113700-9ufjfxo"}
> * {: id="20250206113711-sqx1mkf"}8:25 到工位
>   {: id="20250206113711-b832kvt"}
>   {: id="20250206113657-76iio6w"}
    {: id="20250206113655-7hxzgqj"}

* {: id="20250206113633-psrn6u1"}
  {: id="20250206113633-4gaxyvu"}
  {: id="20250206113633-gjr05tk"}

## <span data-type="text">⚡️今天我做了什么，打了哪些怪</span>{: style="background-color: var(--b3-font-background12); color: var(--b3-font-color12);"}
{: id="20250206113633-w2a573o"}

### 💼工作进展
{: id="20250206113633-4z0at3f"}

* {: id="20250206113633-mxf8bh0"}工作琐事
  {: id="20250206113633-m63v45v"}
  {: id="20250206113633-ucmq994"}

### 📚专业知识精进
{: id="20250206113633-arlp3eh"}

* {: id="20250206113633-4rizeje"}<span data-type="block-ref" data-subtype="s" data-id="20240819134821-1unpzm4">@路线设计</span>
  {: id="20250206113633-seuckbb"}
* {: id="20250206113633-uk37y4m"}<span data-type="block-ref" data-subtype="s" data-id="20240819124207-7gaaokg">@人工智能</span>
  {: id="20250206113633-ty26400"}
* {: id="20250206150815-nd1h4oc"}<span data-type="block-ref" data-subtype="s" data-id="20240819134951-0gjjtwg">@编程学习</span>
  {: id="20250206150815-wv8w2xb"}
  {: id="20250206113633-0h7r350"}

### 🔋兴趣学习充电
{: id="20250206113633-gsx6656"}

* {: id="20250206113633-509tj4f"}<span data-type="block-ref" data-subtype="s" data-id="20240819134901-mi6jsfn">@经济</span>
  {: id="20250206113633-pulbo4o"}

### 🪺个人生活记录
{: id="20250206113633-4yq7vz3"}

* {: id="20250206113633-7ywic9g"}<span data-type="block-ref" data-subtype="s" data-id="20250203132448-4rfidii">@小确幸</span>
  {: id="20250206113633-yw9nob8"}
  
* {: id="20250206113633-ys5zj4m"}<span data-type="block-ref" data-subtype="s" data-id="20250203133436-hksi0zq">@碎碎念</span>
  {: id="20250206113633-wcnv3wl"}
  
* {: id="20250206113633-zk0tvo7"}健身记录
  {: id="20250206113633-8r6x97u"}
  
  {: id="20250206113633-lokwqr8"}

## <span data-type="text">🤔 Reflection: 打怪经验总结与反思</span>{: style="background-color: var(--b3-font-background8); color: var(--b3-font-color8);"}
{: id="20250206113633-a3g8emf"}

### 🐛今日进展与存在问题
{: id="20250206115026-nnuaaph"}

> 💡高端玩家会在一次次游戏中变得更强！
> {: id="20250206113633-u3la7wc"}
{: id="20250206113633-eqt6yy5"}

{: id="20250206115027-i6gd4nc"}

### ✨明日改变计划
{: id="20250206113633-lmqwrsc"}

> 💡作家海明威在写作时有一个习惯，在完成自己一天的工作，趁着自己已经想到新的悬念、明确后续故事走向的时候，就会停下来，留到明天写，他没有选择一天就把自己的精力和灵感在一天耗尽，而是选择把动力延续到下一次写作。这样好处是，<span data-type="strong">每次结束都对下一个阶段要做什么胸有成竹</span>，对新的一天、新的一周是感到兴奋期待，而不是焦虑，这是一种可持续努力的工作方法，提高效率的同时，还有利于激发新的想法和创造性的解决方案。所以及时停下来，做明天计划，或许比埋头苦干地结束一天更有效。
> {: id="20250206114908-ig6m7yn"}
{: id="20250206114905-tjozgib"}

* {: id="20250206113633-s36psi1"}
  {: id="20250206113633-fg2ppzz"}
  {: id="20250206113633-yggnecr"}

{: id="20250206113633-iz06llr"}



.action{/* 获取今天日期和星期 */}
.action{$today := now | date "2006-01-02" }
.action{$weekday := now | date "Mon" }
.action{/* 工作日用红色图标，周末用蓝色图标，%23代表#号，URL不能直接输入#号，所以用URL编码%23代替 */}
.action{$color := "%23d13d51"}
.action{if or (eq $weekday "Sat")  (eq $weekday "Sun") }
.action{$color = "%233eb0ea"}
.action{end} 
.action{/* 设置文档图标：选择type6，仅返回星期样式 */}

{: icon="api/icon/getDynamicIcon?type=6&date=.action{$today}&color=.action{$color}"   type="doc"}
