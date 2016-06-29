---
layout: none
kramdown:
  input: GFM
---
# Header 1 {#anchor-1}

{{ site.time }} {{ site.highlighter }} {{ site.url }}

kramdown
: A Markdown-superset converter

definition term 1
definition term 2
: This is the first line. Since the first non-space characters appears in
column 3, all other lines have to be indented 2 spaces (or lazy syntax may
  be used after an indented line). This tells kramdown that the lines
  belong to the definition.
:       This is the another definition for the same term. It uses a
        different number of spaces for indentation which is okay but
        should generally be avoided.
   : The definition marker is indented 3 spaces which is allowed but
     should also be avoided.

<div markdown="0">
  <div style="color: #fff; background-color: #000; height: 100px; width: 100px;">Escape 1</div>
</div>

<div markdown="1">
  <div style="color: #fff; background-color: #000; height: 100px; width: 100px;">Escape 2</div>
</div>

<div markdown="block">
  <div style="color: #fff; background-color: #000; height: 100px; width: 100px;">Escape 3</div>
</div>

```cpp
#include <cstdio>
#include <algorithm>
#include "header.h"

using namespace std;

namespace lib {
class math {
  int a, b;
  const int n = 100;
  math() : a(0), b(0) {}
};
} // namespace lib

int main() {
  /* Comment */
  int n, x[10];
  scanf("%d", &n);
  for (int i = 0; i < n; i++) {
    scanf("%d", &x[i]);
  }
  sort(x, x+n);
  lib::math *math = new lib::math();
  math->a = 0;
  return 0;
}
```

[reference][anchor-1]

![Google](https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)

![](https://ssl.gstatic.com/gb/images/v1_76783e20.png){:height="50px" width="auto"}

[^1]: Some *crazy* footnote definition.

[^footnote]:
    > Blockquotes can be in a footnote.

        as well as code blocks

    or, naturally, simple paragraphs.

[^other-note]:       no code block here (spaces are stripped away)

[^codeblock-note]:
        this is now a code block (8 spaces indentation)

{::comment}
This text is completely ignored by kramdown - a comment in the text.
{:/comment}

Do you see {::comment}this text{:/comment}?
{::comment}some other comment{:/}

{::options key="val" /}

{::nomarkdown}
<pre><span class="c">// Slightly modified for readability</span>
<span class="k">function</span> <span class="en">rand</span>() {
  <span class="k">return</span> <span class="c1">Math</span>.<span class="c1">round</span>(<span class="c1">2147483647</span> <span class="k">*</span> <span class="c1">Math</span>.<span class="c1">random</span>());
}

<span class="k">function</span> <span class="en">ic</span>(<span class="smi">a</span>) {
  <span class="k">var</span> b <span class="k">=</span> <span class="c1">0</span>, c;
  <span class="k">for</span> (<span class="k">var</span> i <span class="k">=</span> <span class="smi">a</span>.<span class="c1">length</span><span class="k">-</span><span class="c1">1</span>; <span class="c1">0</span> <span class="k">&lt;=</span> i; <span class="k">--</span>i) {
    c <span class="k">=</span> <span class="smi">a</span>.<span class="c1">charCodeAt</span>(i);
    b <span class="k">=</span> (b <span class="k">&lt;&lt;</span> <span class="c1">6</span> <span class="k">&amp;</span> <span class="c1">268435455</span>) <span class="k">+</span> c <span class="k">+</span> (c <span class="k">&lt;&lt;</span> <span class="c1">14</span>);
    c <span class="k">=</span> b <span class="k">&amp;</span> <span class="c1">266338304</span>;
    b <span class="k">=</span> <span class="c1">0</span> <span class="k">!=</span> c <span class="k">?</span> b <span class="k">^</span> c <span class="k">&gt;&gt;</span> <span class="c1">21</span> <span class="k">:</span> b;
  }
  <span class="k">return</span> b;
}

<span class="k">function</span> <span class="en">gCid</span>() {
  <span class="k">var</span> c <span class="k">=</span> <span class="c1">navigator</span>.<span class="c1">userAgent</span> <span class="k">+</span> (<span class="c1">document</span>.<span class="c1">cookie</span> <span class="k">?</span> <span class="c1">document</span>.<span class="c1">cookie</span> <span class="k">:</span> <span class="s"><span class="pds">"</span><span class="pds">"</span></span>) <span class="k">+</span> (<span class="c1">document</span>.<span class="c1">referrer</span> <span class="k">?</span> <span class="c1">document</span>.<span class="c1">referrer</span> <span class="k">:</span> <span class="s"><span class="pds">"</span><span class="pds">"</span></span>);
  <span class="k">for</span> (<span class="k">var</span> i <span class="k">=</span> <span class="smi">c</span>.<span class="c1">length</span>, j <span class="k">=</span> <span class="smi">history</span>.<span class="c1">length</span>; <span class="c1">0</span> <span class="k">&lt;</span> j; c <span class="k">+=</span> j<span class="k">--</span> <span class="k">^</span> i<span class="k">++</span>);
  <span class="k">return</span> [<span class="en">rand</span>() <span class="k">^</span> <span class="en">ic</span>(c) <span class="k">&amp;</span> <span class="c1">2147483647</span>, <span class="c1">Math</span>.<span class="c1">round</span>((<span class="k">new</span> <span class="en">Date</span>).<span class="c1">getTime</span>() <span class="k">/</span> <span class="c1">1e3</span>)].<span class="c1">join</span>(<span class="s"><span class="pds">"</span>.<span class="pds">"</span></span>);
}</pre>
{:/nomarkdown}
