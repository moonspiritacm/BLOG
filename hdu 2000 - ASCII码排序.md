# 地址

http://acm.hdu.edu.cn/showproblem.php?pid=2000

# 定位

 - 字典排序

 - 水题

# 分析

 - 直接使用 C++ 标准库中的 sort() 进行字典排序

# 代码

<div><div class="dp-highlighter bg_cpp"><div class="bar"><div class="tools"><b>[cpp]</b> <a href="#" class="ViewSource" title="view plain" onclick="dp.sh.Toolbar.Command('ViewSource',this);return false;" target="_self">view plain</a><span data-mod="popu_168"> <a href="#" class="CopyToClipboard" title="copy" onclick="dp.sh.Toolbar.Command('CopyToClipboard',this);return false;" target="_self">copy</a><div style="position: absolute; left: 710px; top: 539px; width: 15px; height: 16px; z-index: 99;"><embed id="ZeroClipboardMovie_1" src="https://csdnimg.cn/public/highlighter/ZeroClipboard.swf" loop="false" menu="false" quality="best" bgcolor="#ffffff" width="15" height="16" name="ZeroClipboardMovie_1" align="middle" allowscriptaccess="always" allowfullscreen="false" type="application/x-shockwave-flash" pluginspage="http://www.macromedia.com/go/getflashplayer" flashvars="id=1&amp;width=15&amp;height=16" wmode="transparent"></div></span><span data-mod="popu_169"> <a href="#" class="PrintSource" title="print" onclick="dp.sh.Toolbar.Command('PrintSource',this);return false;" target="_self">print</a></span><a href="#" class="About" title="?" onclick="dp.sh.Toolbar.Command('About',this);return false;" target="_self">?</a></div></div><ol start="1" class="dp-cpp"><li class="alt"><span><span class="preprocessor">#include&nbsp;&lt;iostream&gt;</span><span>&nbsp;&nbsp;</span></span></li><li class=""><span><span class="preprocessor">#include&nbsp;&lt;algorithm&gt;</span><span>&nbsp;&nbsp;</span></span></li><li class="alt"><span><span class="preprocessor">#include&nbsp;&lt;stdio.h&gt;</span><span>&nbsp;&nbsp;</span></span></li><li class=""><span><span class="preprocessor">#include&nbsp;&lt;string.h&gt;</span><span>&nbsp;&nbsp;</span></span></li><li class="alt"><span>&nbsp;&nbsp;</span></li><li class=""><span><span class="keyword">using</span><span>&nbsp;</span><span class="keyword">namespace</span><span>&nbsp;std;&nbsp;&nbsp;</span></span></li><li class="alt"><span>&nbsp;&nbsp;</span></li><li class=""><span><span class="datatypes">int</span><span>&nbsp;main()&nbsp;{&nbsp;&nbsp;</span></span></li><li class="alt"><span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="datatypes">char</span><span>&nbsp;ch[3];&nbsp;&nbsp;</span></span></li><li class=""><span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="keyword">while</span><span>(scanf(</span><span class="string">"%s"</span><span>,ch)!=EOF)&nbsp;{&nbsp;&nbsp;</span></span></li><li class="alt"><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;sort(ch,ch+3,less&lt;<span class="datatypes">char</span><span>&gt;());&nbsp;&nbsp;</span></span></li><li class=""><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;printf(<span class="string">"%c&nbsp;%c&nbsp;%c\n"</span><span>,ch[0],ch[1],ch[2]);&nbsp;&nbsp;</span></span></li><li class="alt"><span>&nbsp;&nbsp;&nbsp;&nbsp;}&nbsp;&nbsp;</span></li><li class=""><span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="keyword">return</span><span>&nbsp;0;&nbsp;&nbsp;</span></span></li><li class="alt"><span>}&nbsp;&nbsp;</span></li></ol></div></div>

# 性能

| Exe.Time | Exe.Memory | Code Length | Language |
|:-------------:|:-------------:|:-----:|:-----:|
| 0MS | 1868K | 286B | c++ |