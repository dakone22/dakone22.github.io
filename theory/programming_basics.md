---


---

<h1 id="основы-программирования.-теория">Основы программирования. Теория</h1>
<p><strong>Язык</strong>: <em>Delphi Pascal</em>.</p>
<h1 id="синтаксис-и-семантика-языков-программирования.-алфавит-языка-delphi-pascal.-cинтаксические-диаграммы">Синтаксис и семантика языков программирования. Алфавит языка Delphi Pascal. Cинтаксические диаграммы</h1>
<p><strong>Синтаксис</strong> - совокупность правил, определяющих допустимые конструкции (слова, предложения) языка, его форму.</p>
<p><strong>Семантика</strong>  – правила, определяющие смысл синтаксически корректных предложений.</p>
<p>Ясная или «интуитивно-понятная» <em>семантика</em> – семантика, позволяющая без большого труда определять смысл программы или «читать» ее.</p>
<p>Алфавит языка программирования <em>Delphi Pascal</em> включает:</p>
<ol>
<li>латинские буквы <strong>без различия</strong> строчных и прописных + символ <code>_</code> (считается как буква);</li>
<li>арабские цифры: <code>0</code>, <code>1</code>, <code>2</code>, <code>3</code>, <code>4</code>, <code>5</code>, <code>6</code>, <code>7</code>, <code>8</code>, <code>9</code>;</li>
<li>шестнадцатеричные цифры: <code>0..9</code>, <code>а..f</code> или <code>A..F</code>;</li>
<li>специальные символы: <code>+</code> <code>-</code> <code>*</code> <code>/</code> <code>=</code> <code>:=</code> <code>;</code> и т.  д.;</li>
<li>служебные слова: <code>do</code>, <code>while</code>, <code>begin</code>, <code>end</code> и т.  д.</li>
</ol>
<p><strong>Синтаксис</strong> – правила, определяющие допустимые конструкции языка, построенные из символов его алфавита.</p>
<p><strong>Синтаксическая диаграмма</strong> — это направленный граф с одним входным ребром и одним выходным ребром и помеченными вершинами. Синтаксическая диаграмма задаёт язык. Цепочка пометок при вершинах на любом пути от входного ребра к выходному — это цепочка языка, задаваемого синтаксической диаграммой.</p>
<p><img src="https://i.imgur.com/PpBOjy8.png" alt="Syntax diagram example"></p>
<h1 id="представление-данных-в-delphi-pascal-константы-и-переменные">Представление данных в Delphi Pascal: константы и переменные</h1>
<h2 id="представление-данных">Представление данных</h2>
<ul>
<li>Данные.
<ol>
<li>Константы.
<ol>
<li>Литералы.</li>
<li>Поименованные константы.</li>
</ol>
</li>
<li>Переменные.</li>
</ol>
</li>
</ul>
<p>В языке <em>Delphi Pascal</em>  все данные подразделяются на <em>константы</em> и <em>переменные</em>:</p>
<p><strong>Константы</strong> – данные, не изменяемые в процессе выполнения программы.</p>
<p>Константы, в свою очередь, подразделяются на <em>литералы</em> и <em>поименованные константы</em>.</p>
<p><strong>Литералы</strong> – константы, указанные непосредственно в тексте программы.</p>
<p>Примеры  литералов:</p>
<ol>
<li><code>-25</code>, <code>2.5</code>, <code>0.1e6</code> – числовые литералы;</li>
<li><code>$2a</code> – шестнадцатеричное число;</li>
<li><code>true</code>, <code>false</code> – логические константы;</li>
<li><code>'d'</code>, <code>#65 = 'A'</code> – символьные константы;</li>
<li><code>'abcd'</code>  – строковая константа;</li>
<li><code>nil</code>  – адресная константа.</li>
</ol>
<p><strong>Поименованные константы</strong> – константы, обращение к которым выполняется по имени. Объявляются в разделе описаний: <code>const &lt;имя&gt;[: &lt;тип&gt;] = &lt;значение&gt;;</code>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">const</span>
    min<span class="token punctuation">:</span> byte <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
    max <span class="token operator">=</span> <span class="token number">100</span><span class="token punctuation">;</span>
    center <span class="token operator">=</span> <span class="token punctuation">(</span>max <span class="token operator">-</span> min<span class="token punctuation">)</span> <span class="token operator">div</span> <span class="token number">2</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<p><strong>Переменные</strong> – поименованные данные, которые могут изменяться в процессе выполнения программы. Объявляются также в разделе описаний: <code>var &lt;имя&gt;[, &lt;имя&gt;]: &lt;тип&gt;;</code></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">,</span> b<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
    c<span class="token punctuation">:</span> Real<span class="token punctuation">;</span>
</code></pre>
<hr>
<p>При установленной опции  <code>Extended syntax</code>  <code>{$X+}</code> (<em>расширенный синтаксис</em>) переменным при объявлении можно задавать начальные значения:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span> 
    a<span class="token punctuation">:</span> Integer <span class="token operator">=</span> <span class="token number">56</span><span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> Real <span class="token operator">=</span> <span class="token number">85.25</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<p>Для <strong>наложения</strong> или же создания <strong>абсолютной переменной</strong> (которая находится по заданному или абсолютному адресу в памяти) используется служебное слово <strong><code>absolute</code></strong>:</p>
<p><code>var &lt;имя&gt;: &lt;тип&gt; absoulute &lt;адрес&gt;:&lt;смещение&gt;;</code> или</p>
<p><code>var &lt;имя&gt;: &lt;тип&gt; absoulute &lt;переменная&gt;;</code>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token comment">//Наложение по абсолютному адресу:</span>
<span class="token keyword">var</span>
    a<span class="token punctuation">:</span> Word <span class="token keyword">absolute</span> <span class="token number">$0000</span><span class="token punctuation">:</span><span class="token number">$00FF</span><span class="token punctuation">;</span>  <span class="token comment">// адрес_сегмента:смещение</span>
    c<span class="token punctuation">:</span> Byte<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> Real <span class="token keyword">absolute</span> c<span class="token punctuation">;</span>  <span class="token comment">// наложение на ранее определенную переменную;</span>
       <span class="token comment">// обычно используется, когда тип переменной, которая тут `c`, может быть разным. </span>
       <span class="token comment">// (см. нетипизированные параметры)</span>
</code></pre>
<hr>
<p><strong>Тип</strong> – описатель данных, который определяет:</p>
<ol>
<li>диапазон изменения значения переменной, задавая размер ее внутреннего представления;</li>
<li>множество операций, которые могут выполняться над этой переменной.</li>
</ol>
<p>Для объявления новых типов данных используется конструкция: <code>type &lt;имя&gt; = &lt;тип&gt;;</code>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    Int <span class="token operator">=</span> LongInt<span class="token punctuation">;</span>
    Date <span class="token operator">=</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span>  <span class="token comment">// объявление нового типа данных</span>

<span class="token keyword">var</span>
    d1<span class="token punctuation">:</span> Date<span class="token punctuation">;</span>  <span class="token comment">// объявление переменной этого типа</span>
</code></pre>
<h1 id="классификация--скалярных-типов-данных-операции-над-ними">Классификация  скалярных типов данных, операции над ними</h1>
<h2 id="классификация-типов-данных-языка">Классификация типов данных языка</h2>
<ol>
<li>Тип
<ol>
<li>Простой
<ol>
<li>Порядковые
<ol>
<li>Целые;</li>
<li>Логические;</li>
<li>Символ;</li>
<li><em>Перечисление;</em></li>
<li><em>Отрезок (Интервал);</em></li>
</ol>
</li>
<li>Вещественный
<ol>
<li>Вещественные;</li>
<li>Большое целое;</li>
</ol>
</li>
</ol>
</li>
<li>Структурный
<ol>
<li>Массив;</li>
<li>Строка;</li>
<li>Запись;</li>
<li>Множество;</li>
<li>Файл;</li>
<li>Указатель; <!--- &#1056;&#1072;&#1079;&#1074;&#1077; &#1091;&#1082;&#1072;&#1079;&#1072;&#1090;&#1077;&#1083;&#1100; &#1101;&#1090;&#1086; &#1085;&#1077; &#1087;&#1088;&#1086;&#1089;&#1090;&#1086; &#1094;&#1077;&#1083;&#1086;&#1077; &#1073;&#1077;&#1079;&#1079;&#1085;&#1072;&#1082;&#1086;&#1074;&#1086;&#1077; &#1095;&#1080;&#1089;&#1083;&#1086;? --></li>
</ol>
</li>
</ol>
</li>
</ol>
<ul>
<li>
<p><strong>Целочисленные знаковые типы</strong></p>

<table>
<thead>
<tr>
<th>Идентификатор</th>
<th>Длина, байт</th>
<th>Диапазон значений</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>ShortInt</code>, <code>Int8</code></td>
<td><code>1</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>128..127</mn></mrow><annotation encoding="application/x-tex">-128..127</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">1</span><span class="mord">2</span><span class="mord">8</span><span class="mord">.</span><span class="mord">.</span><span class="mord">1</span><span class="mord">2</span><span class="mord">7</span></span></span></span></span></td>
</tr>
<tr>
<td><code>SmallInt</code>, <code>Int16</code></td>
<td><code>2</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>32768..32767</mn></mrow><annotation encoding="application/x-tex">-32768..32767</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">3</span><span class="mord">2</span><span class="mord">7</span><span class="mord">6</span><span class="mord">8</span><span class="mord">.</span><span class="mord">.</span><span class="mord">3</span><span class="mord">2</span><span class="mord">7</span><span class="mord">6</span><span class="mord">7</span></span></span></span></span></td>
</tr>
<tr>
<td><em><code>Integer</code></em>*</td>
<td><code>2-4</code></td>
<td>Зависит от платформы</td>
</tr>
<tr>
<td><code>LongInt</code>, <code>Int32</code></td>
<td><code>4</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>2147483648..2147483647</mn></mrow><annotation encoding="application/x-tex">-2147483648..2147483647</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">2</span><span class="mord">1</span><span class="mord">4</span><span class="mord">7</span><span class="mord">4</span><span class="mord">8</span><span class="mord">3</span><span class="mord">6</span><span class="mord">4</span><span class="mord">8</span><span class="mord">.</span><span class="mord">.</span><span class="mord">2</span><span class="mord">1</span><span class="mord">4</span><span class="mord">7</span><span class="mord">4</span><span class="mord">8</span><span class="mord">3</span><span class="mord">6</span><span class="mord">4</span><span class="mord">7</span></span></span></span></span></td>
</tr>
<tr>
<td><code>NativeInt</code></td>
<td><code>4-8</code></td>
<td>Зависит от типа процессора</td>
</tr>
<tr>
<td><code>Int64</code></td>
<td><code>8</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>9223372036854775808..9223372036854775807</mn></mrow><annotation encoding="application/x-tex">-9223372036854775808..9223372036854775807</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">9</span><span class="mord">2</span><span class="mord">2</span><span class="mord">3</span><span class="mord">3</span><span class="mord">7</span><span class="mord">2</span><span class="mord">0</span><span class="mord">3</span><span class="mord">6</span><span class="mord">8</span><span class="mord">5</span><span class="mord">4</span><span class="mord">7</span><span class="mord">7</span><span class="mord">5</span><span class="mord">8</span><span class="mord">0</span><span class="mord">8</span><span class="mord">.</span><span class="mord">.</span><span class="mord">9</span><span class="mord">2</span><span class="mord">2</span><span class="mord">3</span><span class="mord">3</span><span class="mord">7</span><span class="mord">2</span><span class="mord">0</span><span class="mord">3</span><span class="mord">6</span><span class="mord">8</span><span class="mord">5</span><span class="mord">4</span><span class="mord">7</span><span class="mord">7</span><span class="mord">5</span><span class="mord">8</span><span class="mord">0</span><span class="mord">7</span></span></span></span></span></td>
</tr>
</tbody>
</table></li>
<li>
<p><strong>Целочисленные беззнаковые типы</strong></p>

<table>
<thead>
<tr>
<th>Идентификатор</th>
<th>Длина, байт</th>
<th>Диапазон значений</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Byte</code>, <code>UInt8</code></td>
<td><code>1</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>0..255</mn></mrow><annotation encoding="application/x-tex">0..255</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">0</span><span class="mord">.</span><span class="mord">.</span><span class="mord">2</span><span class="mord">5</span><span class="mord">5</span></span></span></span></span></td>
</tr>
<tr>
<td><code>Word</code>, <code>UInt16</code></td>
<td><code>2</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>0..65535</mn></mrow><annotation encoding="application/x-tex">0..65535</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">0</span><span class="mord">.</span><span class="mord">.</span><span class="mord">6</span><span class="mord">5</span><span class="mord">5</span><span class="mord">3</span><span class="mord">5</span></span></span></span></span></td>
</tr>
<tr>
<td><code>LongWord</code>, <code>Cardinal</code>, <code>UInt32</code>, <s><code>DWord</code></s>**</td>
<td><code>4</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>0..4294967295</mn></mrow><annotation encoding="application/x-tex">0..4294967295</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">0</span><span class="mord">.</span><span class="mord">.</span><span class="mord">4</span><span class="mord">2</span><span class="mord">9</span><span class="mord">4</span><span class="mord">9</span><span class="mord">6</span><span class="mord">7</span><span class="mord">2</span><span class="mord">9</span><span class="mord">5</span></span></span></span></span></td>
</tr>
<tr>
<td><em><code>NativeUInt</code></em></td>
<td><code>4-8</code></td>
<td>Зависит от типа процессора</td>
</tr>
<tr>
<td><s><code>QWord</code></s>**, <code>UInt64</code></td>
<td><code>8</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>0..18446744073709551615</mn></mrow><annotation encoding="application/x-tex">0..18446744073709551615</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">0</span><span class="mord">.</span><span class="mord">.</span><span class="mord">1</span><span class="mord">8</span><span class="mord">4</span><span class="mord">4</span><span class="mord">6</span><span class="mord">7</span><span class="mord">4</span><span class="mord">4</span><span class="mord">0</span><span class="mord">7</span><span class="mord">3</span><span class="mord">7</span><span class="mord">0</span><span class="mord">9</span><span class="mord">5</span><span class="mord">5</span><span class="mord">1</span><span class="mord">6</span><span class="mord">1</span><span class="mord">5</span></span></span></span></span></td>
</tr>
</tbody>
</table></li>
<li>
<p><strong>Вещественные типы</strong></p>

<table>
<thead>
<tr>
<th>Идентификатор</th>
<th>Длина, байт</th>
<th>Количество значащих цифр</th>
<th>Диапазон значений</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Single</code></td>
<td><code>4</code></td>
<td><code>7-8</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>1.5</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mrow><mo>−</mo><mn>45</mn></mrow></msup><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mn>3.4</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mn>38</mn></msup></mrow><annotation encoding="application/x-tex">-1.5 * 10^{-45} .. 3.4 * 10^{38}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">1</span><span class="mord">.</span><span class="mord">5</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">−</span><span class="mord mtight">4</span><span class="mord mtight">5</span></span></span></span></span></span></span></span></span><span class="mord">.</span><span class="mord">.</span><span class="mord">3</span><span class="mord">.</span><span class="mord">4</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">8</span></span></span></span></span></span></span></span></span></span></span></span></span></td>
</tr>
<tr>
<td><code>Real48</code></td>
<td><code>6</code></td>
<td><code>11-12</code> <!---&#1058;&#1086;&#1095;&#1085;&#1086; &#1085;&#1077; &#1079;&#1085;&#1072;&#1102;, &#1074;&#1079;&#1103;&#1090;&#1086; &#1089;&#1088;&#1077;&#1076;&#1085;&#1077;&#1077; &#1084;&#1077;&#1078;&#1076;&#1091; 4 &#1080; 8 &#1073;&#1072;&#1081;&#1090;&#1085;&#1099;&#1084;&#1080; &#1090;&#1080;&#1087;&#1072;&#1084;&#1080;--></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>2.9</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mrow><mo>−</mo><mn>39</mn></mrow></msup><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mn>1.7</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mn>38</mn></msup></mrow><annotation encoding="application/x-tex">2.9 * 10^{-39} .. 1.7 * 10^{38}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">2</span><span class="mord">.</span><span class="mord">9</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">−</span><span class="mord mtight">3</span><span class="mord mtight">9</span></span></span></span></span></span></span></span></span><span class="mord">.</span><span class="mord">.</span><span class="mord">1</span><span class="mord">.</span><span class="mord">7</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">8</span></span></span></span></span></span></span></span></span></span></span></span></span></td>
</tr>
<tr>
<td><em><code>Real</code></em>*</td>
<td><code>6-8</code></td>
<td>???</td>
<td>Зависит от платформы</td>
</tr>
<tr>
<td><code>Double</code></td>
<td><code>8</code></td>
<td><code>15-16</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>2.2</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mrow><mo>−</mo><mn>308</mn></mrow></msup><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mn>1.8</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mn>308</mn></msup></mrow><annotation encoding="application/x-tex">-2.2 * 10^{-308} .. 1.8 * 10^{308}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">2</span><span class="mord">.</span><span class="mord">2</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">−</span><span class="mord mtight">3</span><span class="mord mtight">0</span><span class="mord mtight">8</span></span></span></span></span></span></span></span></span><span class="mord">.</span><span class="mord">.</span><span class="mord">1</span><span class="mord">.</span><span class="mord">8</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">0</span><span class="mord mtight">8</span></span></span></span></span></span></span></span></span></span></span></span></span></td>
</tr>
<tr>
<td><code>Currency</code></td>
<td><code>8</code></td>
<td>(4 знака после запятой)</td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>922337203685477.5808..922337203685477.5807</mn></mrow><annotation encoding="application/x-tex">-922337203685477.5808 .. 922337203685477.5807</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">9</span><span class="mord">2</span><span class="mord">2</span><span class="mord">3</span><span class="mord">3</span><span class="mord">7</span><span class="mord">2</span><span class="mord">0</span><span class="mord">3</span><span class="mord">6</span><span class="mord">8</span><span class="mord">5</span><span class="mord">4</span><span class="mord">7</span><span class="mord">7</span><span class="mord">.</span><span class="mord">5</span><span class="mord">8</span><span class="mord">0</span><span class="mord">8</span><span class="mord">.</span><span class="mord">.</span><span class="mord">9</span><span class="mord">2</span><span class="mord">2</span><span class="mord">3</span><span class="mord">3</span><span class="mord">7</span><span class="mord">2</span><span class="mord">0</span><span class="mord">3</span><span class="mord">6</span><span class="mord">8</span><span class="mord">5</span><span class="mord">4</span><span class="mord">7</span><span class="mord">7</span><span class="mord">.</span><span class="mord">5</span><span class="mord">8</span><span class="mord">0</span><span class="mord">7</span></span></span></span></span></td>
</tr>
<tr>
<td><code>Comp</code></td>
<td><code>8</code></td>
<td><code>19-20</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>9223372036854775807..9223372036854775807</mn></mrow><annotation encoding="application/x-tex">-9223372036854775807..9223372036854775807</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">9</span><span class="mord">2</span><span class="mord">2</span><span class="mord">3</span><span class="mord">3</span><span class="mord">7</span><span class="mord">2</span><span class="mord">0</span><span class="mord">3</span><span class="mord">6</span><span class="mord">8</span><span class="mord">5</span><span class="mord">4</span><span class="mord">7</span><span class="mord">7</span><span class="mord">5</span><span class="mord">8</span><span class="mord">0</span><span class="mord">7</span><span class="mord">.</span><span class="mord">.</span><span class="mord">9</span><span class="mord">2</span><span class="mord">2</span><span class="mord">3</span><span class="mord">3</span><span class="mord">7</span><span class="mord">2</span><span class="mord">0</span><span class="mord">3</span><span class="mord">6</span><span class="mord">8</span><span class="mord">5</span><span class="mord">4</span><span class="mord">7</span><span class="mord">7</span><span class="mord">5</span><span class="mord">8</span><span class="mord">0</span><span class="mord">7</span></span></span></span></span></td>
</tr>
<tr>
<td><em><code>Extended</code></em>*</td>
<td><code>8</code></td>
<td><code>15-16</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>2.2</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mrow><mo>−</mo><mn>308</mn></mrow></msup><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mn>1.8</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mn>308</mn></msup></mrow><annotation encoding="application/x-tex">-2.2 * 10^{-308} .. 1.8 * 10^{308}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">2</span><span class="mord">.</span><span class="mord">2</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">−</span><span class="mord mtight">3</span><span class="mord mtight">0</span><span class="mord mtight">8</span></span></span></span></span></span></span></span></span><span class="mord">.</span><span class="mord">.</span><span class="mord">1</span><span class="mord">.</span><span class="mord">8</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">0</span><span class="mord mtight">8</span></span></span></span></span></span></span></span></span></span></span></span></span></td>
</tr>
<tr>
<td><em><code>Extended</code></em>*</td>
<td><code>10</code></td>
<td><code>19-20</code></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>−</mo><mn>3.4</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mrow><mo>−</mo><mn>4932</mn></mrow></msup><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mn>1.1</mn><mo>∗</mo><mn>1</mn><msup><mn>0</mn><mn>4932</mn></msup></mrow><annotation encoding="application/x-tex">-3.4 * 10^{-4932} .. 1.1 * 10^{4932}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">−</span><span class="mord">3</span><span class="mord">.</span><span class="mord">4</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">−</span><span class="mord mtight">4</span><span class="mord mtight">9</span><span class="mord mtight">3</span><span class="mord mtight">2</span></span></span></span></span></span></span></span></span><span class="mord">.</span><span class="mord">.</span><span class="mord">1</span><span class="mord">.</span><span class="mord">1</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">4</span><span class="mord mtight">9</span><span class="mord mtight">3</span><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span></span></span></span></td>
</tr>
</tbody>
</table></li>
<li>
<p><strong>Символьные типы</strong></p>

<table>
<thead>
<tr>
<th>Идентификатор</th>
<th>Длина, байт</th>
<th>Диапазон значений</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>AnsiChar</code></td>
<td><code>1</code></td>
<td><code>#0..#255</code></td>
</tr>
<tr>
<td><em><code>Char</code></em>*</td>
<td><code>1-2</code></td>
<td>Зависит от платформы</td>
</tr>
<tr>
<td><code>WideChar</code>, <s><code>UnicodeChar</code></s>**</td>
<td><code>2</code></td>
<td><code>#0..#65535</code></td>
</tr>
</tbody>
</table></li>
<li>
<p><strong>Логические типы</strong></p>

<table>
<thead>
<tr>
<th>Идентификатор</th>
<th>Длина, байт</th>
<th>Диапазон значений</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Boolean</code></td>
<td><code>1</code></td>
<td><code>False..True</code></td>
</tr>
<tr>
<td><code>ByteBool</code></td>
<td><code>1</code></td>
<td><code>False..True</code></td>
</tr>
<tr>
<td><code>WordBool</code></td>
<td><code>2</code></td>
<td><code>False..True</code></td>
</tr>
<tr>
<td><code>LongBool</code></td>
<td><code>4</code></td>
<td><code>False..True</code></td>
</tr>
</tbody>
</table></li>
<li>
<p><strong>Перечисления</strong> – значения переменных этого типа описываются явно (перечисляются).</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    DayOfWeek <span class="token operator">=</span> <span class="token punctuation">(</span>Mon<span class="token punctuation">,</span> Tue<span class="token punctuation">,</span> Wed<span class="token punctuation">,</span> Thu<span class="token punctuation">,</span> Fri<span class="token punctuation">,</span> Sat<span class="token punctuation">,</span> Sun<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span>
    d<span class="token punctuation">:</span> DayOfWeek<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
d <span class="token operator">:=</span> Fri<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Отрезок</strong> – значения переменных этого типа входят в определенный диапазон значений стандартного типа.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    Day <span class="token operator">=</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span>  <span class="token comment">// значения - числа от 1 до 31</span>
<span class="token keyword">var</span>
    d<span class="token punctuation">:</span> Day<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
d <span class="token operator">:=</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<p><strong>*</strong> Зависит от платформы. В <em>Delphi Pascal</em>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
	Integer <span class="token operator">=</span> LongInt<span class="token punctuation">;</span>  <span class="token comment">// FreePscal: SmallInt</span>
	Real <span class="token operator">=</span> Double<span class="token punctuation">;</span>      <span class="token comment">// FreePascal: 6-byte</span>
	<span class="token comment">// Extended (10 bytes)</span>
	Char <span class="token operator">=</span> WideChar<span class="token punctuation">;</span>    <span class="token comment">// since Delphi 2009, FreePascal: ANSIChar</span>
</code></pre>
<p><strong>**</strong> Идентификаторы отсутствуют в <em>Delphi Pascal</em>.</p>
<h6 id="источники-wiki.freepascal.org-1-wiki.freepascal.org-2-delphibasics.ru.">Источники: <a href="https://wiki.freepascal.org/Data_type">wiki.freepascal.org 1</a>, <a href="https://wiki.freepascal.org/Variables_and_Data_Types">wiki.freepascal.org 2</a>, <a href="http://delphibasics.ru/1Types.php">delphibasics.ru</a>.</h6>
<h2 id="процедуры-и-функции-порядковых-типов-данных">Процедуры и функции порядковых типов данных</h2>
<ol>
<li>Функция <code>ord(x: ordinal): int</code> – возвращает номер значения по порядку (не применима к 64-битным аргументам)<pre class=" language-pascal"><code class="prism  language-pascal">ord<span class="token punctuation">(</span><span class="token string">'A'</span><span class="token punctuation">)</span>  <span class="token comment">// 65</span>
</code></pre>
</li>
<li>Функция <code>pred(x: ordinal): int</code> – возвращает предыдущее значение.<br>
Процедура <code>dec(var x: int)</code> – уменьшает значение переменной на <code>1</code>.<pre class=" language-pascal"><code class="prism  language-pascal">x <span class="token operator">:=</span> <span class="token number">5</span><span class="token punctuation">;</span>
pred<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 4</span>
dec<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 4</span>
</code></pre>
</li>
<li>Функция <code>succ(x: ordinal): int</code> – возвращает следующее значение.<br>
Процедура <code>inc(var x: int)</code> – увеличивает значение переменной на <code>1</code>.<pre class=" language-pascal"><code class="prism  language-pascal">x <span class="token operator">:=</span> <span class="token number">5</span><span class="token punctuation">;</span>
succ<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 6</span>
inc<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 6</span>
</code></pre>
</li>
<li>Функция <code>high(x)</code> – возвращает самое большое значение типа переменной <code>x</code> или максимальный размер типа строки или массива переменной <code>x</code>.<br>
Функция <code>low(x)</code> – возвращает самое малое значение типа переменной <code>x</code> или минимальный размер типа строки или массива переменной <code>x</code>.<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    x<span class="token punctuation">:</span> ShortInt<span class="token punctuation">;</span>
    s<span class="token punctuation">:</span> <span class="token keyword">String</span><span class="token punctuation">[</span><span class="token number">42</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    m<span class="token punctuation">:</span> <span class="token keyword">array</span> <span class="token punctuation">[</span><span class="token number">5</span><span class="token operator">..</span><span class="token number">35</span><span class="token punctuation">]</span> <span class="token keyword">of</span> ShortInt<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
writeLn<span class="token punctuation">(</span>low<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">', '</span><span class="token punctuation">,</span> high<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// -128, 127</span>
writeLn<span class="token punctuation">(</span>low<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">', '</span><span class="token punctuation">,</span> high<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 0, 42</span>
writeLn<span class="token punctuation">(</span>low<span class="token punctuation">(</span>m<span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">', '</span><span class="token punctuation">,</span> high<span class="token punctuation">(</span>m<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 5, 35</span>
</code></pre>
</li>
</ol>
<h2 id="операции-над-скалярными-типами-данных.">Операции над скалярными типами данных.</h2>
<ol>
<li><strong>Арифметические  операции</strong> – применяют к вещественным и целым константам и переменным:<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token operator">+</span> <span class="token operator">-</span> <span class="token operator">*</span>
<span class="token operator">/</span>  <span class="token comment">{вещественное деление}</span>
<span class="token operator">div</span><span class="token punctuation">,</span> <span class="token operator">mod</span>  <span class="token comment">{целочисленное деление и остаток от целочисленного}</span>
</code></pre>
</li>
<li><strong>Операции отношения</strong> – применяют к числам, символам, строкам для сравнения. Результат – логическое значение:
<table>
<thead>
<tr>
<th>не равно</th>
<th>равно</th>
</tr>
</thead>
<tbody>
<tr>
<td>&lt;&gt;</td>
<td>=</td>
</tr>
<tr>
<td><strong>нестрогие</strong></td>
<td><strong>строгие</strong></td>
</tr>
<tr>
<td>&lt;</td>
<td>&lt;=</td>
</tr>
<tr>
<td>&gt;</td>
<td>&gt;=</td>
</tr>
</tbody>
</table>
</li>
<li><strong>Логические операции</strong> – применяют к логическим значениям. Результат логическое значение:<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">,</span> b<span class="token punctuation">:</span> Boolean<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a <span class="token operator">:=</span> <span class="token keyword">true</span><span class="token punctuation">;</span> 
b <span class="token operator">:=</span> <span class="token keyword">false</span><span class="token punctuation">;</span>
a <span class="token operator">and</span> b <span class="token comment">{false}</span><span class="token punctuation">;</span>  <span class="token operator">not</span> a <span class="token comment">{false}</span><span class="token punctuation">;</span>  a <span class="token operator">xor</span> b <span class="token comment">{true}</span>
a <span class="token operator">or</span> b <span class="token comment">{true}</span><span class="token punctuation">;</span>    <span class="token operator">not</span> b <span class="token comment">{true}</span><span class="token punctuation">;</span>   a <span class="token operator">xor</span> a <span class="token comment">{false}</span>
</code></pre>
</li>
<li><strong>Побитовые (поразрядные) операции</strong> – выполняются поразрядно, применяют к целым. Результат целое число.<br>
<code>not</code>, <code>and</code>, <code>or</code>, <code>xor</code>, <code>shr</code> (сдвиг вправо), <code>shl</code> (сдвиг влево).<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span> 
    a<span class="token punctuation">:</span> Byte<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a <span class="token operator">:=</span> <span class="token number">5</span><span class="token punctuation">;</span>
<span class="token operator">not</span> a   <span class="token comment">{побитовая инверсия (НЕ)   : 00000101 -&gt; 11111010}</span><span class="token punctuation">;</span>
a <span class="token operator">shl</span> <span class="token number">2</span> <span class="token comment">{побитовый сдвиг влево на 2: 00000101 -&gt; 00010100}</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ol>
<h2 id="математические-функции">Математические функции</h2>
<p>(<code>int</code> – абстрактный целочисленный тип, <code>float</code> – абстрактный вещественный тип)</p>

<table>
<thead>
<tr>
<th>Имя функции</th>
<th>Тип принимаемого значения</th>
<th>Тип возвращаемого значения</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>abs(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td>так же, как аргумент</td>
<td>Модуль числа (абсолютное значение числа)</td>
</tr>
<tr>
<td><code>sqr(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td>так же, как аргумент</td>
<td>Квадрат числа (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msup><mi>x</mi><mn>2</mn></msup></mrow><annotation encoding="application/x-tex">x^2</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord"><span class="mord mathdefault">x</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span></span></span>)</td>
</tr>
<tr>
<td><code>sqrt(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td><code>float</code></td>
<td>Квадратный корень числа (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msqrt><mi>x</mi></msqrt></mrow><annotation encoding="application/x-tex">\sqrt{x}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 1.04em; vertical-align: -0.23972em;"></span><span class="mord sqrt"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.80028em;"><span class="svg-align" style="top: -3em;"><span class="pstrut" style="height: 3em;"></span><span class="mord" style="padding-left: 0.833em;"><span class="mord mathdefault">x</span></span></span><span class="" style="top: -2.76028em;"><span class="pstrut" style="height: 3em;"></span><span class="hide-tail" style="min-width: 0.853em; height: 1.08em;"><svg width="400em" height="1.08em" viewBox="0 0 400000 1080" preserveAspectRatio="xMinYMin slice"><path d="M95,702c-2.7,0,-7.17,-2.7,-13.5,-8c-5.8,-5.3,-9.5,
-10,-9.5,-14c0,-2,0.3,-3.3,1,-4c1.3,-2.7,23.83,-20.7,67.5,-54c44.2,-33.3,65.8,
-50.3,66.5,-51c1.3,-1.3,3,-2,5,-2c4.7,0,8.7,3.3,12,10s173,378,173,378c0.7,0,
35.3,-71,104,-213c68.7,-142,137.5,-285,206.5,-429c69,-144,104.5,-217.7,106.5,
-221c5.3,-9.3,12,-14,20,-14H400000v40H845.2724s-225.272,467,-225.272,467
s-235,486,-235,486c-2.7,4.7,-9,7,-19,7c-6,0,-10,-1,-12,-3s-194,-422,-194,-422
s-65,47,-65,47z M834 80H400000v40H845z"></path></svg></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.23972em;"><span class=""></span></span></span></span></span></span></span></span></span>)</td>
</tr>
<tr>
<td><code>exp(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td><code>float</code></td>
<td>Экспонента числа (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msup><mi>e</mi><mi>x</mi></msup></mrow><annotation encoding="application/x-tex">e^x</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.664392em; vertical-align: 0em;"></span><span class="mord"><span class="mord mathdefault">e</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.664392em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathdefault mtight">x</span></span></span></span></span></span></span></span></span></span></span></span>)</td>
</tr>
<tr>
<td><code>ln(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td><code>float</code></td>
<td>Натуральный логарифм числа</td>
</tr>
<tr>
<td><code>sin(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td><code>float</code></td>
<td>Синус числа</td>
</tr>
<tr>
<td><code>cos(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td><code>float</code></td>
<td>Косинус числа</td>
</tr>
<tr>
<td><code>arctan(x)</code></td>
<td><code>int</code> или <code>float</code></td>
<td><code>float</code></td>
<td>Арктангенс числа</td>
</tr>
</tbody>
</table><h3 id="работа-с-вещественными-числами-и-генератором-псевдослучайных-чисел">Работа с вещественными числами и генератором псевдослучайных чисел</h3>

<table>
<thead>
<tr>
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>int(x: float): int</code></td>
<td>Целая часть числа <code>x</code></td>
</tr>
<tr>
<td><code>frac(x: float): int</code></td>
<td>Дробная часть числа <code>x</code></td>
</tr>
<tr>
<td><code>randomize</code></td>
<td>Инициализация генератора псевдослучайных чисел</td>
</tr>
<tr>
<td><code>random: float</code></td>
<td>Случайное число <code>r</code> в диапазоне: <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>0</mn><mo>≤</mo><mi>r</mi><mo>&lt;</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">0 \le r \lt 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.78041em; vertical-align: -0.13597em;"></span><span class="mord">0</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">≤</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.5782em; vertical-align: -0.0391em;"></span><span class="mord mathdefault" style="margin-right: 0.02778em;">r</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&lt;</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">1</span></span></span></span></span></td>
</tr>
<tr>
<td><code>random(x: int): int</code></td>
<td>Случайное целое число <code>r</code> в диапазоне: <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>0</mn><mo>≤</mo><mi>r</mi><mo>&lt;</mo><mi>x</mi></mrow><annotation encoding="application/x-tex">0 \le r \lt x</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.78041em; vertical-align: -0.13597em;"></span><span class="mord">0</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">≤</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.5782em; vertical-align: -0.0391em;"></span><span class="mord mathdefault" style="margin-right: 0.02778em;">r</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&lt;</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.43056em; vertical-align: 0em;"></span><span class="mord mathdefault">x</span></span></span></span></span></td>
</tr>
</tbody>
</table><h2 id="совместимость-типов-данных-и-операции-преобразования-типов">Совместимость типов данных и операции преобразования типов</h2>
<h3 id="правила-вычисления-выражений.-приоритеты">Правила вычисления выражений. Приоритеты</h3>
<ol>
<li>
<p>Порядок выполнения операций определяется <strong>приоритетами</strong> и <strong>скобками</strong>:</p>

<table>
<thead>
<tr>
<th></th>
<th>Операции</th>
<th>Приоритет (порядок выполнения)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Унарные</td>
<td><code>+</code>, <code>-</code>, <code>not</code>, <code>@</code>, <code>^</code></td>
<td>1</td>
</tr>
<tr>
<td></td>
<td><code>*</code>, <code>/</code>, <code>div</code>, <code>mod</code>, <code>and</code>, <code>shr</code>, <code>shl</code></td>
<td>2</td>
</tr>
<tr>
<td></td>
<td><code>+</code>, <code>-</code>, <code>or</code>, <code>xor</code></td>
<td>3</td>
</tr>
<tr>
<td>Логические</td>
<td><code>=</code>, <code>&lt;&gt;</code>, <code>&lt;</code>, <code>&gt;</code>, <code>&lt;=</code>, <code>&gt;=</code></td>
<td>4</td>
</tr>
</tbody>
</table><p>Примеры:</p>
<ol>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mstyle displaystyle="true" scriptlevel="0"><mfrac><mrow><mi>x</mi><mo stretchy="false">(</mo><mi>x</mi><mo>+</mo><mn>2</mn><mo stretchy="false">)</mo></mrow><mrow><mi>y</mi><mo stretchy="false">(</mo><mi>y</mi><mo>−</mo><mn>1</mn><mo stretchy="false">)</mo></mrow></mfrac></mstyle><mo>⇒</mo><mi>x</mi><mo>∗</mo><mo stretchy="false">(</mo><mi>x</mi><mo>+</mo><mn>2</mn><mo stretchy="false">)</mo><mi mathvariant="normal">/</mi><mi>y</mi><mstyle mathcolor="red"><mi mathvariant="normal">/</mi></mstyle><mo stretchy="false">(</mo><mi>y</mi><mo>−</mo><mn>1</mn><mo stretchy="false">)</mo><mo>=</mo><mi>x</mi><mo>∗</mo><mo stretchy="false">(</mo><mi>x</mi><mo>+</mo><mn>2</mn><mo stretchy="false">)</mo><mi mathvariant="normal">/</mi><mstyle mathcolor="red"><mo stretchy="false">(</mo></mstyle><mi>y</mi><mo>∗</mo><mo stretchy="false">(</mo><mi>y</mi><mo>−</mo><mn>1</mn><mo stretchy="false">)</mo><mstyle mathcolor="red"><mo stretchy="false">)</mo></mstyle></mrow><annotation encoding="application/x-tex">\dfrac{x(x+2)}{y(y-1)} \Rightarrow x*(x+2) / y\textcolor{red}{/} (y-1) = x*(x+2) / \textcolor{red}{(}y*(y - 1)\textcolor{red}{)}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 2.363em; vertical-align: -0.936em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.427em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord mathdefault" style="margin-right: 0.03588em;">y</span><span class="mopen">(</span><span class="mord mathdefault" style="margin-right: 0.03588em;">y</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mord">1</span><span class="mclose">)</span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord mathdefault">x</span><span class="mopen">(</span><span class="mord mathdefault">x</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mord">2</span><span class="mclose">)</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.936em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">⇒</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.46528em; vertical-align: 0em;"></span><span class="mord mathdefault">x</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mopen">(</span><span class="mord mathdefault">x</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">2</span><span class="mclose">)</span><span class="mord">/</span><span class="mord mathdefault" style="margin-right: 0.03588em;">y</span><span class="mord" style="color: red;">/</span><span class="mopen">(</span><span class="mord mathdefault" style="margin-right: 0.03588em;">y</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.46528em; vertical-align: 0em;"></span><span class="mord mathdefault">x</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mopen">(</span><span class="mord mathdefault">x</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">2</span><span class="mclose">)</span><span class="mord">/</span><span class="mopen" style="color: red;">(</span><span class="mord mathdefault" style="margin-right: 0.03588em;">y</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∗</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mopen">(</span><span class="mord mathdefault" style="margin-right: 0.03588em;">y</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mclose" style="color: red;">)</span></span></span></span></span></li>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mstyle mathcolor="red"><mo stretchy="false">(</mo></mstyle><mi>a</mi><mo>&lt;</mo><mi>b</mi><mstyle mathcolor="red"><mo stretchy="false">)</mo></mstyle><mtext>&nbsp;</mtext><mi>a</mi><mi>n</mi><mi>d</mi><mtext>&nbsp;</mtext><mstyle mathcolor="red"><mo stretchy="false">(</mo></mstyle><mi>b</mi><mo>&gt;</mo><mo>=</mo><mn>1</mn><mstyle mathcolor="red"><mo stretchy="false">)</mo></mstyle></mrow><annotation encoding="application/x-tex">\textcolor{red}{(}a &lt; b\textcolor{red}{)} \space and \space \textcolor{red}{(}b &gt;= 1\textcolor{red}{)}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mopen" style="color: red;">(</span><span class="mord mathdefault">a</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&lt;</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord mathdefault">b</span><span class="mclose" style="color: red;">)</span><span class="mspace">&nbsp;</span><span class="mord mathdefault">a</span><span class="mord mathdefault">n</span><span class="mord mathdefault">d</span><span class="mspace">&nbsp;</span><span class="mopen" style="color: red;">(</span><span class="mord mathdefault">b</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&gt;</span></span><span class="base"><span class="strut" style="height: 0.36687em; vertical-align: 0em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">1</span><span class="mclose" style="color: red;">)</span></span></span></span></span></li>
</ol>
</li>
<li>
<p>При выполнении арифметических операций над числами различных типов автоматически осуществляется <strong>неявное преобразование:</strong></p>
<ul>
<li>целого и вещественного типов – к вещественному,</li>
<li>с разными интервалами представлений – к типу с большим интервалом.</li>
</ul>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
    k<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a <span class="token operator">/</span> k<span class="token punctuation">;</span>  <span class="token comment">// число k преобразуется к типу Single</span>
</code></pre>
</li>
<li>
<p>При сравнении вещественных чисел из-за их неточного представления проверку равенства и неравенства следует осуществлять <strong>с явным указанием допуска</strong>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    x<span class="token punctuation">,</span> y<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
x <span class="token operator">&lt;&gt;</span> y  <span class="token operator">=</span><span class="token operator">=</span><span class="token operator">&gt;</span>  abs<span class="token punctuation">(</span>x <span class="token operator">-</span> y<span class="token punctuation">)</span> <span class="token operator">&gt;</span> <span class="token number">1e-10</span>  
x <span class="token operator">=</span> y   <span class="token operator">=</span><span class="token operator">=</span><span class="token operator">&gt;</span>  abs<span class="token punctuation">(</span>x <span class="token operator">-</span> y<span class="token punctuation">)</span> <span class="token operator">&lt;</span> <span class="token number">1e-10</span>  
</code></pre>
</li>
</ol>
<h3 id="оператор-присваивания-">Оператор присваивания <code>:=</code></h3>
<p>Используется для изменения значений переменных.<br>
Формат: <code>&lt;идентификатор_переменной&gt; := &lt;выражение&gt;;</code></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    v<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
    a<span class="token punctuation">,</span> b<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
    a <span class="token operator">:=</span> v <span class="token operator">*</span> b <span class="token operator">/</span> <span class="token number">2.0</span><span class="token punctuation">;</span>
</code></pre>
<p>Корректное выполнение оператора предполагает, что результат вычисления и переменная правой части <strong>одного типа</strong> или <strong>совместимы по типу</strong>.</p>
<p>По правилам <strong>совместимы</strong>:</p>
<ol>
<li>все целые типы между собой;</li>
<li>все вещественные типы между собой;</li>
<li>отрезок базового типа и базовый тип;</li>
<li>два отрезка одного и того же базового типа;</li>
<li>символ и строка.</li>
</ol>
<h3 id="неявное-преобразование-типов">Неявное преобразование типов</h3>
<p>Если типы результата и переменной не совпадают, но совместимы, то при выполнении присваивания выполняется <strong>неявное автоматическое преобразование</strong>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    l<span class="token punctuation">:</span> LongInt<span class="token punctuation">;</span> 
    e<span class="token punctuation">,</span> x<span class="token punctuation">:</span> Extended<span class="token punctuation">;</span> 
    i<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span> 
    r<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
<span class="token comment">{...}</span>
r <span class="token operator">:=</span> i <span class="token operator">*</span> e <span class="token operator">/</span> <span class="token punctuation">(</span>x <span class="token operator">+</span> l<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// тип результата выражения `i * e / (x + l)` - Extended,</span>
<span class="token comment">// но так как тип переменной `r` - Single, то результат автоматически преобразуется в Single.</span>
</code></pre>
<!--- ??? &#1091; &#1084;&#1077;&#1085;&#1103; &#1085;&#1077; &#1087;&#1086;&#1083;&#1091;&#1095;&#1080;&#1083;&#1086;&#1089;&#1100; &#1085;&#1080;&#1082;&#1072;&#1082; &#1074;&#1099;&#1079;&#1074;&#1072;&#1090;&#1100; &#1082;&#1072;&#1082;&#1091;&#1102;-&#1083;&#1102;&#1073;&#1086; &#1086;&#1096;&#1080;&#1073;&#1082;&#1091; &#1087;&#1088;&#1086; &#1087;&#1077;&#1088;&#1077;&#1087;&#1086;&#1083;&#1085;&#1077;&#1085;&#1080;&#1077; &#1087;&#1088;&#1080; &#1088;&#1072;&#1073;&#1086;&#1090;&#1077; &#1089; &#1074;&#1077;&#1097;&#1077;&#1089;&#1090;&#1074;&#1077;&#1085;&#1085;&#1099;&#1084;&#1080; &#1090;&#1080;&#1087;&#1072;&#1084;&#1080; -->
<p><s>Если результат не умещается в разрядную сетку переменной, то автоматически генерируется ошибка «<em>Переполнение разрядной сетки</em>».</s></p>
<p><s><strong>Исключение!</strong> Для получения ошибки переполнения при работе с целыми числами необходимо установить опции  компилятора <code>Overflow checking {$Q+}</code> и <code>Range checking {$R+}</code>.</s></p>
<blockquote>
<p>Здесь что-то странное. Немного протестировав, у меня получилось так:</p>
</blockquote>
<ul>
<li>
<p>При <code>Overflow checking {$Q+}</code>: если в результате каких-либо арифметических действий или присвоении произойдёт переполнение целочисленного типа, то вызывается ошибка.</p>
</li>
<li>
<p>При <code>Range checking {$R+}</code>: если при присвоении произойдёт переполнение целочисленного типа, то вызывается ошибка.</p>
</li>
</ul>
<h3 id="явное-преобразование-типов">Явное преобразование типов</h3>
<p>Для несовместимых типов результата и переменной, в которую его необходимо занести, при выполнении присваивания  необходимо <strong>явное преобразование типов</strong>, например, посредством специальных функций:</p>
<ul>
<li><code>trunc(x: float): int</code> или <code>int(x: float): int</code>  – преобразует вещественное число в целое, отбрасывая дробную часть.</li>
<li><code>round(x: float): int</code> – округляет вещественное число до целого по правилам арифметики.</li>
<li><code>ord(c: ordinal): int</code> – преобразует значение в его номер.</li>
<li><code>chr(x: int): Char</code> – преобразует номер символа в символ.</li>
</ul>
<h2 id="условный-оператор----оператор-условной-передачи-управления----if-...-else">Условный оператор – оператор условной передачи управления – <code>if ... else</code></h2>
<p>Оператор условной передачи управления используется при обработке вариантов вычислений и реализует конструкцию ветвления.</p>
<p>Формат: <code>if &lt;логическое_выражение&gt; then &lt;оператор&gt; [else &lt;оператор&gt;];</code></p>
<p><em>Оператором</em> может быть как простой оператор, так и составной оператор (блок операторов в операторных скобках <code>begin...end</code>)</p>
<h2 id="оператор-выбора----case">Оператор выбора – <code>case</code></h2>
<p>Оператор позволяет программировать несколько вариантов решения.</p>
<p>Формат:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">case</span> <span class="token operator">&lt;</span>выражение<span class="token operator">&gt;</span> <span class="token keyword">of</span>
    <span class="token operator">&lt;</span>константа<span class="token operator">/</span>диапазон<span class="token operator">&gt;</span><span class="token punctuation">:</span> <span class="token operator">&lt;</span>оператор<span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">[</span><span class="token operator">&lt;</span>константа<span class="token operator">/</span>диапазон<span class="token operator">&gt;</span><span class="token punctuation">:</span> <span class="token operator">&lt;</span>оператор<span class="token operator">&gt;</span><span class="token punctuation">;</span> <span class="token operator">..</span><span class="token punctuation">.</span><span class="token punctuation">]</span>
    <span class="token punctuation">[</span><span class="token keyword">else</span> <span class="token operator">&lt;</span>оператор<span class="token operator">&gt;</span><span class="token punctuation">;</span><span class="token punctuation">]</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<p>Пример:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">case</span> <span class="token number">1</span> <span class="token operator">+</span> <span class="token number">2</span> <span class="token operator">*</span> j <span class="token keyword">of</span>
    <span class="token number">3</span><span class="token punctuation">:</span>         z<span class="token operator">:=</span>sin<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token number">-1</span><span class="token operator">..</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">10</span><span class="token punctuation">:</span> z<span class="token operator">:=</span>cos<span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">else</span>       z<span class="token operator">:=</span><span class="token number">0</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="операторы-циклов-delphi-pascal">Операторы циклов Delphi Pascal</h2>
<h3 id="операторы-организации-циклов">Операторы организации циклов</h3>
<ul>
<li>Циклы:
<ul>
<li>Счётные (<code>for-loop</code>).</li>
<li>Итерационные (<code>while-do</code>, <code>repeat-until</code>).</li>
<li>Поисковые.</li>
</ul>
</li>
</ul>
<p><strong>Cчетный цикл</strong> – цикл, количество повторений которого известно или можно посчитать. Выход из такого цикла программируется по счетчику.</p>
<p><strong>Итерационный цикл</strong> – цикл, количество повторений которого неизвестно или считается неизвестным при построении цикла. Выход из цикла программируется по выполнению или нарушению условия.</p>
<p><strong>Поисковый цикл</strong> имеет два выхода: <em>нашли</em> и <em>перебрали все и не нашли</em>.</p>
<hr>
<h3 id="счётный-цикл-for-loop">Счётный цикл <code>for-loop</code></h3>
<p>Блок-схема: <img src="https://i.imgur.com/7Cx0LVo.png" alt="for-loop-diagramm"></p>
<p>Выполняется конкретное количество раз.</p>
<p>Формат:<br>
<code>for &lt;переменная-счётчик&gt; := &lt;значение_от&gt; to &lt;значение_по&gt; do &lt;оператор&gt;;</code> (если <em>от</em> &lt; <em>по</em>)<br>
<code>for &lt;переменная-счётчик&gt; := &lt;значение_от&gt; downto &lt;значение_по&gt; do &lt;оператор&gt;;</code> (если <em>от</em> &gt; <em>по</em>)</p>
<p>Пример:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span> i<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
<span class="token keyword">for</span> i <span class="token operator">:=</span> <span class="token number">1</span> <span class="token keyword">to</span> <span class="token number">10</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        x <span class="token operator">:=</span> x <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">;</span>
        e <span class="token operator">:=</span> e <span class="token operator">/</span> <span class="token number">10</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h3 id="цикл-пока-while-do">Цикл-пока <code>while-do</code></h3>
<p>Блок-схема:<br>
<img src="https://i.imgur.com/LdGMa6z.png" alt="while-do-diagramm"></p>
<p>Выполняется, пока <em>условие <strong>истинно</strong></em>.</p>
<p>Формат: <code>while &lt;логическое_выражение&gt; do &lt;оператор&gt;;</code></p>
<p>Пример:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">while</span> abs<span class="token punctuation">(</span>e<span class="token punctuation">)</span> <span class="token operator">&gt;=</span> <span class="token number">1e-5</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        x <span class="token operator">:=</span> x <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">;</span>
        e <span class="token operator">:=</span> e <span class="token operator">/</span> <span class="token number">10</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h3 id="цикл-до-repeat-until">Цикл-до <code>repeat-until</code></h3>
<p>Блок-схема:<br>
<img src="https://i.imgur.com/92dV0CE.png" alt="repeat-until-diagramm"></p>
<p>Выполняется, до тех пор, пока <em>условие не станет <strong>истинно</strong></em> (то есть пока условие ложно).</p>
<p>Формат:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">repeat</span> 
    <span class="token operator">&lt;</span>оператор<span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">[</span><span class="token operator">&lt;</span>оператор<span class="token operator">&gt;</span><span class="token punctuation">;</span> <span class="token operator">..</span><span class="token punctuation">.</span><span class="token punctuation">]</span>
<span class="token keyword">until</span> <span class="token operator">&lt;</span>логическое выражение<span class="token operator">&gt;</span><span class="token punctuation">;</span>
</code></pre>
<p>Пример:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">repeat</span>
    x <span class="token operator">:=</span> x <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">;</span>
	e <span class="token operator">:=</span> e <span class="token operator">/</span> <span class="token number">10</span><span class="token punctuation">;</span>
<span class="token keyword">until</span> abs<span class="token punctuation">(</span>e<span class="token punctuation">)</span> <span class="token operator">&lt;</span> <span class="token number">1e-5</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="поисковый-цикл.-неструктурная-и-структурная-реализации-поискового-цикла.">Поисковый цикл. Неструктурная и структурная реализации поискового цикла.</h2>
<blockquote>
<p>В лекциях конкретного мало было, поэтому попробую расписать самостоятельно …</p>
</blockquote>
<!--- &#1053;&#1072; &#1089;&#1072;&#1084;&#1086;&#1084; &#1076;&#1077;&#1083;&#1077;, &#1082;&#1090;&#1086; &#1074;&#1086;&#1086;&#1073;&#1097;&#1077; &#1074;&#1099;&#1076;&#1077;&#1083;&#1103;&#1077;&#1090; &#1087;&#1086;&#1080;&#1089;&#1082;&#1086;&#1074;&#1099;&#1077; &#1094;&#1080;&#1082;&#1083;&#1099; &#1082;&#1072;&#1082; &#1086;&#1090;&#1076;&#1077;&#1083;&#1100;&#1085;&#1099;&#1077;? &#10;&#1069;&#1090;&#1086; &#1078;&#1077; &#1087;&#1088;&#1086;&#1089;&#1090;&#1086; &#1085;&#1077;&#1084;&#1085;&#1086;&#1075;&#1086; &#1086;&#1089;&#1086;&#1073;&#1099;&#1081; &#1080;&#1090;&#1077;&#1088;&#1072;&#1094;&#1080;&#1086;&#1085;&#1085;&#1099;&#1081; &#1094;&#1080;&#1082;&#1083; (&#1089; &#1092;&#1083;&#1072;&#1075;&#1086;&#1084;, &#1077;&#1089;&#1083;&#1080; &#1085;&#1091;&#1078;&#1085;&#1086;)  --> 
<p><strong>Поисковый цикл</strong> – особый вид цикла, который имеет два случая выхода:</p>
<ol>
<li>нашли,</li>
<li>перебрали все элементы, но не нашли.</li>
</ol>
<p>Существуют <strong>структурная</strong> (приведённая к обычному итерационному циклу) и <strong>неструктурная</strong> реализации данного цикла. <!--- &#1061;&#1086;&#1090;&#1103; &#1103; &#1085;&#1077; &#1091;&#1074;&#1077;&#1088;&#1077;&#1085;, &#1095;&#1090;&#1086; &#1101;&#1090;&#1086; &#1087;&#1088;&#1072;&#1074;&#1080;&#1083;&#1100;&#1085;&#1086;--></p>
<ul>
<li><em>Задача для примера</em>:
<ul>
<li>определить сумму ряда <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>S</mi><mo>=</mo><mn>1</mn><mo>−</mo><mstyle displaystyle="true" scriptlevel="0"><mfrac><mn>1</mn><mi>x</mi></mfrac></mstyle><mo>+</mo><mstyle displaystyle="true" scriptlevel="0"><mfrac><mn>1</mn><msup><mi>x</mi><mn>2</mn></msup></mfrac></mstyle><mo>−</mo><mstyle displaystyle="true" scriptlevel="0"><mfrac><mn>1</mn><msup><mi>x</mi><mn>3</mn></msup></mfrac></mstyle><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi></mrow><annotation encoding="application/x-tex">S = 1 - \dfrac{1}{x} + \dfrac{1}{x^2} - \dfrac{1}{x^3} +...</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05764em;">S</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">1</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 2.00744em; vertical-align: -0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.32144em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord mathdefault">x</span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord">1</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.686em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 2.00744em; vertical-align: -0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.32144em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord"><span class="mord mathdefault">x</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.740108em;"><span class="" style="top: -2.989em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord">1</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.686em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 2.00744em; vertical-align: -0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.32144em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord"><span class="mord mathdefault">x</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.740108em;"><span class="" style="top: -2.989em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">3</span></span></span></span></span></span></span></span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord">1</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.686em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.10556em; vertical-align: 0em;"></span><span class="mord">.</span><span class="mord">.</span><span class="mord">.</span></span></span></span></span> с заданной точностью <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>ε</mi></mrow><annotation encoding="application/x-tex">\varepsilon</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.43056em; vertical-align: 0em;"></span><span class="mord mathdefault">ε</span></span></span></span></span>.<br>
(Рекуррентная формула последовательности: <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi>R</mi><mn>1</mn></msub><mo>=</mo><mn>1</mn><mo separator="true">;</mo><msub><mi>R</mi><mi>n</mi></msub><mo>=</mo><mo>−</mo><mstyle displaystyle="true" scriptlevel="0"><mfrac><msub><mi>R</mi><mrow><mi>n</mi><mo>−</mo><mn>1</mn></mrow></msub><mi>x</mi></mfrac></mstyle></mrow><annotation encoding="application/x-tex">R_1 = 1; R_n = -\dfrac{R_{n-1}}{x}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord mathdefault" style="margin-right: 0.00773em;">R</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.301108em;"><span class="" style="top: -2.55em; margin-left: -0.00773em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">1</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.87777em; vertical-align: -0.19444em;"></span><span class="mord">1</span><span class="mpunct">;</span><span class="mspace" style="margin-right: 0.166667em;"></span><span class="mord"><span class="mord mathdefault" style="margin-right: 0.00773em;">R</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: -0.00773em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathdefault mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 2.04633em; vertical-align: -0.686em;"></span><span class="mord">−</span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.36033em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord mathdefault">x</span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord"><span class="mord mathdefault" style="margin-right: 0.00773em;">R</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.301108em;"><span class="" style="top: -2.55em; margin-left: -0.00773em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathdefault mtight">n</span><span class="mbin mtight">−</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.208331em;"><span class=""></span></span></span></span></span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.686em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span></span></span></span>).</li>
</ul>
</li>
</ul>
<h3 id="неструктурная-реализация-поискового-цикла">Неструктурная реализация поискового цикла</h3>
<p>Примерный общий вид неструктурной реализации поискового цикла:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    found<span class="token punctuation">:</span> boolean<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
found <span class="token operator">:=</span> <span class="token keyword">false</span><span class="token punctuation">;</span>
<span class="token keyword">while</span> <span class="token keyword">true</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        <span class="token comment">{операторы, выполняемые до проверки}</span>
        
        <span class="token keyword">if</span> <span class="token comment">{проверка на то, нашли ли необходимое}</span> <span class="token keyword">then</span> <span class="token keyword">begin</span>
                found <span class="token operator">:=</span> <span class="token keyword">true</span><span class="token punctuation">;</span>  <span class="token comment">// ставим флаг, что нашли</span>
                <span class="token keyword">break</span><span class="token punctuation">;</span>          <span class="token comment">// прерываем цикл</span>
            <span class="token keyword">end</span><span class="token punctuation">;</span>
        <span class="token keyword">if</span> <span class="token comment">{проверка на то, не перебрали ли всё}</span> <span class="token keyword">then</span>
            <span class="token keyword">break</span><span class="token punctuation">;</span>
        
        <span class="token comment">{операторы, выполняемые после проверки}</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> found <span class="token keyword">then</span>
    <span class="token comment">{нашли}</span>
<span class="token keyword">else</span>
    <span class="token comment">{не нашли}</span>
</code></pre>
<ul>
<li>
<p><em>Решение примера</em>:</p>
<ul>
<li>
<p>Блок-схема:<br>
<img src="https://i.imgur.com/8lmr4ml.png" alt="non-struct-search-loop"></p>
</li>
<li>
<p>Код:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    x<span class="token punctuation">,</span> eps<span class="token punctuation">,</span> s<span class="token punctuation">,</span> r<span class="token punctuation">:</span> Double<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    readLn<span class="token punctuation">(</span>x<span class="token punctuation">,</span> eps<span class="token punctuation">)</span><span class="token punctuation">;</span>
    s <span class="token operator">:=</span> <span class="token number">0</span><span class="token punctuation">;</span>
    r <span class="token operator">:=</span> <span class="token number">1</span><span class="token punctuation">;</span>
    <span class="token keyword">while</span> <span class="token keyword">true</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        s <span class="token operator">:=</span> s <span class="token operator">+</span> r<span class="token punctuation">;</span>
        <span class="token keyword">if</span> abs<span class="token punctuation">(</span>r<span class="token punctuation">)</span> <span class="token operator">&lt;=</span> eps <span class="token keyword">then</span>
            <span class="token keyword">break</span><span class="token punctuation">;</span>
        r <span class="token operator">:=</span> <span class="token operator">-</span>r <span class="token operator">/</span> x<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>x<span class="token punctuation">,</span> <span class="token string">' '</span><span class="token punctuation">,</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<h3 id="структурная-реализация-поискового-цикла-№1-через-while-do">Структурная реализация поискового цикла №1 (через <code>while-do</code>)</h3>
<p>Примерный общий вид структурной реализации поискового цикла:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    found<span class="token punctuation">:</span> boolean<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
<span class="token comment">{операторы, выполняемые до проверки}</span>
found <span class="token operator">:=</span> <span class="token comment">{нашли ли необходимое}</span><span class="token punctuation">;</span>
<span class="token keyword">while</span> <span class="token operator">not</span> <span class="token punctuation">(</span>found<span class="token punctuation">)</span> <span class="token operator">and</span> <span class="token operator">not</span> <span class="token punctuation">(</span><span class="token comment">{не перебрали ли всё}</span><span class="token punctuation">)</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        <span class="token comment">{операторы, выполняемые после проверки}</span>
        <span class="token comment">{операторы, выполняемые до проверки}</span>
        <span class="token keyword">if</span> <span class="token comment">{нашли ли необходимое}</span> <span class="token keyword">then</span>
                found <span class="token operator">:=</span> <span class="token keyword">true</span><span class="token punctuation">;</span>  <span class="token comment">// ставим флаг, что нашли</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> found <span class="token keyword">then</span>
    <span class="token comment">{нашли}</span>
<span class="token keyword">else</span>
    <span class="token comment">{не нашли}</span>
</code></pre>
<ul>
<li>
<p><em>Решение примера</em>:</p>
<ul>
<li>
<p>Блок-схема:<br>
<img src="https://i.imgur.com/NaYb68j.png" alt="struct-1-search-loop"></p>
</li>
<li>
<p>Код:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    x<span class="token punctuation">,</span> eps<span class="token punctuation">,</span> s<span class="token punctuation">,</span> r<span class="token punctuation">:</span> Double<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    readLn<span class="token punctuation">(</span>x<span class="token punctuation">,</span> eps<span class="token punctuation">)</span><span class="token punctuation">;</span>
    s <span class="token operator">:=</span> <span class="token number">0</span><span class="token punctuation">;</span>
    r <span class="token operator">:=</span> <span class="token number">1</span><span class="token punctuation">;</span>
    s <span class="token operator">:=</span> s <span class="token operator">+</span> r<span class="token punctuation">;</span>
    <span class="token keyword">while</span> abs<span class="token punctuation">(</span>r<span class="token punctuation">)</span> <span class="token operator">&gt;</span> eps <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        r <span class="token operator">:=</span> <span class="token operator">-</span>r <span class="token operator">/</span> x<span class="token punctuation">;</span>
        s <span class="token operator">:=</span> s <span class="token operator">+</span> r<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>x<span class="token punctuation">,</span> <span class="token string">' '</span><span class="token punctuation">,</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<h3 id="структурная-реализация-поискового-цикла-№2-через-repeat-until">Структурная реализация поискового цикла №2 (через <code>repeat-until</code>)</h3>
<p>Примерный общий вид структурной реализации поискового цикла:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    found<span class="token punctuation">:</span> boolean<span class="token punctuation">;</span>
<span class="token comment">{...}</span>

found <span class="token operator">:=</span> <span class="token keyword">false</span><span class="token punctuation">;</span>
<span class="token keyword">repeat</span>
    <span class="token comment">{операторы, выполняемые после проверки}</span>
    <span class="token comment">{операторы, выполняемые до проверки}</span> <span class="token comment">// !!! </span>
                                         <span class="token comment">// тут отличается от первой структурной реализации:</span>
                  <span class="token comment">// выполнится в первый раз в любой случае, в отличие от первой реализации!</span>
    <span class="token keyword">if</span> <span class="token comment">{нашли ли необходимое}</span> <span class="token keyword">then</span>
        found <span class="token operator">:=</span> <span class="token keyword">true</span><span class="token punctuation">;</span>                   <span class="token comment">// ставим флаг, что нашли</span>
<span class="token keyword">until</span> <span class="token punctuation">(</span>found<span class="token punctuation">)</span> <span class="token operator">or</span> <span class="token punctuation">(</span><span class="token comment">{всё перебрали}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> found <span class="token keyword">then</span>
    <span class="token comment">{нашли}</span>
<span class="token keyword">else</span>
    <span class="token comment">{не нашли}</span>
</code></pre>
<ul>
<li>
<p><em>Решение примера</em>:</p>
<ul>
<li>
<p>Блок-схема:<br>
<img src="https://i.imgur.com/9UR8Oli.png" alt="struct-2-search-loop"></p>
</li>
<li>
<p>Код:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    x<span class="token punctuation">,</span> eps<span class="token punctuation">,</span> s<span class="token punctuation">,</span> r<span class="token punctuation">:</span> Double<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    readLn<span class="token punctuation">(</span>x<span class="token punctuation">,</span> eps<span class="token punctuation">)</span><span class="token punctuation">;</span>
    s <span class="token operator">:=</span> <span class="token number">0</span><span class="token punctuation">;</span>
    r <span class="token operator">:=</span> <span class="token number">1</span><span class="token punctuation">;</span>
    <span class="token keyword">repeat</span>
        s <span class="token operator">:=</span> s <span class="token operator">+</span> r<span class="token punctuation">;</span>
        r <span class="token operator">:=</span> <span class="token operator">-</span>r <span class="token operator">/</span> x<span class="token punctuation">;</span>
    <span class="token keyword">until</span> abs<span class="token punctuation">(</span>r<span class="token punctuation">)</span> <span class="token operator">&lt;=</span> eps<span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>x<span class="token punctuation">,</span> <span class="token string">' '</span><span class="token punctuation">,</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<hr>
<blockquote>
<p>Я мог что-то неправильно понять из того, что является структурными и неструктурным поисковым циклом, поэтому советую проверить самому.</p>
</blockquote>
<hr>
<h2 id="массивы-delphi-pascal">Массивы Delphi Pascal</h2>
<p><strong>Массив</strong> – это <em>упорядоченная</em> совокупность <em>однотипных</em> данных. Каждому элементу массива соответствует один или несколько <em>индексов порядкового типа</em>, определяющих положение элемента в массиве.</p>
<p>Формат: <code>array [&lt;типы индекса&gt;] of &lt;тип элемента&gt;</code> (<em>типы индекса перечисляются через запятую, если их больше одного</em>).</p>
<p>Количество типов индексов задает <strong>размерность</strong> массива.<br>
<strong>Тип индекса</strong> –  порядковый – определяет доступ к элементу.<br>
<strong>Тип элемента</strong> – любой кроме файла, в том числе массивы, строки и т.п.<br>
Массив в памяти не может занимать более 2 Гб (из-за технических ограничений).</p>
<blockquote>
<p>Кажется, потому, что это связано с <a href="https://superuser.com/questions/1163749/why-do-32-bit-processes-have-a-2-gb-ram-limit">технической проблемой выделить для 32-битной системы один кусок памяти больше, чем для 32-битного указателя</a>, то есть <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mn>32</mn><mtext>&nbsp;</mtext><mi mathvariant="normal">б</mi><mi mathvariant="normal">и</mi><mi mathvariant="normal">т</mi><mi mathvariant="normal">а</mi><mo>⇒</mo><mi mathvariant="normal">м</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">к</mi><mi mathvariant="normal">с</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">р</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">з</mi><mi mathvariant="normal">м</mi><mi mathvariant="normal">е</mi><mi mathvariant="normal">р</mi><mtext>&nbsp;</mtext><msup><mn>2</mn><mn>32</mn></msup><mo>=</mo><mn>4294967296</mn></mrow><annotation encoding="application/x-tex">32\spaceбита \Rightarrow макс. размер\space 2^{32}  = 4294967296</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.69444em; vertical-align: 0em;"></span><span class="mord">3</span><span class="mord">2</span><span class="mspace">&nbsp;</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">и</span><span class="mord cyrillic_fallback">т</span><span class="mord cyrillic_fallback">а</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">⇒</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 1.00855em; vertical-align: -0.19444em;"></span><span class="mord cyrillic_fallback">м</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">к</span><span class="mord cyrillic_fallback">с</span><span class="mord">.</span><span class="mord cyrillic_fallback">р</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">з</span><span class="mord cyrillic_fallback">м</span><span class="mord cyrillic_fallback">е</span><span class="mord cyrillic_fallback">р</span><span class="mspace">&nbsp;</span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">2</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">4</span><span class="mord">2</span><span class="mord">9</span><span class="mord">4</span><span class="mord">9</span><span class="mord">6</span><span class="mord">7</span><span class="mord">2</span><span class="mord">9</span><span class="mord">6</span></span></span></span></span> для одного сегмента, но половина предназначена для системы. Поэтому в языке Pascal установлено жёсткое ограничение на 2 ГБ памяти.</p>
</blockquote>
<p>Примеры объявления массива:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span> 
    mas <span class="token operator">=</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">10</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Integer<span class="token punctuation">;</span>

<span class="token keyword">var</span> 
    a<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Integer<span class="token punctuation">;</span>
    с<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span>’A’<span class="token operator">..</span>’C’<span class="token punctuation">,</span> <span class="token number">-5</span><span class="token operator">..</span><span class="token number">-3</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Byte<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span>Byte<span class="token punctuation">]</span> <span class="token keyword">of</span> Char<span class="token punctuation">;</span>
</code></pre>
<p>Инициализация массива при объявлении:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Real <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">-3.6</span><span class="token punctuation">,</span> <span class="token number">7.8</span><span class="token punctuation">,</span> <span class="token number">3.789</span><span class="token punctuation">,</span> <span class="token number">5.0</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span>Boolean<span class="token punctuation">,</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Real <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">-3.6</span><span class="token punctuation">,</span> <span class="token number">7.8</span><span class="token punctuation">,</span> <span class="token number">3.789</span><span class="token punctuation">,</span> <span class="token number">5.0</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
                                       <span class="token punctuation">(</span><span class="token number">6.1</span><span class="token punctuation">,</span> <span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">-4.56</span><span class="token punctuation">,</span> <span class="token number">8.9</span><span class="token punctuation">,</span> <span class="token number">3.0</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="операции-над-массивами">Операции над массивами</h3>
<ol>
<li>Операция  присваивания (только для массивов одного типа):<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">,</span> b<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span>Boolean<span class="token punctuation">]</span> <span class="token keyword">of</span> Real<span class="token punctuation">;</span>
    c<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span>Boolean<span class="token punctuation">]</span> <span class="token keyword">of</span> Real<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
b <span class="token operator">:=</span> a<span class="token punctuation">;</span>
c <span class="token operator">:=</span> a<span class="token punctuation">;</span> <span class="token comment">// ОШИБКА! Их типы считаются разными, так как объявлены раздельно, </span>
        <span class="token comment">//         несмотря на то, что по факту они идентичны!</span>
</code></pre>
</li>
<li>Доступ к элементу массива (<strong>прямой</strong> и <strong>косвенный доступ</strong>):<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span>Char<span class="token punctuation">,</span> Boolean<span class="token punctuation">]</span> <span class="token keyword">of</span> Real<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a<span class="token punctuation">[</span>’A’<span class="token punctuation">,</span> <span class="token keyword">true</span><span class="token punctuation">]</span> <span class="token operator">:=</span> <span class="token number">5.1</span><span class="token punctuation">;</span> <span class="token comment">{прямой доступ}</span>
<span class="token comment">{...}</span>
ch <span class="token operator">:=</span> ’B’<span class="token punctuation">;</span> 
b <span class="token operator">:=</span> <span class="token keyword">false</span><span class="token punctuation">;</span>
a<span class="token punctuation">[</span>ch<span class="token punctuation">,</span> b<span class="token punctuation">]</span> <span class="token operator">:=</span> <span class="token number">3</span><span class="token punctuation">;</span> <span class="token comment">{косвенный доступ: значения индексов находятся в переменных}</span>
</code></pre>
</li>
<li>Ввод/вывод массивов осуществляется поэлементно:<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Real<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
<span class="token keyword">for</span> i <span class="token operator">:=</span> <span class="token number">1</span> <span class="token keyword">to</span> <span class="token number">5</span> <span class="token keyword">do</span>
    <span class="token keyword">read</span><span class="token punctuation">(</span>a<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
readLn<span class="token punctuation">;</span> <span class="token comment">{обрабатывает последний Enter}</span>
</code></pre>
Вывод матрицы:<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">7</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Real<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
<span class="token keyword">for</span> i <span class="token operator">:=</span> <span class="token number">1</span> <span class="token keyword">to</span> <span class="token number">5</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        <span class="token keyword">for</span> j <span class="token operator">:=</span> <span class="token number">1</span> <span class="token keyword">to</span> <span class="token number">7</span> <span class="token keyword">do</span>
            <span class="token keyword">write</span><span class="token punctuation">(</span>a<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">[</span>j<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>   <span class="token comment">// также можно a[i, j]</span>
                 <span class="token comment">{a[i][1], a[i][2], a[i][3], a[i][4], a[i][5], a[i][6], a[i][7]}</span>
        writeLn<span class="token punctuation">;</span>  <span class="token comment">{переход на следующую строку}</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ol>
<h2 id="строки-delphi-pascal">Строки Delphi Pascal</h2>
<p><strong>Строка</strong> – последовательность символов (<em>фактически, массив символов</em>).</p>
<p>Формат (обычно): <code>string</code> или <code>string[&lt;размер&gt;]</code>, где <em>размер</em> – максимальная длина строки.</p>
<p>Внутренний формат:<br>
<img src="https://i.imgur.com/Q4pLScN.png" alt="Internal string format"></p>
<hr>
<blockquote>
<h3 id="здесь-нужно-сделать-небольшое-отступление-насчёт-длинных-строк">Здесь нужно сделать небольшое отступление насчёт длинных строк</h3>
</blockquote>
<p>С более новых версий языка <em>Pascal</em> существует несколько видов строк, поэтому тип <code>string</code> зависит от платформы.</p>
<p>В <em>Delphi Pascal</em> (с версии <em>Delphi 2009</em>):</p>

<table>
<thead>
<tr>
<th>Тип</th>
<th>Максимальная длина</th>
<th>Размер</th>
<th>Размер символа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="http://docwiki.embarcadero.com/Libraries/Sydney/en/System.ShortString" title="lib en:System.ShortString"><code>ShortString</code></a></td>
<td>255</td>
<td>256 байт</td>
<td>1 байт</td>
<td>Является псевдонимом для <code>string[255]</code> (с фиксированной длиной)</td>
</tr>
<tr>
<td><a href="http://docwiki.embarcadero.com/Libraries/Sydney/en/System.AnsiString" title="lib en:System.AnsiString"><code>AnsiString</code></a></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>≈</mo><msup><mn>2</mn><mn>31</mn></msup></mrow><annotation encoding="application/x-tex">\approx2^{31}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.48312em; vertical-align: 0em;"></span><span class="mrel">≈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span></span></span></span></span>*</td>
<td>4 Б – 2 ГБ*</td>
<td>1 байт</td>
<td>Длинные, динамические строки, но с однобайтовыми символами</td>
</tr>
<tr>
<td><a href="http://docwiki.embarcadero.com/Libraries/Sydney/en/System.UnicodeString" title="lib en:System.UnicodeString"><code>UnicodeString</code></a></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>≈</mo><msup><mn>2</mn><mn>30</mn></msup></mrow><annotation encoding="application/x-tex">\approx2^{30}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.48312em; vertical-align: 0em;"></span><span class="mrel">≈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">0</span></span></span></span></span></span></span></span></span></span></span></span></span>*</td>
<td>4 Б – 2 ГБ*</td>
<td>2 байта</td>
<td>Длинные, динамические строки с двухбайтовыми символами. <strong>В среде разработки <em>RAD Studio</em> <code>string</code> (без размера!) является псевдонимом для <code>UnicodeString</code></strong></td>
</tr>
<tr>
<td><a href="http://docwiki.embarcadero.com/Libraries/Sydney/en/System.WideString" title="lib en:System.WideString"><code>WideString</code></a></td>
<td><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>≈</mo><msup><mn>2</mn><mn>30</mn></msup></mrow><annotation encoding="application/x-tex">\approx2^{30}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.48312em; vertical-align: 0em;"></span><span class="mrel">≈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">0</span></span></span></span></span></span></span></span></span></span></span></span></span>*</td>
<td>4 Б – 2 ГБ*</td>
<td>2 байта</td>
<td><em>Кажется, какой-то старый костыль, который был до <code>UnicodeString</code>. Использовать не рекомендуется</em></td>
</tr>
</tbody>
</table><p>При использовании <code>string[&lt;размер&gt;]</code> используется тип <code>ShortString</code>, но с размером <code>&lt;размер&gt;</code>, то есть строка фиксированной длины, меньшей 256, и символом, размером в 1 байт.<br>
При использовании <code>string</code> (без размера) используется по умолчанию <code>UnicodeString</code>.</p>
<p>* Ограничение в 2 ГБ по тем же причинам, что и с массивами.</p>
<p>Также включить или отключить (<em>кажется, только для старых версий</em>) переопределение <code>string</code> на длинные строки можно с помощью опций компилятора:</p>

<table>
<thead>
<tr>
<th>Включить</th>
<th>Выключить</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>{$H+}</code></td>
<td><code>{$H-}</code></td>
</tr>
<tr>
<td><code>{$LONGSTRINGS ON}</code></td>
<td><code>{$LONGSTRINGS OFF}</code></td>
</tr>
</tbody>
</table><!--- &#1042;&#1086;&#1086;&#1073;&#1097;&#1077; &#1082;&#1072;&#1082;-&#1090;&#1086; &#1085;&#1077; &#1091;&#1074;&#1077;&#1088;&#1077;&#1085; &#1085;&#1072;&#1089;&#1095;&#1105;&#1090; &#1074;&#1089;&#1077;&#1093; &#1101;&#1090;&#1080;&#1093; &#1088;&#1072;&#1079;&#1083;&#1080;&#1095;&#1085;&#1099;&#1093; &#1089;&#1090;&#1088;&#1086;&#1082;. &#1052;&#1086;&#1078;&#1077;&#1090;, &#1082;&#1090;&#1086; &#1079;&#1085;&#1072;&#1077;&#1090;, &#1087;&#1086;&#1076;&#1089;&#1082;&#1072;&#1078;&#1077;&#1090;? -->
<h6 id="источник-docwiki.embarcadero.com">Источник: <a href="http://docwiki.embarcadero.com/RADStudio/Sydney/en/String_Types_(Delphi)">docwiki.embarcadero.com</a></h6>
<hr>
<p>Примеры описания строк:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span> 
    s1<span class="token punctuation">,</span> s2<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token number">40</span><span class="token punctuation">]</span><span class="token punctuation">;</span> 
    s3<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    S40 <span class="token operator">=</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token number">40</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    ST <span class="token operator">=</span> <span class="token keyword">string</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    s1<span class="token punctuation">,</span> s2<span class="token punctuation">:</span> S40<span class="token punctuation">;</span>
    s3<span class="token punctuation">:</span> ST<span class="token punctuation">;</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    s<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token number">40</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token string">'String-constant'</span><span class="token punctuation">;</span>
    s1<span class="token punctuation">:</span> <span class="token keyword">string</span> <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="операции-над-строками">Операции над строками</h3>
<ol>
<li>
<p>Присваивание строк:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">s1 <span class="token operator">:=</span> <span class="token string">'ABCD'</span><span class="token punctuation">;</span>
s1 <span class="token operator">:=</span> s2<span class="token punctuation">;</span>
s1 <span class="token operator">:=</span> <span class="token string">'A'</span><span class="token punctuation">;</span>
s1 <span class="token operator">:=</span> <span class="token string">''</span><span class="token punctuation">;</span> <span class="token comment">{пустая строка}</span>
</code></pre>
</li>
<li>
<p>Обращение к элементу:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">s1<span class="token punctuation">[</span><span class="token number">5</span><span class="token punctuation">]</span>  <span class="token comment">{прямое}</span>
s1<span class="token punctuation">[</span>i<span class="token punctuation">]</span>  <span class="token comment">{косвенное}</span>
</code></pre>
</li>
<li>
<p><strong>Конкатенация</strong> (сцепление) строк:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">str <span class="token operator">:=</span> str <span class="token operator">+</span> <span class="token string">'A'</span><span class="token punctuation">;</span>
str <span class="token operator">:=</span> <span class="token string">'A'</span> <span class="token operator">+</span> <span class="token string">'BC'</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Операции отношения</strong> – выполняется попарным сравнением кодов символов, результат определяется по отношению кодов первых различных символов:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">s1 <span class="token operator">:=</span> <span class="token string">'ABCD'</span><span class="token punctuation">;</span> 
s2 <span class="token operator">:=</span> <span class="token string">'ABCA'</span><span class="token punctuation">;</span>
b <span class="token operator">:=</span> s1 <span class="token operator">&gt;</span> s2<span class="token punctuation">;</span>  <span class="token comment">// true, так как 4: 'D' &gt; 'A'</span>
<span class="token string">'T'</span> <span class="token operator">&lt;</span> <span class="token string">'Ta'</span><span class="token punctuation">;</span>    <span class="token comment">// true, так как размер первой строки меньше</span>
</code></pre>
</li>
<li>
<p>Ввод-вывод  строк:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">readLn<span class="token punctuation">(</span>s1<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// Строка вводится до Enter (переноса строки, пропуская сам перенос) </span>
             <span class="token comment">// или максимальной длины</span>
writeLn<span class="token punctuation">(</span>s1<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ol>
<h3 id="стандартные-процедуры-и-функции-для-работы-со-строками">Стандартные процедуры и функции для работы со строками</h3>
<ol>
<li>
<p>Функция <code>length(str: string): word</code> – возвращает длину строки <code>str</code>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">n <span class="token operator">:=</span> length<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>Процедура <code>delete(var str: string; i, k: int)</code> – удаляет <code>k</code> символов строки <code>str</code>, начиная с <code>i</code>-го символа:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">s <span class="token operator">:=</span> <span class="token string">'aabbbbccccc'</span><span class="token punctuation">;</span>
delete<span class="token punctuation">(</span>s<span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// s = 'aaccccc''</span>
</code></pre>
</li>
<li>
<p>Процедура <code>insert(sub: string; var str: string; i: int)</code> – вставляет подстроку <code>sub</code> в строку <code>str</code>, начиная с символа с номером <code>i</code>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">my_string <span class="token operator">:=</span> <span class="token string">'aaacc'</span><span class="token punctuation">;</span>
sub_str <span class="token operator">:=</span> <span class="token string">'bbbb'</span><span class="token punctuation">;</span>
insert<span class="token punctuation">(</span>sub_str<span class="token punctuation">,</span> my_string<span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 'aaabbbbcc'</span>
insert<span class="token punctuation">(</span><span class="token string">'Pas'</span><span class="token punctuation">,</span> my_string<span class="token punctuation">,</span> <span class="token number">6</span><span class="token punctuation">)</span><span class="token punctuation">;</span>    <span class="token comment">// 'aaabbPasbbcc'</span>
</code></pre>
</li>
<li>
<p>Процедура <code>str(x[:w[:d]], var str)</code> – преобразует результат выражения <code>x</code>, в строку <code>str</code>, содержащую запись этого числа в виде последовательности символов (как при выводе):</p>
<pre class=" language-pascal"><code class="prism  language-pascal">x <span class="token operator">:=</span> <span class="token number">-5.67</span><span class="token punctuation">;</span>
str<span class="token punctuation">(</span>x<span class="token punctuation">:</span><span class="token number">7</span><span class="token punctuation">:</span><span class="token number">3</span><span class="token punctuation">,</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// s = ' -5.670'</span>
</code></pre>
</li>
<li>
<p>Процедура <code>val(str, var x, var status_code)</code> – преобразует строку <code>str</code> с записью числа в виде последовательности символов во внутреннее представление целого или вещественного числа и помещает его в переменную <code>x</code>.  В целочисленной переменной <code>status_code</code> процедура возвращает код ошибки:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"> <span class="token keyword">var</span>
    s<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
    a<span class="token punctuation">:</span> real<span class="token punctuation">;</span>
    code<span class="token punctuation">:</span> integer<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
<span class="token keyword">repeat</span>
   <span class="token keyword">write</span><span class="token punctuation">(</span><span class="token string">'Input a: '</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
   readLn<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">;</span>
   val<span class="token punctuation">(</span>s<span class="token punctuation">,</span> a<span class="token punctuation">,</span> code<span class="token punctuation">)</span><span class="token punctuation">;</span>
   <span class="token keyword">if</span> code <span class="token operator">&lt;&gt;</span> <span class="token number">0</span> <span class="token keyword">then</span>
       writeLn<span class="token punctuation">(</span><span class="token string">'Wrong input!'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">until</span> code <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>Функция <code>copy(str: string; i, k: int): string</code> – возвращает фрагмент строки <code>str</code>, длиной <code>k</code> символов, начиная с <code>i</code>-го символа:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">str <span class="token operator">:=</span> <span class="token string">'qqqEEEEEEuuuuu'</span><span class="token punctuation">;</span>
s <span class="token operator">:=</span> copy<span class="token punctuation">(</span>str<span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">6</span><span class="token punctuation">)</span><span class="token punctuation">;</span>    <span class="token comment">// 'EEEEEE'</span>
</code></pre>
</li>
<li>
<p>Функция <code>pos(sub, str: string): int</code> – возвращает номер позиции первого вхождения подстроки <code>sub</code> в строку <code>str</code>. Если вхождение не найдено, то функция возвращает <code>0</code>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">str <span class="token operator">:=</span> <span class="token string">'qqqEEррEEuuuuu'</span><span class="token punctuation">;</span>
i <span class="token operator">:=</span> pos<span class="token punctuation">(</span><span class="token string">'EE'</span><span class="token punctuation">,</span> str<span class="token punctuation">)</span><span class="token punctuation">;</span>      <span class="token comment">// i = 4</span>
j <span class="token operator">:=</span> pos<span class="token punctuation">(</span><span class="token string">'X'</span><span class="token punctuation">,</span> str<span class="token punctuation">)</span><span class="token punctuation">;</span>      <span class="token comment">// j = 4</span>
</code></pre>
</li>
<li>
<p>Функция <code>upCase(c: char): char</code> – возвращает символ, соответствующий символу верхнего регистра для <code>c</code>, если таковой имеется, либо сам символ <code>c</code>, если для него не определен символ верхнего регистра.</p>
</li>
</ol>
<blockquote>
<p>Кажется, противоположной функции <code>downCase</code> или <code>lowerCase</code> нет.</p>
</blockquote>
<h2 id="множества-delphi-pascal">Множества Delphi Pascal</h2>
<p><strong>Множество</strong> – <em>неупорядоченная</em> совокупность <em>неповторяющихся</em> элементов.</p>
<p>Формат: <code>set of &lt;базовый_тип&gt;</code>.<br>
Тип элементов – <em>порядковый</em>, но количество элементов <strong>не должно превышать 256</strong>. (То есть нельзя использовать <code>Word</code>, <code>Integer</code>, <code>UInt64</code> и т. д., так как они явно больше 256)</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    Digits <span class="token operator">=</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">100</span><span class="token punctuation">;</span>
    SetChar <span class="token operator">=</span> <span class="token keyword">set</span> <span class="token keyword">of</span> Char<span class="token punctuation">;</span>
    Letter <span class="token operator">=</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token string">'a'</span><span class="token operator">..</span><span class="token string">'z'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    mychar<span class="token punctuation">:</span> SetChar<span class="token punctuation">;</span>
    mydig<span class="token punctuation">:</span> Digits<span class="token punctuation">;</span>
    simst<span class="token punctuation">:</span> Letter<span class="token punctuation">;</span>
    <span class="token comment">// or</span>
    number<span class="token punctuation">:</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span>
    cif<span class="token punctuation">:</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token number">0</span><span class="token operator">..</span><span class="token number">9</span><span class="token punctuation">;</span>
    codes<span class="token punctuation">:</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token string">#0</span><span class="token operator">..</span><span class="token string">#255</span><span class="token punctuation">;</span> 
</code></pre>
<h3 id="конструкторы-и-инициализация-множеств">Конструкторы и инициализация множеств</h3>
<p>Конструкторы множеств – константы множественного типа:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token punctuation">[</span><span class="token punctuation">]</span> – пустое множество<span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">11</span><span class="token punctuation">]</span> – множество чисел<span class="token punctuation">;</span>
<span class="token punctuation">[</span>’a’<span class="token punctuation">,</span> ’d’<span class="token punctuation">,</span> ’f’<span class="token punctuation">,</span> ’h’<span class="token punctuation">]</span> – множество символов<span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> k<span class="token punctuation">]</span> – множество чисел<span class="token punctuation">,</span> переменная k должна содержать число<span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">2</span><span class="token operator">..</span><span class="token number">100</span><span class="token punctuation">]</span> – множество содержит целые числа из указанного интервала<span class="token punctuation">;</span>
<span class="token punctuation">[</span>k<span class="token operator">..</span><span class="token number">2</span> <span class="token operator">*</span> k<span class="token punctuation">]</span> – интервал можно задать выражениями<span class="token punctuation">;</span>
<span class="token punctuation">[</span>red<span class="token punctuation">,</span> yellow<span class="token punctuation">,</span> green<span class="token punctuation">]</span><span class="token operator">-</span> множество перечисляемого типа<span class="token punctuation">.</span>
</code></pre>
<p>Инициализация множеств при объявлении:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    SetNum <span class="token operator">=</span> <span class="token keyword">set</span> <span class="token keyword">of</span> Byte<span class="token punctuation">;</span>
<span class="token keyword">var</span> 
    s<span class="token punctuation">:</span> SetNum <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">10</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="операции-над-множествами">Операции над множествами</h3>
<ol>
<li>
<p>Присваивание:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">A <span class="token operator">:=</span> B<span class="token punctuation">;</span>
A <span class="token operator">:=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>Объединение, пересечение и дополнение:</p>
<ul>
<li><code>A + B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>∪</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A \cup B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∪</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – объединение  множеств <code>А</code> и <code>B</code> – множество, состоящее из элементов, принадлежащих множествам <code>А</code> и <code>B</code>.</li>
<li><code>A * B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>∩</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A \cap B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∩</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – пересечение множеств <code>А</code> и <code>B</code> – множество, состоящее из элементов, принадлежащих одновременно и множеству <code>А</code> и множеству <code>B</code>.</li>
<li><code>A - B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>∖</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A \setminus B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">∖</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – дополнение  множества <code>А</code> до <code>B</code> – множество, состоящее из тех элементов множества <code>А</code>, которые не принадлежат множеству <code>B</code>.</li>
</ul>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">]</span> <span class="token operator">+</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">10</span><span class="token punctuation">]</span> <span class="token operator">*</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">9</span> <span class="token punctuation">,</span><span class="token number">15</span><span class="token punctuation">,</span> <span class="token number">23</span><span class="token punctuation">,</span> <span class="token number">45</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">15</span><span class="token punctuation">]</span> <span class="token operator">-</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">,</span> <span class="token number">15</span><span class="token punctuation">,</span> <span class="token number">23</span><span class="token punctuation">,</span> <span class="token number">45</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token operator">..</span><span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">10</span><span class="token operator">..</span><span class="token number">14</span><span class="token punctuation">]</span>
<span class="token punctuation">[</span>red<span class="token punctuation">,</span> blue<span class="token punctuation">,</span> green<span class="token punctuation">,</span> black<span class="token punctuation">]</span> <span class="token operator">*</span> <span class="token punctuation">[</span>blue<span class="token punctuation">,</span> magneta<span class="token punctuation">,</span> yellow<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span>blue<span class="token punctuation">]</span>
</code></pre>
</li>
<li>
<p>Операции отношения:</p>
<ul>
<li><code>A = B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>=</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A = B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – проверка совпадения  множеств А и B (если совпадают – <code>true</code>).</li>
<li><code>A &lt;&gt; B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>≠</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A \not= B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.88888em; vertical-align: -0.19444em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel"><span class="mord"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.69444em;"><span class="" style="top: -3em;"><span class="pstrut" style="height: 3em;"></span><span class="rlap"><span class="strut" style="height: 0.88888em; vertical-align: -0.19444em;"></span><span class="inner"><span class="mrel"></span></span><span class="fix"></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.19444em;"><span class=""></span></span></span></span></span></span></span><span class="base"><span class="strut" style="height: 0.36687em; vertical-align: 0em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – проверка не совпадения  множеств А и B (не совпадают – <code>true</code>).</li>
<li><code>A &lt;= B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>⊆</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A \subseteq B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.8193em; vertical-align: -0.13597em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">⊆</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – проверка нестрогого вхождения A в B (если входит – <code>true</code>).</li>
<li><code>A &gt; B</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>A</mi><mo>⊃</mo><mi>B</mi></mrow><annotation encoding="application/x-tex">A \supset B</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.72243em; vertical-align: -0.0391em;"></span><span class="mord mathdefault">A</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">⊃</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.05017em;">B</span></span></span></span></span>) – проверка строгого вхождения B в A (если входит – <code>true</code>).</li>
</ul>
</li>
</ol>
<!--- &#1053;&#1072;&#1076;&#1077;&#1102;&#1089;&#1100;, &#1095;&#1090;&#1086; &#1087;&#1088;&#1072;&#1074;&#1080;&#1083;&#1100;&#1085;&#1086; &#1088;&#1072;&#1089;&#1089;&#1090;&#1072;&#1074;&#1080;&#1083; &#1079;&#1085;&#1072;&#1082;&#1080; &#1087;&#1088;&#1080;&#1085;&#1072;&#1076;&#1083;&#1077;&#1078;&#1085;&#1086;&#1089;&#1090;&#1080;... -->
<ol start="4">
<li>Проверка вхождения элемента во множество:<br>
<code>x in A</code> (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>x</mi><mo>∈</mo><mi>A</mi></mrow><annotation encoding="application/x-tex">x \in A</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.5782em; vertical-align: -0.0391em;"></span><span class="mord mathdefault">x</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">∈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault">A</span></span></span></span></span>) – входит ли элемент <code>x</code>  в множество <code>A</code> (если входит – <code>true</code>).<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">]</span> <span class="token operator">+</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">10</span><span class="token punctuation">]</span> <span class="token operator">*</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">9</span> <span class="token punctuation">,</span><span class="token number">15</span><span class="token punctuation">,</span> <span class="token number">23</span><span class="token punctuation">,</span> <span class="token number">45</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">15</span><span class="token punctuation">]</span> <span class="token operator">-</span> <span class="token punctuation">[</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">,</span> <span class="token number">15</span><span class="token punctuation">,</span> <span class="token number">23</span><span class="token punctuation">,</span> <span class="token number">45</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token operator">..</span><span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">10</span><span class="token operator">..</span><span class="token number">14</span><span class="token punctuation">]</span>
<span class="token punctuation">[</span>red<span class="token punctuation">,</span> blue<span class="token punctuation">,</span> green<span class="token punctuation">,</span> black<span class="token punctuation">]</span> <span class="token operator">*</span> <span class="token punctuation">[</span>blue<span class="token punctuation">,</span> magneta<span class="token punctuation">,</span> yellow<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span>blue<span class="token punctuation">]</span>
</code></pre>
</li>
</ol>
<h3 id="ввод-вывод-элементов-множеств">Ввод-вывод элементов множеств</h3>
<p><strong>Значения множественного типа нельзя вводить и выводить!</strong></p>
<ul>
<li>
<p>Ввод элементов множества:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    s<span class="token punctuation">:</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">100</span><span class="token punctuation">;</span>
    n<span class="token punctuation">:</span> Word<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
s <span class="token operator">:=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">read</span><span class="token punctuation">(</span>n<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">while</span> n <span class="token operator">&lt;&gt;</span> <span class="token number">0</span> <span class="token keyword">do</span>
    <span class="token keyword">begin</span>
        s <span class="token operator">:=</span> s <span class="token operator">+</span> <span class="token punctuation">[</span>n<span class="token punctuation">]</span><span class="token punctuation">;</span>
        <span class="token keyword">read</span><span class="token punctuation">(</span>n<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
readLn<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
</code></pre>
</li>
<li>
<p>Вывод элементов множества:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    s<span class="token punctuation">:</span> <span class="token keyword">set</span> <span class="token keyword">of</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">100</span><span class="token punctuation">;</span>

<span class="token comment">{...}</span>
s <span class="token operator">:=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">for</span> item <span class="token operator">:=</span> <span class="token string">'a'</span> <span class="token keyword">to</span> <span class="token string">'z'</span> <span class="token keyword">do</span>
    <span class="token keyword">if</span> item <span class="token operator">in</span> s <span class="token keyword">then</span>
        <span class="token keyword">write</span><span class="token punctuation">(</span>i<span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
writeLn<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h2 id="записи-delphi-pascal">Записи Delphi Pascal</h2>
<p><strong>Запись</strong> – это структура данных, образованная <em>фиксированным числом разнотипных компонентов</em>, называемых <strong>полями</strong> записи</p>
<p>Формат:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    <span class="token operator">&lt;</span>имя<span class="token operator">&gt;</span> <span class="token operator">=</span> <span class="token keyword">record</span>
        <span class="token operator">&lt;</span>переменные<span class="token operator">&gt;</span><span class="token punctuation">:</span> <span class="token operator">&lt;</span>тип<span class="token operator">&gt;</span><span class="token punctuation">;</span>               <span class="token comment">// фиксированная часть</span>
        <span class="token comment">{--//--}</span>
        <span class="token punctuation">[</span><span class="token keyword">case</span> <span class="token punctuation">[</span>тэг<span class="token punctuation">:</span><span class="token punctuation">]</span> <span class="token punctuation">[</span>набор_типов<span class="token punctuation">]</span> <span class="token keyword">of</span>      <span class="token comment">// вариантная часть</span>
	        <span class="token operator">&lt;</span>тип<span class="token operator">&gt;</span><span class="token punctuation">:</span> <span class="token punctuation">(</span>
	            <span class="token operator">&lt;</span>переменные<span class="token operator">&gt;</span><span class="token punctuation">:</span> <span class="token operator">&lt;</span>тип<span class="token operator">&gt;</span><span class="token punctuation">;</span>
	            <span class="token comment">{--//--}</span>
	        <span class="token punctuation">)</span><span class="token punctuation">;</span>
	        <span class="token comment">{--//--}</span>
	    <span class="token punctuation">]</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<p>Примеры:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
	rec1<span class="token punctuation">:</span> <span class="token keyword">record</span>
	    day<span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span>
        month<span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">12</span><span class="token punctuation">;</span>
        year<span class="token punctuation">:</span> Word<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    Data <span class="token operator">=</span> <span class="token keyword">record</span>
        day<span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span>
        month<span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">12</span><span class="token punctuation">;</span>
        year<span class="token punctuation">:</span> Word<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> 
    rec1<span class="token punctuation">:</span> Data<span class="token punctuation">;</span>
    birthDay<span class="token punctuation">:</span> Data <span class="token operator">=</span> <span class="token punctuation">(</span>day<span class="token punctuation">:</span> <span class="token number">30</span><span class="token punctuation">;</span> month<span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">;</span> year<span class="token punctuation">:</span> <span class="token number">1973</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    EntryType <span class="token operator">=</span> <span class="token punctuation">(</span>Book<span class="token punctuation">,</span> Magazine<span class="token punctuation">)</span><span class="token punctuation">;</span>
    Entry <span class="token operator">=</span> <span class="token keyword">record</span>  
        autor<span class="token punctuation">,</span> title<span class="token punctuation">:</span> <span class="token keyword">String</span><span class="token punctuation">;</span>  
        year <span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">2000</span><span class="token punctuation">;</span>
        <span class="token keyword">case</span> tag<span class="token punctuation">:</span> EntryType <span class="token keyword">of</span>
            Book<span class="token punctuation">:</span> <span class="token punctuation">(</span>publisher<span class="token punctuation">,</span> city<span class="token punctuation">:</span> <span class="token keyword">String</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            Magazine<span class="token punctuation">:</span> <span class="token punctuation">(</span>
                magName<span class="token punctuation">:</span> <span class="token keyword">String</span><span class="token punctuation">;</span> 
                volume<span class="token punctuation">,</span> issue<span class="token punctuation">:</span> Integer
            <span class="token punctuation">)</span><span class="token punctuation">;</span>            <span class="token comment">// case не имеет своего end'а и пишется последним.</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    e<span class="token punctuation">:</span> Entry<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
e<span class="token punctuation">.</span>tag <span class="token operator">:=</span> Book<span class="token punctuation">;</span>               <span class="token comment">// вариант записи: Book</span>
e<span class="token punctuation">.</span>autor <span class="token operator">:=</span> <span class="token string">'Thomas Hobbes'</span><span class="token punctuation">;</span>  
e<span class="token punctuation">.</span>title <span class="token operator">:=</span> <span class="token string">'Leviathan'</span><span class="token punctuation">;</span>  
e<span class="token punctuation">.</span>year <span class="token operator">:=</span> <span class="token number">1651</span><span class="token punctuation">;</span>  
<span class="token comment">// Как бы предназначены для варианта Book записи Entry:</span>
e<span class="token punctuation">.</span>publisher <span class="token operator">:=</span> <span class="token string">'Andrew Crooke'</span><span class="token punctuation">;</span>  
e<span class="token punctuation">.</span>city <span class="token operator">:=</span> <span class="token string">'London'</span><span class="token punctuation">;</span>
</code></pre>
<h6 id="подробнее-про-вариативную-часть-informatics.mccme.ru">Подробнее про вариативную часть: <a href="https://informatics.mccme.ru/mod/book/view.php?id=534&amp;chapterid=259">informatics.mccme.ru</a></h6>
<h3 id="операции-над-записями">Операции над записями</h3>
<ol>
<li>Присваивание записей одного типа:<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    Date <span class="token operator">=</span> <span class="token keyword">record</span>
        day<span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span>
        month<span class="token punctuation">:</span> <span class="token number">1.12</span><span class="token punctuation">;</span>
        year<span class="token punctuation">:</span> Word<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    a<span class="token punctuation">,</span> b<span class="token punctuation">:</span> Date<span class="token punctuation">;</span>
    c<span class="token punctuation">:</span> Date<span class="token punctuation">;</span>
    d<span class="token punctuation">,</span> e<span class="token punctuation">:</span> <span class="token keyword">record</span> day<span class="token punctuation">:</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">31</span><span class="token punctuation">;</span> month<span class="token punctuation">:</span> <span class="token number">1.12</span><span class="token punctuation">;</span> year<span class="token punctuation">:</span> Word<span class="token punctuation">;</span> <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token comment">{...}</span>
a <span class="token operator">:=</span> b<span class="token punctuation">;</span>
b <span class="token operator">:=</span> c<span class="token punctuation">;</span>
a <span class="token operator">:=</span> c<span class="token punctuation">;</span>
d <span class="token operator">:=</span> e<span class="token punctuation">;</span>

a <span class="token operator">:=</span> d<span class="token punctuation">;</span> <span class="token comment">// ОШИБКА! Считаются разными типами!</span>
e <span class="token operator">:=</span> c<span class="token punctuation">;</span> <span class="token comment">// ОШИБКА! Считаются разными типами!</span>
</code></pre>
</li>
<li>Доступ к полям записи<pre class=" language-pascal"><code class="prism  language-pascal">a<span class="token punctuation">.</span>day <span class="token operator">:=</span> <span class="token number">21</span><span class="token punctuation">;</span>      <span class="token comment">{точечная нотация}</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">with</span> a <span class="token keyword">do</span>         <span class="token comment">{оператор доступа}</span>
    day <span class="token operator">:=</span> <span class="token number">27</span><span class="token punctuation">;</span>  
<span class="token keyword">with</span> b <span class="token keyword">do</span> <span class="token keyword">begin</span>   <span class="token comment">{оператор доступа c блочным оператором}</span>
    day <span class="token operator">:=</span> <span class="token number">22</span><span class="token punctuation">;</span>  
    month <span class="token operator">:=</span> <span class="token number">6</span><span class="token punctuation">;</span>
    year <span class="token operator">:=</span> <span class="token number">1983</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>Ввод и вывод записей осуществляется по полям.</li>
</ol>
<h2 id="процедуры-и-функции.-определение-описание-особенности.-примеры.">Процедуры и функции. Определение, описание, особенности. Примеры.</h2>
<p><strong>Процедуры и функции</strong> – самостоятельные фрагменты программы, соответствующим образом оформленные и вызываемые по имени (программные блоки).</p>
<p>Общий вид программного блока: <code>Заголовок блока -&gt; Раздел описаний -&gt; Раздел операторов</code></p>
<h3 id="различия-между-процедурой-и-функцией">Различия между <em>процедурой</em> и <em>функцией</em></h3>
<h4 id="процедура">Процедура</h4>
<p>Заголовок начинается с служебного слова <code>procedure</code>.<br>
После работы процедура не возвращает значений.</p>
<p>Общий вид:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">procedure</span> <span class="token operator">&lt;</span>идентификатор<span class="token operator">&gt;</span> <span class="token punctuation">[</span><span class="token punctuation">(</span><span class="token operator">&lt;</span>паратметры<span class="token operator">&gt;</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token keyword">var</span>
   <span class="token operator">&lt;</span>локальные переменные<span class="token operator">&gt;</span><span class="token punctuation">;</span><span class="token punctuation">]</span>
<span class="token keyword">begin</span>
	<span class="token operator">&lt;</span>операторы<span class="token operator">&gt;</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<p>Пример заголовка</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">procedure</span> alpha<span class="token punctuation">(</span>x<span class="token punctuation">:</span> Integer<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h4 id="функция">Функция</h4>
<p>Заголовок начинается с служебного слова <code>function</code> и заканчивается возвращаемым типом. После работы функции, она возвращает значение типа, который указан в заголовке как возвращаемый.</p>
<p>Общий вид:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> <span class="token operator">&lt;</span>идентификатор<span class="token operator">&gt;</span> <span class="token punctuation">[</span><span class="token punctuation">(</span><span class="token operator">&lt;</span>паратметры<span class="token operator">&gt;</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">:</span> <span class="token operator">&lt;</span>возвращаемый тип<span class="token operator">&gt;</span><span class="token punctuation">;</span>
<span class="token punctuation">[</span><span class="token keyword">var</span>
   <span class="token operator">&lt;</span>локальные переменные<span class="token operator">&gt;</span><span class="token punctuation">;</span><span class="token punctuation">]</span>
<span class="token keyword">begin</span>
	<span class="token operator">&lt;</span>операторы<span class="token operator">&gt;</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<p>Пример заголовка:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> func<span class="token punctuation">(</span>x<span class="token punctuation">:</span> Integer<span class="token punctuation">)</span><span class="token punctuation">:</span> Double<span class="token punctuation">;</span>
</code></pre>
<p>Чтобы вернуть какое-то значение из функции, в процессе её выполнения необходимо присвоить системной переменной <em><code>&lt;идентификатор_функции&gt;</code></em> (или  <code>result</code>, при включенном расширенном синтаксисе <code>{$X+}</code>) это необходимое значение.</p>
<p>Пример возврата значения:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token comment">{$X+}</span>
<span class="token keyword">function</span> hypot<span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">:</span> Double<span class="token punctuation">)</span><span class="token punctuation">:</span> Double<span class="token punctuation">;</span>
<span class="token keyword">var</span>
	c_sqr<span class="token punctuation">,</span> c<span class="token punctuation">:</span> Double<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
	c_sqr <span class="token operator">:=</span> sqr<span class="token punctuation">(</span>a<span class="token punctuation">)</span> <span class="token operator">+</span> sqr<span class="token punctuation">(</span>b<span class="token punctuation">)</span><span class="token punctuation">;</span>
	c <span class="token operator">:=</span> sqrt<span class="token punctuation">(</span>c_sqr<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">result</span> <span class="token operator">:=</span> c<span class="token punctuation">;</span>  <span class="token comment">// или `hypot := sqrt(c_sqr);`</span>
	writeLn<span class="token punctuation">(</span><span class="token string">'Hypot is '</span><span class="token punctuation">,</span> c<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="локальные-и-глобальные-переменные-законы-«видимости»-идентификаторов">Локальные и глобальные переменные, законы «видимости» идентификаторов</h3>

<table>
<thead>
<tr>
<th>Классы переменных</th>
<th>Время жизни</th>
<th>Доступность</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Глобальные</strong> – объявленные в основной программе</td>
<td>От запуска до завершения программы</td>
<td>Из любого места программы, включая подпрограммы*</td>
</tr>
<tr>
<td><strong>Локальные</strong> – объявленные в подпрограмме</td>
<td>От вызова подпрограммы до возврата управления</td>
<td>Из подпрограммы и подпрограмм, вызываемых из нее*</td>
</tr>
</tbody>
</table><p><strong>*</strong> – при отсутствии перекрытия имен</p>
<h3 id="способы-передачи-данных-в-подпрограмму-на-delphi-pascal">Способы передачи данных в подпрограмму на Delphi Pascal</h3>
<p>Подпрограмма может получать данные из основной программы:</p>
<ol>
<li><strong>неявно</strong> – с использованием свойства доступности глобальных переменных;</li>
<li><strong>явно</strong> – через параметры.</li>
</ol>
<p>Очевидно, что <em>явная</em> передача значительно лучше, так как позволяет делать подпрограммы более универсальными и независимыми.</p>
<h3 id="формальные-и-фактические-параметры-подпрограмм-delphi-pascal">Формальные и фактические параметры подпрограмм Delphi Pascal</h3>
<p>Параметры, описанные в заголовке – <strong>формальные</strong>.</p>
<p>При вызове подпрограммы необходимо определить <strong>фактические</strong> значения этих параметров – аргументы (константы и переменные).</p>
<blockquote>
<p>Вот только кто вообще их так называет?<br>
Обычно их называют <strong>параметрами</strong> и <strong>аргументами</strong> соответственно.</p>
</blockquote>
<p><em>Формальные</em> и <em>фактические</em> параметры должны соответствовать по количеству, типу и порядку:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> proc<span class="token punctuation">(</span>a<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span> b<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">:</span> Byte<span class="token punctuation">;</span>
<span class="token comment">{...}</span>

n <span class="token operator">:=</span> proc<span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">2.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// a = 5, b = 2.1</span>
</code></pre>
<h3 id="типы-параметров-constvar-переменные">Типы параметров, <code>const</code>/<code>var</code>-переменные</h3>
<ul>
<li>
<p><strong>Параметры-значения</strong> при описании подпрограммы не помечаются. По факту в эту переменную <em>копируется</em> значение переданного аргумента, поэтому изменение этой переменной в подпрограмме не отразится на внешней.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> beta<span class="token punctuation">(</span>x<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span> n<span class="token punctuation">:</span> Byte<span class="token punctuation">)</span><span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    x <span class="token operator">:=</span> x <span class="token operator">-</span> <span class="token number">5</span><span class="token punctuation">;</span>
    beta <span class="token operator">:=</span> x <span class="token operator">*</span> n<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a <span class="token operator">:=</span> <span class="token number">6</span><span class="token punctuation">;</span>
writeLn<span class="token punctuation">(</span>beta<span class="token punctuation">(</span>a<span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 3</span>
writeLn<span class="token punctuation">(</span>a<span class="token punctuation">)</span><span class="token punctuation">;</span>           <span class="token comment">// 6</span>
</code></pre>
</li>
<li>
<p><strong>Параметры-переменные</strong> при описании подпрограммы помечаются служебным словом <code>var</code>.<br>
По факту происходит передача переменной <em>по адресу</em>, то есть все изменения такой переменной в подпрограмме <strong>отразятся на внешней</strong>!</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> alpha<span class="token punctuation">(</span><span class="token keyword">var</span> x<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span> n<span class="token punctuation">:</span> Byte<span class="token punctuation">)</span><span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    x <span class="token operator">:=</span> x <span class="token operator">-</span> <span class="token number">5</span><span class="token punctuation">;</span>
    alpha <span class="token operator">:=</span> x <span class="token operator">*</span> n<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a <span class="token operator">:=</span> <span class="token number">6</span><span class="token punctuation">;</span>
writeLn<span class="token punctuation">(</span>alpha<span class="token punctuation">(</span>a<span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// 3</span>
writeLn<span class="token punctuation">(</span>a<span class="token punctuation">)</span><span class="token punctuation">;</span>            <span class="token comment">// 1</span>
</code></pre>
<p><strong>Ограничение</strong>: в качестве фактических значений (<em>аргументов</em>) <em><strong>параметров-переменных</strong></em> нельзя использовать литералы!</p>
<pre class=" language-pascal"><code class="prism  language-pascal">alpha<span class="token punctuation">(</span><span class="token number">6</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span> <span class="token comment">// Ошибка!</span>
</code></pre>
</li>
<li>
<p><strong>Параметры-константы</strong> при описании подпрограммы помечаются служебным словом <code>const</code>.<br>
Как и с <em>параметрами-переменными</em>, по факту происходит передача переменной <em>по адресу</em>, но при попытке изменить значение переменной в подпрограмме, вызывается ошибка. То есть изменять значение в подпрограмме запрещено.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> gamma<span class="token punctuation">(</span><span class="token keyword">const</span> x<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span> n<span class="token punctuation">:</span> Byte<span class="token punctuation">)</span><span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    x <span class="token operator">:=</span> x <span class="token operator">-</span> <span class="token number">5</span><span class="token punctuation">;</span>        <span class="token comment">// ОШИБКА</span>
    gamma<span class="token operator">:=</span> x <span class="token operator">*</span> n<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
<span class="token comment">{...}</span>
a <span class="token operator">:=</span> <span class="token number">6</span><span class="token punctuation">;</span>
writeLn<span class="token punctuation">(</span>gamma<span class="token punctuation">(</span>a<span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// ОШИБКА</span>
writeLn<span class="token punctuation">(</span>a<span class="token punctuation">)</span><span class="token punctuation">;</span>            <span class="token comment">// -</span>
</code></pre>
</li>
</ul>
<p><strong>Ограничение</strong>: в качестве фактических значений (<em>аргументов</em>) <strong>параметров-переменных</strong> нельзя использовать литералы!</p>
<h2 id="структурные-типы-параметров-параметры-строки-параметры-массивы.">Структурные типы параметров: параметры-строки, параметры-массивы.</h2>
<p>Структурные типы параметров должны быть <strong>предварительно объявлены</strong>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    IntArr <span class="token operator">=</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">100</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Integer<span class="token punctuation">;</span>
    MyStr <span class="token operator">=</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token number">25</span><span class="token punctuation">]</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> sum<span class="token punctuation">(</span>arr<span class="token punctuation">:</span> IntArr<span class="token punctuation">;</span> n<span class="token punctuation">:</span> Integer<span class="token punctuation">)</span><span class="token punctuation">:</span> integer<span class="token punctuation">;</span>
<span class="token comment">{...}</span>

<span class="token keyword">procedure</span> test_string<span class="token punctuation">(</span>str<span class="token punctuation">:</span> MyStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">{...}</span>

<span class="token keyword">var</span>
    my_arr<span class="token punctuation">:</span> IntArr<span class="token punctuation">;</span>
    my_str<span class="token punctuation">:</span> MyStr<span class="token punctuation">;</span>
    <span class="token comment">{...}</span>

<span class="token keyword">begin</span>
    <span class="token comment">{...}</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Sum(arr) = '</span><span class="token punctuation">,</span> sum<span class="token punctuation">(</span>my_arr<span class="token punctuation">,</span> n<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    test_string<span class="token punctuation">(</span>my_str<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h2 id="принципы-разработки-универсальных-подпрограмм">Принципы разработки универсальных подпрограмм</h2>
<h3 id="открытые-массивы">Открытые массивы</h3>
<p><strong>Открытый массив</strong> – конструкция описания типа массива без указания типа индексов.<br>
Используется только при объявлении <em>формальных параметров</em>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">array</span> <span class="token keyword">of</span> Single<span class="token punctuation">;</span>
<span class="token keyword">array</span> <span class="token keyword">of</span> Integer<span class="token punctuation">;</span>
</code></pre>
<p>С помощью открытых массивов можно делать более <em>универсальные</em> подпрограммы.</p>
<p><strong>Индексы открытого массива всегда начинаются с <code>0</code>-го.</strong></p>
<p>Размер можно:</p>
<ul>
<li>передать через дополнительный параметр;</li>
<li>получить, используя функцию <code>high(&lt;идентификатор_массива&gt;)</code>.</li>
</ul>
<h3 id="открытые-строки">Открытые строки</h3>
<p><s><strong>Для строк, передаваемых в подпрограмму как параметр-переменная, осуществляет контроль длины строки.</strong></s></p>
<p><s>Чтобы избежать его необходимо использовать «<em>открытые</em>» строки (<code>openstring</code>).</s></p>
<blockquote>
<p><s>Или <a href="http://docwiki.embarcadero.com/RADStudio/Sydney/en/Open_String_Parameters_(Delphi)">можно использовать параметр</a> <code>{$P+}</code>, который сам будет делать так, что параметрами будут открытые строки</s></p>
</blockquote>
<p><s>Пример.  Программа, формирующая строку из букв латинского алфавита.</s></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">unit</span> Stroka<span class="token punctuation">;</span>

<span class="token keyword">interface</span>
    <span class="token keyword">procedure</span> add<span class="token punctuation">(</span><span class="token keyword">var</span> s<span class="token punctuation">:</span> Openstring<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">implementation</span>
    <span class="token keyword">procedure</span> add<span class="token punctuation">;</span>
    <span class="token keyword">var</span> 
        ch<span class="token punctuation">:</span> Char<span class="token punctuation">;</span>
    
    <span class="token keyword">begin</span>
        ch <span class="token operator">:=</span> s<span class="token punctuation">[</span>length<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
        s <span class="token operator">:=</span> s <span class="token operator">+</span> chr<span class="token punctuation">(</span>succ<span class="token punctuation">(</span>Ord<span class="token punctuation">(</span>Ch<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex4_6<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>

<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span> Stroka <span class="token operator">in</span> <span class="token string">'Stroka.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    s<span class="token punctuation">:</span> <span class="token keyword">String</span><span class="token punctuation">[</span><span class="token number">26</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    i<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    s <span class="token operator">:=</span> <span class="token string">'A'</span><span class="token punctuation">;</span>
    <span class="token keyword">for</span> i <span class="token operator">:=</span> <span class="token number">2</span> <span class="token keyword">to</span> <span class="token number">26</span> <span class="token keyword">do</span>
        add<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">;</span>
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<blockquote>
<p>Протестировав такое, у меня без этих “<em>открытых</em>” строк проблем не возникло. Скорее всего, из-за того, что сейчас, в новых версиях, обычные строки всегда считаются “длинными” (<code>UnicodeString</code>), поэтому и проблем сейчас с передачей строк нет:<br>
<strong>Note:</strong> The <code>$P</code> directive is obsolete. Now the default string is long (<a href="http://docwiki.embarcadero.com/Libraries/Sydney/en/System.UnicodeString" title="lib en:System.UnicodeString"><code>UnicodeString</code></a>). You should not have to use <code>{$OPENSTRINGS}</code> in any new applications you write.<br>
Источник: <a href="http://docwiki.embarcadero.com/RADStudio/Sydney/en/Open_String_Parameters_(Delphi)">docwiki.embarcadero.com</a></p>
</blockquote>
<h3 id="нетипизированные-параметры.">Нетипизированные параметры.</h3>
<p><strong>Нетипизированные параметры</strong> – <em>параметры-переменные</em>, тип которых при объявлении не указан.</p>
<p>Для приведения нетипизированного параметра к определенному типу можно использовать:</p>
<ol>
<li>
<p>автоопределенное преобразование типов:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">procedure</span> proc<span class="token punctuation">(</span><span class="token keyword">var</span> a<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">{...}</span>
b <span class="token operator">:=</span> Integer<span class="token punctuation">(</span>a<span class="token punctuation">)</span> <span class="token operator">+</span> <span class="token number">10</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>наложенное описание переменной определенного типа:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    TType <span class="token operator">=</span> <span class="token punctuation">(</span>TReal<span class="token punctuation">,</span> TInteger<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> proc<span class="token punctuation">(</span><span class="token keyword">var</span> a<span class="token punctuation">;</span> t<span class="token punctuation">:</span> TType<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span>
    r<span class="token punctuation">:</span> Real <span class="token keyword">absolute</span> a<span class="token punctuation">;</span>
    i<span class="token punctuation">:</span> Integer <span class="token keyword">absolute</span> a<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
    <span class="token keyword">if</span> t <span class="token operator">=</span> TReal <span class="token keyword">then</span>
        <span class="token comment">{используем переменную `r`}</span>
    <span class="token keyword">else</span>
        <span class="token comment">{используем переменную `i`}</span>
</code></pre>
<p>По факту, тут <code>a</code> является ссылкой на какой-то адрес в памяти, но нужный размер в памяти нам неизвестен. С помощью наложения мы делаем несколько видов переменных, <em>накладывая</em> на адрес переменной <code>a</code> разные типы.</p>
</li>
</ol>
<h3 id="параметры-процедурного-типа">Параметры процедурного типа</h3>
<p>Параметры процедурного типа используются для передачи в подпрограмму имен процедур и функций.</p>
<p>Для объявления процедурного типа используется заголовок подпрограммы, в котором отсутствует имя:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    Proc <span class="token operator">=</span> <span class="token keyword">procedure</span> <span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">,</span> c<span class="token punctuation">:</span> Real<span class="token punctuation">;</span> <span class="token keyword">var</span> d<span class="token punctuation">:</span> Real<span class="token punctuation">)</span><span class="token punctuation">;</span>
    UnaryFunc <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span>x<span class="token punctuation">:</span> Double<span class="token punctuation">)</span><span class="token punctuation">:</span> Double<span class="token punctuation">;</span>
</code></pre>
<p>Значениями переменных процедурных типов являются идентификаторы процедур и функций с соответствующими заголовками:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token comment">{...}</span>

<span class="token keyword">function</span> fun1<span class="token punctuation">(</span>x<span class="token punctuation">:</span> Double<span class="token punctuation">)</span><span class="token punctuation">:</span> Double<span class="token punctuation">;</span>
<span class="token comment">{...}</span>

<span class="token keyword">procedure</span> test_function<span class="token punctuation">(</span>f<span class="token punctuation">:</span> UnaryFunc<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">if</span> f<span class="token punctuation">(</span><span class="token number">0</span><span class="token punctuation">)</span> <span class="token operator">&gt;</span> <span class="token number">0</span> <span class="token keyword">then</span>  <span class="token comment">// какая-то проверка функции</span>
        <span class="token comment">{...}</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    f<span class="token punctuation">:</span> UnaryFunc<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
f <span class="token operator">:=</span> fun1<span class="token punctuation">;</span>
test_function<span class="token punctuation">(</span>f<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// или test_function(fun1);</span>
</code></pre>
<h2 id="модули-delphi-pascal">Модули Delphi Pascal</h2>
<p><strong>Модуль</strong> – это автономно компилируемая коллекция программных ресурсов, предназначенных для использования другими модулями и программами</p>
<p><strong>Ресурсы</strong> – переменные, константы, описания типов и подпрограммы.</p>
<p>Все ресурсы, определенные в модуле делят на:</p>
<ol>
<li><strong>внешние</strong> – предназначенные для использования другими программами и модулями.</li>
<li><strong>внутренние</strong> – предназначенные для использования внутри модуля.</li>
</ol>
<p>Структура модуля:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">unit</span> <span class="token operator">&lt;</span>имя_модуля<span class="token operator">&gt;</span><span class="token punctuation">;</span>  <span class="token comment">// Имя модуля должно совпадать с </span>
                    <span class="token comment">// именем файла, в котором он описан.</span>

<span class="token keyword">interface</span>
    <span class="token operator">&lt;</span>интерфейсная_секция<span class="token operator">&gt;</span>

<span class="token keyword">implementation</span>
    <span class="token operator">&lt;</span>секция_реализации<span class="token operator">&gt;</span>

<span class="token punctuation">[</span><span class="token keyword">initialization</span>
    <span class="token operator">&lt;</span>секция_инициализации<span class="token operator">&gt;</span>

<span class="token punctuation">[</span><span class="token keyword">finalization</span>
    <span class="token operator">&lt;</span>секция_завершения<span class="token operator">&gt;</span><span class="token punctuation">]</span><span class="token punctuation">]</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h3 id="подключение-модуля-к-программе">Подключение модуля к программе</h3>
<p>Подключение модуля к программе осуществляется по имени:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">uses</span> <span class="token operator">&lt;</span>имя_модуля<span class="token number">1</span><span class="token operator">&gt;</span><span class="token punctuation">,</span> <span class="token operator">&lt;</span>имя_модуля<span class="token number">2</span><span class="token operator">&gt;</span><span class="token punctuation">,</span>  <span class="token comment">{...}</span><span class="token punctuation">;</span>
</code></pre>
<h4 id="объявление-модулей-в-файле-проекта">Объявление модулей в файле проекта</h4>
<blockquote>
<p>Только для проектов (<em>Delphi</em>, <em>Lazarus</em>). Для обычных программ формата <code>.pas</code> не работает.</p>
</blockquote>
<p>Если:</p>
<ul>
<li>к проекту подключается модуль, который находится в каталоге, не совпадающем с каталогом проекта и не указанном в путях компилятора;</li>
<li>в путях компилятора имеется несколько модулей с одинаковыми именами,</li>
</ul>
<p>то необходимо указать местонахождение модуля:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">uses</span>  Strings <span class="token operator">in</span> <span class="token string">'C:\Classes\Strings.pas'</span><span class="token punctuation">;</span> <span class="token comment">{абсолютный путь}</span>
<span class="token comment">// или</span>
<span class="token keyword">uses</span>  Strings <span class="token operator">in</span> <span class="token string">'..\Strings.pas'</span><span class="token punctuation">;</span>         <span class="token comment">{относительный путь}</span>
</code></pre>
<h3 id="законы-видимости-идентификаторов.-доступ-к--«перекрытым»-идентификаторам">Законы видимости идентификаторов. Доступ к  «перекрытым» идентификаторам</h3>
<p><strong>Ресурсы модуля перекрываются ресурсами программы и ранее указанных модулей.</strong></p>
<p>Для доступа к перекрытым ресурсам модуля используют точечную нотацию: <code>&lt;имя_модуля&gt;.&lt;имя_ресурса&gt;</code></p>
<p>Пример:<br>
<img src="https://i.imgur.com/R0qXc5n.png" alt="identificators_intersection"></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">unit</span> A<span class="token punctuation">;</span>
    <span class="token keyword">interface</span>
        <span class="token keyword">var</span> x<span class="token punctuation">:</span> Real<span class="token punctuation">;</span>  <span class="token comment">// !!!</span>
        <span class="token comment">{...}</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> ex<span class="token punctuation">;</span>
<span class="token keyword">uses</span> A<span class="token punctuation">;</span>
<span class="token keyword">var</span> x<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>       <span class="token comment">// !!!</span>
<span class="token keyword">begin</span>
    x <span class="token operator">:=</span> <span class="token number">10</span><span class="token punctuation">;</span>
    A<span class="token punctuation">.</span>x <span class="token operator">:=</span> <span class="token number">0.45</span><span class="token punctuation">;</span>
    <span class="token comment">{...}</span>
</code></pre>
<h2 id="рекурсия">Рекурсия</h2>
<p><strong>Рекурсия</strong> – организация вычислений, при которой процедура или функция обращаются к самим себе.</p>
<p>Различают <em>явную</em> и <em>косвенную</em> рекурсии.<br>
При <em>явной</em> – в теле подпрограммы существует вызов самой себя, при <em>косвенной</em> – вызов осуществляется в подпрограммах, вызываемых из рассматриваемой.</p>
<p>Косвенная рекурсия требует предопределения <code>forward</code>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">procedure</span> B<span class="token punctuation">(</span>j<span class="token punctuation">:</span> Byte<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">forward</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> A<span class="token punctuation">(</span>j<span class="token punctuation">:</span> Byte<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token comment">{...}</span> B<span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">{...}</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> B<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token comment">{...}</span> A<span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">{...}</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="структура-рекурсивной-подпрограммы">Структура рекурсивной подпрограммы</h3>
<p><img src="https://i.imgur.com/Bvqfn7D.png" alt="enter image description here"></p>
<p>«<em>Операторы после вызова</em>», выполняются <strong>после возврата управления</strong> из рекурсивно вызванной подпрограммы.</p>
<h3 id="фрейм-активации">Фрейм активации</h3>
<p>Каждое обращение к рекурсивной подпрограмме вызывает независимую <em>активацию</em> этой подпрограммы.</p>
<p>Совокупность данных, необходимых для <em>одной</em> активации рекурсивной подпрограммы, называется <strong>фреймом активации</strong>.</p>
<p>Фрейм активации включает</p>
<ul>
<li>локальные переменные подпрограммы;</li>
<li>копии параметров-значений;</li>
<li>адреса параметров-переменных и параметров-констант (4 байта);</li>
<li>копию строки результата (для функций типа <code>string</code>);</li>
<li>служебную информацию (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>≈</mo><mn>12</mn></mrow><annotation encoding="application/x-tex">\approx12</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.48312em; vertical-align: 0em;"></span><span class="mrel">≈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">1</span><span class="mord">2</span></span></span></span></span> байт, точный размер этой области зависит от способа передачи параметров).</li>
</ul>
<p>Пример.<br>
Задача: переворот заданной строки.</p>
<ol>
<li>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token comment">///               pointer: 4 bytes;  string[255]: 256 bytes</span>
<span class="token keyword">function</span> reverse1<span class="token punctuation">(</span><span class="token keyword">const</span> st<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">if</span> length<span class="token punctuation">(</span>st<span class="token punctuation">)</span> <span class="token operator">=</span> <span class="token number">0</span> <span class="token keyword">then</span> 
        <span class="token keyword">result</span> <span class="token operator">:=</span> ‘‘
    <span class="token keyword">else</span>
        <span class="token keyword">result</span> <span class="token operator">:=</span> reverse1<span class="token punctuation">(</span>copy<span class="token punctuation">(</span>st<span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> length<span class="token punctuation">(</span>st<span class="token punctuation">)</span> <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">+</span> st<span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<p><em>Фрейм активации</em>: <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>V</mi><mo>=</mo><mn>4</mn><mo>+</mo><mn>256</mn><mtext>&nbsp;</mtext><mo>+</mo><mo>&lt;</mo><mi mathvariant="normal">с</mi><mi mathvariant="normal">л</mi><mi mathvariant="normal">у</mi><mi mathvariant="normal">ж</mi><mi mathvariant="normal">е</mi><mi mathvariant="normal">б</mi><mi mathvariant="normal">н</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">я</mi><mtext>&nbsp;</mtext><mi mathvariant="normal">о</mi><mi mathvariant="normal">б</mi><mi mathvariant="normal">л</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">с</mi><mi mathvariant="normal">т</mi><mi mathvariant="normal">ь</mi><mo>&gt;</mo><mtext>&nbsp;</mtext><mo>≈</mo><mn>272</mn><mtext>&nbsp;</mtext><mi mathvariant="normal">б</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">й</mi><mi mathvariant="normal">т</mi></mrow><annotation encoding="application/x-tex">V = 4 + 256\space+ &lt;служебная\spaceобласть&gt; \space\approx 272\spaceбайт</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.22222em;">V</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">4</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">2</span><span class="mord">5</span><span class="mord">6</span><span class="mspace">&nbsp;</span><span class="mord">+</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&lt;</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.88888em; vertical-align: -0.19444em;"></span><span class="mord cyrillic_fallback">с</span><span class="mord cyrillic_fallback">л</span><span class="mord cyrillic_fallback" style="margin-right: 0.01389em;">у</span><span class="mord cyrillic_fallback">ж</span><span class="mord cyrillic_fallback">е</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">н</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">я</span><span class="mspace">&nbsp;</span><span class="mord cyrillic_fallback">о</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">л</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">с</span><span class="mord cyrillic_fallback">т</span><span class="mord cyrillic_fallback">ь</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&gt;</span><span class="mspace">&nbsp;</span></span><span class="base"><span class="strut" style="height: 0.48312em; vertical-align: 0em;"></span><span class="mrel">≈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.69444em; vertical-align: 0em;"></span><span class="mord">2</span><span class="mord">7</span><span class="mord">2</span><span class="mspace">&nbsp;</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">й</span><span class="mord cyrillic_fallback">т</span></span></span></span></span></p>
</li>
<li>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token comment">///              pointer: 4 bytes; longint: 4 bytes</span>
<span class="token keyword">procedure</span> reverse2<span class="token punctuation">(</span><span class="token keyword">var</span> ss<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span> n<span class="token punctuation">:</span> integer<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span>
    temp<span class="token punctuation">:</span> char<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    <span class="token keyword">if</span> n <span class="token operator">&lt;=</span> length<span class="token punctuation">(</span>ss<span class="token punctuation">)</span> <span class="token operator">div</span> <span class="token number">2</span> <span class="token keyword">then</span> 
        <span class="token keyword">begin</span>
            temp <span class="token operator">:=</span> ss<span class="token punctuation">[</span>n<span class="token punctuation">]</span><span class="token punctuation">;</span>
            ss<span class="token punctuation">[</span>n<span class="token punctuation">]</span> <span class="token operator">:=</span> ss<span class="token punctuation">[</span>length<span class="token punctuation">(</span>ss<span class="token punctuation">)</span> <span class="token operator">-</span> n <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
            ss<span class="token punctuation">[</span>length<span class="token punctuation">(</span>ss<span class="token punctuation">)</span> <span class="token operator">-</span> n <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">]</span> <span class="token operator">:=</span> temp<span class="token punctuation">;</span>
            reverse2<span class="token punctuation">(</span>ss<span class="token punctuation">,</span> n <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">end</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<p><em>Фрейм активации</em>: <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>V</mi><mo>=</mo><mn>4</mn><mo>+</mo><mn>4</mn><mtext>&nbsp;</mtext><mo>+</mo><mo>&lt;</mo><mi mathvariant="normal">с</mi><mi mathvariant="normal">л</mi><mi mathvariant="normal">у</mi><mi mathvariant="normal">ж</mi><mi mathvariant="normal">е</mi><mi mathvariant="normal">б</mi><mi mathvariant="normal">н</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">я</mi><mtext>&nbsp;</mtext><mi mathvariant="normal">о</mi><mi mathvariant="normal">б</mi><mi mathvariant="normal">л</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">с</mi><mi mathvariant="normal">т</mi><mi mathvariant="normal">ь</mi><mo>&gt;</mo><mtext>&nbsp;</mtext><mo>≈</mo><mn>21</mn><mtext>&nbsp;</mtext><mi mathvariant="normal">б</mi><mi mathvariant="normal">а</mi><mi mathvariant="normal">й</mi><mi mathvariant="normal">т</mi></mrow><annotation encoding="application/x-tex">V = 4 + 4\space+ &lt;служебная\spaceобласть&gt; \space\approx 21\spaceбайт</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.22222em;">V</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">4</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.72777em; vertical-align: -0.08333em;"></span><span class="mord">4</span><span class="mspace">&nbsp;</span><span class="mord">+</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&lt;</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.88888em; vertical-align: -0.19444em;"></span><span class="mord cyrillic_fallback">с</span><span class="mord cyrillic_fallback">л</span><span class="mord cyrillic_fallback" style="margin-right: 0.01389em;">у</span><span class="mord cyrillic_fallback">ж</span><span class="mord cyrillic_fallback">е</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">н</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">я</span><span class="mspace">&nbsp;</span><span class="mord cyrillic_fallback">о</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">л</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">с</span><span class="mord cyrillic_fallback">т</span><span class="mord cyrillic_fallback">ь</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&gt;</span><span class="mspace">&nbsp;</span></span><span class="base"><span class="strut" style="height: 0.48312em; vertical-align: 0em;"></span><span class="mrel">≈</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.69444em; vertical-align: 0em;"></span><span class="mord">2</span><span class="mord">1</span><span class="mspace">&nbsp;</span><span class="mord cyrillic_fallback">б</span><span class="mord cyrillic_fallback">а</span><span class="mord cyrillic_fallback">й</span><span class="mord cyrillic_fallback">т</span></span></span></span></span></p>
</li>
</ol>
<h3 id="древовидная-рекурсия.-перестановки">Древовидная рекурсия. Перестановки</h3>
<p><img src="https://i.imgur.com/N57aijY.png" alt="perest"></p>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-PwdhE8PEpk4CzztH" width="100%" style="max-width: 576.9375px;" viewBox="0 0 576.9375 324"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M290.5078125,31.718779973144063L96.875,65L96.875,90" marker-end="url(#arrowhead383)" style="fill:none"></path><defs><marker id="arrowhead383" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M300.5078125,40L300.5078125,65L300.5078125,90" marker-end="url(#arrowhead384)" style="fill:none"></path><defs><marker id="arrowhead384" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M310.5078125,31.718450326045264L504.1796875,65L504.1796875,90" marker-end="url(#arrowhead385)" style="fill:none"></path><defs><marker id="arrowhead385" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M81.453125,127.53251533742332L45.9375,161L45.9375,186" marker-end="url(#arrowhead386)" style="fill:none"></path><defs><marker id="arrowhead386" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M112.296875,127.53251533742332L147.8125,161L147.8125,186" marker-end="url(#arrowhead387)" style="fill:none"></path><defs><marker id="arrowhead387" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M285.328125,127.31527244819647L249.609375,161L249.609375,186" marker-end="url(#arrowhead388)" style="fill:none"></path><defs><marker id="arrowhead388" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M315.6875,127.31527244819647L351.40625,161L351.40625,186" marker-end="url(#arrowhead389)" style="fill:none"></path><defs><marker id="arrowhead389" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M488.828125,127.47735993860323L453.28125,161L453.28125,186" marker-end="url(#arrowhead390)" style="fill:none"></path><defs><marker id="arrowhead390" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M519.53125,127.47735993860323L555.078125,161L555.078125,186" marker-end="url(#arrowhead391)" style="fill:none"></path><defs><marker id="arrowhead391" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M45.9375,232L45.9375,257L45.9375,282" marker-end="url(#arrowhead392)" style="fill:none"></path><defs><marker id="arrowhead392" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M147.8125,232L147.8125,257L147.8125,282" marker-end="url(#arrowhead393)" style="fill:none"></path><defs><marker id="arrowhead393" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M249.609375,232L249.609375,257L249.609375,282" marker-end="url(#arrowhead394)" style="fill:none"></path><defs><marker id="arrowhead394" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M351.40625,232L351.40625,257L351.40625,282" marker-end="url(#arrowhead395)" style="fill:none"></path><defs><marker id="arrowhead395" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M453.28125,232L453.28125,257L453.28125,282" marker-end="url(#arrowhead396)" style="fill:none"></path><defs><marker id="arrowhead396" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M555.078125,232L555.078125,257L555.078125,282" marker-end="url(#arrowhead397)" style="fill:none"></path><defs><marker id="arrowhead397" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="base" transform="translate(300.5078125,30)" style="opacity: 1;"><rect rx="0" ry="0" x="-10" y="-10" width="20" height="20"></rect><g class="label" transform="translate(0,0)"><g transform="translate(0,0)"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"></div></foreignObject></g></g></g><g class="node" id="A" transform="translate(96.875,113)" style="opacity: 1;"><rect rx="0" ry="0" x="-15.421875" y="-23" width="30.84375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-5.421875,-13)"><foreignObject width="10.84375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">A</div></foreignObject></g></g></g><g class="node" id="B" transform="translate(300.5078125,113)" style="opacity: 1;"><rect rx="0" ry="0" x="-15.1796875" y="-23" width="30.359375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-5.1796875,-13)"><foreignObject width="10.359375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">B</div></foreignObject></g></g></g><g class="node" id="C" transform="translate(504.1796875,113)" style="opacity: 1;"><rect rx="0" ry="0" x="-15.3515625" y="-23" width="30.703125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-5.3515625,-13)"><foreignObject width="10.703125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">C</div></foreignObject></g></g></g><g class="node" id="AB" transform="translate(45.9375,209)" style="opacity: 1;"><rect rx="0" ry="0" x="-20.59375" y="-23" width="41.1875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-10.59375,-13)"><foreignObject width="21.1875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">AB</div></foreignObject></g></g></g><g class="node" id="AC" transform="translate(147.8125,209)" style="opacity: 1;"><rect rx="0" ry="0" x="-20.765625" y="-23" width="41.53125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-10.765625,-13)"><foreignObject width="21.53125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">AC</div></foreignObject></g></g></g><g class="node" id="BA" transform="translate(249.609375,209)" style="opacity: 1;"><rect rx="0" ry="0" x="-20.515625" y="-23" width="41.03125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-10.515625,-13)"><foreignObject width="21.03125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">BA</div></foreignObject></g></g></g><g class="node" id="BC" transform="translate(351.40625,209)" style="opacity: 1;"><rect rx="0" ry="0" x="-20.5234375" y="-23" width="41.046875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-10.5234375,-13)"><foreignObject width="21.046875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">BC</div></foreignObject></g></g></g><g class="node" id="CA" transform="translate(453.28125,209)" style="opacity: 1;"><rect rx="0" ry="0" x="-20.765625" y="-23" width="41.53125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-10.765625,-13)"><foreignObject width="21.53125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">CA</div></foreignObject></g></g></g><g class="node" id="CB" transform="translate(555.078125,209)" style="opacity: 1;"><rect rx="0" ry="0" x="-20.5234375" y="-23" width="41.046875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-10.5234375,-13)"><foreignObject width="21.046875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">CB</div></foreignObject></g></g></g><g class="node" id="ABC" transform="translate(45.9375,305)" style="opacity: 1;"><rect rx="0" ry="0" x="-25.9375" y="-23" width="51.875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-15.9375,-13)"><foreignObject width="31.875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">ABC</div></foreignObject></g></g></g><g class="node" id="ACB" transform="translate(147.8125,305)" style="opacity: 1;"><rect rx="0" ry="0" x="-25.9375" y="-23" width="51.875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-15.9375,-13)"><foreignObject width="31.875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">ACB</div></foreignObject></g></g></g><g class="node" id="BAC" transform="translate(249.609375,305)" style="opacity: 1;"><rect rx="0" ry="0" x="-25.859375" y="-23" width="51.71875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-15.859375,-13)"><foreignObject width="31.71875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">BAC</div></foreignObject></g></g></g><g class="node" id="BCA" transform="translate(351.40625,305)" style="opacity: 1;"><rect rx="0" ry="0" x="-25.9375" y="-23" width="51.875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-15.9375,-13)"><foreignObject width="31.875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">BCA</div></foreignObject></g></g></g><g class="node" id="CAB" transform="translate(453.28125,305)" style="opacity: 1;"><rect rx="0" ry="0" x="-25.9375" y="-23" width="51.875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-15.9375,-13)"><foreignObject width="31.875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">CAB</div></foreignObject></g></g></g><g class="node" id="CBA" transform="translate(555.078125,305)" style="opacity: 1;"><rect rx="0" ry="0" x="-25.859375" y="-23" width="51.71875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-15.859375,-13)"><foreignObject width="31.71875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">CBA</div></foreignObject></g></g></g></g></g></g></svg></div>
<p><img src="https://i.imgur.com/WL7RK19.png" alt="enter image description here"></p>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-361n0Qta79CbmU6z" width="100%" style="max-width: -1984px;" viewBox="0 0 -1984 -1984"><g transform="translate(-992, -992)"><g class="output"><g class="clusters"></g><g class="edgePaths"></g><g class="edgeLabels"></g><g class="nodes"></g></g></g></svg></div>
<p><a href="https://mermaid-js.github.io/mermaid-live-editor">https://mermaid-js.github.io/mermaid-live-editor</a></p>
<h2 id="динамическая-память">Динамическая память</h2>
<p>Минимальная адресуемая единица памяти – <strong>байт</strong>.</p>
<p><strong>Физический адрес</strong> <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi mathvariant="normal">А</mi><mi mathvariant="normal">ф</mi></msub></mrow><annotation encoding="application/x-tex">А_ф</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord cyrillic_fallback">А</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.336108em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord cyrillic_fallback mtight">ф</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span> – номер байта оперативной памяти.<br>
Адресация по схеме «база+смещение»: <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi mathvariant="normal">А</mi><mi mathvariant="normal">ф</mi></msub><mo>=</mo><msub><mi mathvariant="normal">А</mi><mi mathvariant="normal">б</mi></msub><mo>+</mo><msub><mi mathvariant="normal">А</mi><mrow><mi mathvariant="normal">с</mi><mi mathvariant="normal">м</mi></mrow></msub></mrow><annotation encoding="application/x-tex">А_ф = А_б + А_{см}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord cyrillic_fallback">А</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.336108em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord cyrillic_fallback mtight">ф</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord cyrillic_fallback">А</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.336108em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord cyrillic_fallback mtight">б</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord cyrillic_fallback">А</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord cyrillic_fallback mtight">с</span><span class="mord cyrillic_fallback mtight">м</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span>,<br>
где <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi mathvariant="normal">А</mi><mi mathvariant="normal">б</mi></msub></mrow><annotation encoding="application/x-tex">А_б</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord cyrillic_fallback">А</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.336108em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord cyrillic_fallback mtight">б</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span> – адрес базы – адрес, относительно которого считают остальные адреса;<br>
<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi mathvariant="normal">А</mi><mrow><mi mathvariant="normal">с</mi><mi mathvariant="normal">м</mi></mrow></msub></mrow><annotation encoding="application/x-tex">А_{см}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord cyrillic_fallback">А</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord cyrillic_fallback mtight">с</span><span class="mord cyrillic_fallback mtight">м</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span> – смещение – расстояние от базового адреса  до физического.</p>
<p><strong>Указатель</strong> – тип данных, используемый для хранения <strong>смещений</strong>.<br>
В памяти занимает 4 байта, адресует сегмент размером <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>V</mi><mo>=</mo><msup><mn>2</mn><mn>32</mn></msup><mo>=</mo><mn>4</mn></mrow><annotation encoding="application/x-tex">V = 2^{32} =  4</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathdefault" style="margin-right: 0.22222em;">V</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.814108em; vertical-align: 0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.814108em;"><span class="" style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">3</span><span class="mord mtight">2</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">4</span></span></span></span></span> ГБ.<br>
Базовый адрес = адрес сегмента.</p>
<h3 id="типизированные-и-нетипизированные-указатели">Типизированные и нетипизированные указатели</h3>
<p>Различают указатели:</p>
<ul>
<li><em>типизированные</em> – адресующие данные конкретного типа;</li>
<li><em>нетипизированные</em> – не связанные с данными определенного типа.</li>
</ul>
<p>Объявление типизированного указателя: <code>^&lt;идентификатор_базового_типа&gt;</code></p>
<p>Объявление нетипизированного указателя:  <code>Pointer</code></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    TPI <span class="token operator">=</span> <span class="token string">^I</span>nteger<span class="token punctuation">;</span>
 
 <span class="token keyword">var</span>
     pi<span class="token punctuation">:</span> TPI<span class="token punctuation">;</span>
     pr<span class="token punctuation">:</span> <span class="token string">^R</span>eal<span class="token punctuation">;</span>
     p<span class="token punctuation">:</span> Pointer
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    PP <span class="token operator">=</span> <span class="token string">^P</span>erson<span class="token punctuation">;</span>    <span class="token comment">// Можно объявлять указатель типа, который объявлен следом</span>
    Preson <span class="token operator">=</span> <span class="token keyword">record</span>
        <span class="token keyword">name</span><span class="token punctuation">:</span> <span class="token keyword">String</span><span class="token punctuation">;</span>
        next<span class="token punctuation">:</span> PP<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    r<span class="token punctuation">:</span> <span class="token string">^I</span>nteger <span class="token operator">=</span> <span class="token keyword">nil</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="операции-с-указателями">Операции с указателями</h3>
<ol>
<li>
<p><strong>Присваивание</strong>. Допускается присваивать указателю только значение того же или неопределенного типа.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    p1<span class="token punctuation">,</span> p2<span class="token punctuation">:</span> <span class="token string">^I</span>nteger<span class="token punctuation">;</span>
    p3<span class="token punctuation">:</span> <span class="token string">^R</span>eal<span class="token punctuation">;</span>
    p<span class="token punctuation">:</span> Pointer<span class="token punctuation">;</span>
<span class="token comment">{...}</span>
p1 <span class="token operator">:=</span> p2<span class="token punctuation">;</span>
p <span class="token operator">:=</span> p3<span class="token punctuation">;</span>
p1 <span class="token operator">:=</span> p<span class="token punctuation">;</span>
p1 <span class="token operator">:=</span> <span class="token keyword">nil</span><span class="token punctuation">;</span>
p <span class="token operator">:=</span> <span class="token keyword">nil</span><span class="token punctuation">;</span>
<span class="token comment">{нельзя:
p3 := p2;
p1 := p3;}</span>
</code></pre>
</li>
<li>
<p><strong>Получение адреса</strong>: оператор <code>@</code>. Результат операции – указатель типа <code>pointer</code> –  может присвоен любому указателю.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    i<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
    pi<span class="token punctuation">:</span> <span class="token string">^I</span>nteger<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
pi <span class="token operator">:=</span> <span class="token operator">@</span>i<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Доступ к данным</strong> по указателю (<strong>операция разыменования</strong>). Полученное  значение имеет тип, совпадающий с базовым типом данных указателя. <em>Нетипизированные указатели разыменовывать нельзя</em>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal">j <span class="token operator">:=</span> pi<span class="token operator">^</span><span class="token punctuation">;</span>
pi<span class="token operator">^</span> <span class="token operator">:=</span> pi<span class="token operator">^</span> <span class="token operator">+</span> <span class="token number">2</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><em>Операции отношения</em>: проверка равенства <code>=</code> и неравенства <code>&lt;&gt;</code>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal">sign <span class="token operator">:=</span> p1 <span class="token operator">=</span> p2<span class="token punctuation">;</span>
<span class="token keyword">if</span> p1 <span class="token operator">&lt;&gt;</span> <span class="token keyword">nil</span> <span class="token keyword">then</span> <span class="token comment">{...}</span>
</code></pre>
</li>
</ol>
<h3 id="функции-для-работы-с-указателями">Функции для работы с указателями</h3>
<ol>
<li>
<p>Функция <code>addr(x): Pointer</code> – возвращает адрес объекта <code>x</code>, в качестве которого может быть указано имя переменной, функции, процедуры. Фактически, <code>addr(x)</code> <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>≡</mo></mrow><annotation encoding="application/x-tex">\equiv</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.46375em; vertical-align: 0em;"></span><span class="mrel">≡</span></span></span></span></span> <code>@x</code>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal">ptr <span class="token operator">:=</span> addr<span class="token punctuation">(</span>obj<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// &lt;-&gt; ptr := @obj;</span>
</code></pre>
</li>
<li>
<p>Функция <code>assigned(const p): Boolean</code> – проверяет, присвоено ли значение указателю. Фактически, <code>assigned(p)</code> <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mo>≡</mo></mrow><annotation encoding="application/x-tex">\equiv</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.46375em; vertical-align: 0em;"></span><span class="mrel">≡</span></span></span></span></span> <code>p &lt;&gt; nil</code>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal">ptr <span class="token operator">:=</span> addr<span class="token punctuation">(</span>obj<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// &lt;-&gt; ptr := @obj;</span>
</code></pre>
</li>
<li>
<p>Функция <code>ptr(address: Integer): Pointer</code> – преобразует число в указатель.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
    p<span class="token punctuation">:</span> Pointer<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
p <span class="token operator">:=</span> ptr<span class="token punctuation">(</span>a<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ol>
<h3 id="динамическое-распределение-памяти">Динамическое распределение памяти</h3>
<p>Управление выделением и освобождением памяти осуществляется посредством специальных процедур и функций:</p>
<ol>
<li>
<p>Процедура <code>new(var p: ^&lt;тип&gt;)</code> – выделяет память для размещения переменной, размер определяется типом указателя.</p>
</li>
<li>
<p>Процедура <code>dispose(var p: ^&lt;тип&gt;)</code> – освобождает выделенную память.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    pi<span class="token punctuation">:</span> <span class="token string">^I</span>nteger<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
writeLn<span class="token punctuation">(</span>assigned<span class="token punctuation">(</span>pi<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// false</span>
<span class="token keyword">new</span><span class="token punctuation">(</span>pi<span class="token punctuation">)</span><span class="token punctuation">;</span>
pi<span class="token operator">^</span> <span class="token operator">:=</span> <span class="token number">5</span><span class="token punctuation">;</span>
<span class="token keyword">dispose</span><span class="token punctuation">(</span>pi<span class="token punctuation">)</span><span class="token punctuation">;</span>
writeLn<span class="token punctuation">(</span>assigned<span class="token punctuation">(</span>pi<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// true (так как pi &lt;&gt; nil)</span>
</code></pre>
</li>
<li>
<p>Процедура <code>getMem(var p: Pointer; size: Integer)</code> – выделяет указанное количество памяти и помещает ее адрес в указатель.</p>
</li>
<li>
<p>Процедура <code>freeMem(var p: Pointer[; size: Integer])</code> – освобождает выделенную память.</p>
</li>
<li>
<p>Процедура <code>sizeOf(x): Integer</code> – возвращает размер объекта в байтах.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    buffer<span class="token punctuation">:</span> <span class="token string">^a</span>rray<span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">100</span><span class="token punctuation">]</span> <span class="token keyword">of</span> Byte<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
getMem<span class="token punctuation">(</span>buffer<span class="token punctuation">,</span> sizeOf<span class="token punctuation">(</span>buffer<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
buffer<span class="token operator">^</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span> <span class="token operator">:=</span> <span class="token number">125</span><span class="token punctuation">;</span>
<span class="token comment">{...}</span>
freeMem<span class="token punctuation">(</span>buffer<span class="token punctuation">,</span> sizeOf<span class="token punctuation">(</span>buffer<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
</code></pre>
<!--- sizeOf(buffer) = 4  ?????-->
</li>
</ol>
<h2 id="динамические-структуры-данных">Динамические структуры данных</h2>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-c51E9BhmW0I7plol" width="100%" style="max-width: 484.625px;" viewBox="0 0 484.625 158"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M214.1640625,62.91961102106969L101.3671875,91L101.3671875,116" marker-end="url(#arrowhead409)" style="fill:none"></path><defs><marker id="arrowhead409" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M294.1796875,66L294.1796875,91L294.1796875,116" marker-end="url(#arrowhead410)" style="fill:none"></path><defs><marker id="arrowhead410" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M367.4659830729167,66L447.125,91L447.125,116" marker-end="url(#arrowhead411)" style="fill:none"></path><defs><marker id="arrowhead411" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="base" transform="translate(294.1796875,43)" style="opacity: 1;"><rect rx="0" ry="0" x="-80.015625" y="-23" width="160.03125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-70.015625,-13)"><foreignObject width="140.03125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Структуры данных</div></foreignObject></g></g></g><g class="node" id="a" transform="translate(101.3671875,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-81.3671875" y="-23" width="162.734375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-71.3671875,-13)"><foreignObject width="142.734375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Последовательные</div></foreignObject></g></g></g><g class="node" id="b" transform="translate(294.1796875,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-61.4453125" y="-23" width="122.890625" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-51.4453125,-13)"><foreignObject width="102.890625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Древовидные</div></foreignObject></g></g></g><g class="node" id="c" transform="translate(447.125,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-41.5" y="-23" width="83" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-31.5,-13)"><foreignObject width="63" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Сетевые</div></foreignObject></g></g></g></g></g></g></svg></div>
<p><em>Пример последовательных</em>: вектор, матрица, строка, запись, очередь, стек, дек.<br>
<em>Пример древовидных</em>: бинарные деревья.</p>
<h3 id="динамические-линейные-структуры">Динамические линейные структуры</h3>
<ol>
<li><strong>Очередь</strong> – структура данных, реализующая: добавление – в конец, а удаление – из начала.</li>
<li><strong>Стек</strong> – структура данных, реализующая: добавление и удаление с одной стороны.</li>
<li><strong>Дек</strong> – структура данных, реализующая: добавление и удаление с двух сторон.</li>
</ol>
<h3 id="списки">Списки</h3>
<p><strong>Список</strong> – способ организации данных, предполагающий использование указателей для определения следующего элемента.</p>
<p>Элемент списка состоит из двух частей: <em>информационной</em> и <em>адресной</em>.</p>
<p>Информационная часть содержит поля данных.</p>
<p>Адресная – включает от одного до n указателей, содержащих адреса следующих элементов. Количество связей, между соседними элементами списка определяет его связность: односвязные, двусвязные, n-связные.</p>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-vdC0ac8FMxeXmIuy" width="100%" style="max-width: 584.9375px;" viewBox="0 0 584.9375 158"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M261.5234375,50.709110643782644L68.1875,91L68.1875,116" marker-end="url(#arrowhead421)" style="fill:none"></path><defs><marker id="arrowhead421" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M261.5234375,64.8685653805446L217.3203125,91L217.3203125,116" marker-end="url(#arrowhead422)" style="fill:none"></path><defs><marker id="arrowhead422" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M335.5078125,64.8685653805446L379.7109375,91L379.7109375,116" marker-end="url(#arrowhead423)" style="fill:none"></path><defs><marker id="arrowhead423" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M335.5078125,50.35153318669944L540.046875,91L540.046875,116" marker-end="url(#arrowhead424)" style="fill:none"></path><defs><marker id="arrowhead424" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="base" transform="translate(298.515625,43)" style="opacity: 1;"><rect rx="0" ry="0" x="-36.9921875" y="-23" width="73.984375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-26.9921875,-13)"><foreignObject width="53.984375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Списки</div></foreignObject></g></g></g><g class="node" id="a" transform="translate(68.1875,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-48.1875" y="-23" width="96.375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-38.1875,-13)"><foreignObject width="76.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Линейные</div></foreignObject></g></g></g><g class="node" id="b" transform="translate(217.3203125,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-50.9453125" y="-23" width="101.890625" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-40.9453125,-13)"><foreignObject width="81.890625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Кольцевые</div></foreignObject></g></g></g><g class="node" id="c" transform="translate(379.7109375,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-61.4453125" y="-23" width="122.890625" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-51.4453125,-13)"><foreignObject width="102.890625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Древовидные</div></foreignObject></g></g></g><g class="node" id="e" transform="translate(540.046875,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-48.890625" y="-23" width="97.78125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-38.890625,-13)"><foreignObject width="77.78125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">N-связные</div></foreignObject></g></g></g></g></g></g></svg></div>
<h4 id="виды-списков">Виды списков</h4>
<h2 id="списковые-структуры-данных.-классификация-и-основные-приемы-работы-с-ними-создание-элемента-добавление-элемента-к-списку-удаление-элемента-из-списка.-область--применения-списковых-структур-данных.-пример.">21. Списковые структуры данных. Классификация и основные приемы работы с ними: создание элемента, добавление элемента к списку, удаление элемента из списка. Область  применения списковых структур данных. Пример.</h2>
<h2 id="работа-с-файлами">Работа с файлами</h2>
<h3 id="файловая-система">Файловая система</h3>
<p><strong>Файл</strong> – поименованная последовательность элементов данных (компонентов файла), хранящихся, как правило, во внешней памяти.</p>
<p>Как исключение данные файла могут не храниться, а вводиться с внешних устройств (ВУ), например клавиатуры или выводиться на ВУ.</p>
<p>Полное имя файла включает:</p>
<p><code>&lt;Имя диска&gt;:&lt;Список имен каталогов&gt;\&lt;Имя файла&gt;.&lt;Расширение&gt;</code></p>
<p>Имя файла в Windows составляют из строчных и прописных букв латинского и русского алфавитов, арабских цифр и некоторых специальных символов, например, символов подчеркивания <code>_</code> или доллара <code>$</code></p>
<h3 id="файлы-delphi-pascal">Файлы <em>Delphi Pascal</em></h3>
<p><strong>Файл языка Pascal</strong> –  последовательность однотипных компонентов: файл записей, файл целых чисел, файл строк.</p>
<p>В зависимости от типа компонентов различают три типа файлов: <strong>типизированные</strong>, <strong>текстовые</strong> и <strong>нетипизированные</strong>.</p>
<p>Количество компонентов файла при объявлении файловой переменной не указывается.</p>
<p>Максимальный размер файла определяется свободным пространством на устройстве, например, диске.</p>
<p>Физически операции ввода-вывода с файлами выполняются с использованием буфера.</p>
<p>Для файлов принципиально возможен не только последовательный, но и <strong>произвольный доступ</strong>,  при котором чтение информации  осуществляется из указанного места.</p>
<h3 id="указатель-файла">Указатель файла</h3>
<p>Доступ к компонентам файла осуществляется через <strong>указатель файла</strong>.</p>
<p>При выполнении операции чтения или записи указатель <strong>автоматически</strong> перемещается  на следующий компонент.</p>
<p>После вывода последнего компонента файла система пишет специальную запись – <strong>маркер «<em>Конец файла</em>»</strong> (байт <code>#26</code>).</p>
<p>При обнаружении во время операции чтения  маркера конца файла – операция завершается. Попытка читать маркер вызывает прерывание по ошибке чтения.</p>
<h3 id="описание-файловых-переменных">Описание файловых переменных</h3>
<ol>
<li>Типизированные файлы: <code>file of &lt;тип&gt;</code></li>
<li>Текстовые файлы: <code>text</code></li>
<li>Нетипизированные файлы: <code>file</code></li>
</ol>
<h3 id="использование-файлов-в-качестве-параметров-подпрограмм">Использование файлов в качестве параметров подпрограмм</h3>
<p>Файлы можно передавать в подпрограмму только через <strong>параметры-переменные</strong>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    FF <span class="token operator">=</span> <span class="token keyword">file</span> <span class="token keyword">of</span> Integer<span class="token punctuation">;</span>

<span class="token keyword">procedure</span> print<span class="token punctuation">(</span><span class="token keyword">var</span> f1<span class="token punctuation">:</span> FF<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="работа-с-файлами-1">Работа с файлами</h3>
<p>Работа с файлами включает:</p>
<ul>
<li><strong>инициализацию файловой переменной</strong>  – установление связи файловой переменной с файлом;</li>
<li><strong>открытие файла</strong>  – подготовку файла для выполнения операций ввода-вывода;</li>
<li><strong>обработку компонентов файла</strong>  – выполнение операций ввода-вывода элементов данных;</li>
<li><strong>закрытие файла</strong>.</li>
</ul>
<h4 id="инициализация-файловой-переменной">Инициализация файловой переменной</h4>
<p>Процедура  <code>assign</code>  или  <code>assignFile (var f; path: String)</code> (<em>предпочтительнее</em>)  – связывает файловую переменную <code>f</code> с файлом, имя которого указано в строке <code>path</code>.</p>
<p>Если файл находится в текущем каталоге, то достаточно задать имя файла и его расширение. В противном случае необходимо указать полное имя файла.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    FI1 <span class="token operator">=</span> <span class="token keyword">file</span> <span class="token keyword">of</span> Integer<span class="token punctuation">;</span>

<span class="token keyword">var</span>
    f1<span class="token punctuation">,</span> f2<span class="token punctuation">:</span> FI1<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
assignFile<span class="token punctuation">(</span>f1<span class="token punctuation">,</span> ’F1<span class="token punctuation">.</span>dat’<span class="token punctuation">)</span><span class="token punctuation">;</span>        <span class="token comment">{файл в текущем каталоге, относительный путь}</span>
assignFile<span class="token punctuation">(</span>f2<span class="token punctuation">,</span> ’d<span class="token punctuation">:</span>\iva\a<span class="token punctuation">.</span>dat’<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">{файл в другом каталоге, абсолютный путь}</span>
</code></pre>
<h4 id="открытие-файла">Открытие файла</h4>
<p>При открытии файла необходимо задать направление передачи данных: запись или чтение. Кроме того текстовый файл можно открыть для добавления компонентов.</p>
<ol>
<li>
<p>Процедура <code>reSet(var f)</code> – открывает файл для чтения данных.<br>
Устанавливает указатель файла на первый компонент. Если файл не существует, выдается сообщение об ошибке.</p>
</li>
<li>
<p>Процедура <code>reWrite(var f)</code> – открывает файл для записи.<br>
Если указанный файл существовал, то он уничтожается без выдачи предупреждения пользователю, иначе он создается и указатель устанавливается на начало.</p>
</li>
<li>
<p>Процедура <code>append(var f: Text)</code> – открывает текстовый файл для добавления данных.<br>
Указатель файла устанавливается на конец файла.</p>
</li>
</ol>
<h4 id="контроль-операций-ввода-вывода">Контроль операций ввода-вывода</h4>
<p>Функция <code>IOResult: Word</code>  – возвращает код завершения операции ввода-вывода: 0 – если операция прошла нормально, код ошибки, если нет. <strong>Функция применяется при отключенном контроле операций ввода-вывода <code>{$I-}</code></strong>.</p>
<p>Пример. Проверка существования файла.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    f<span class="token punctuation">:</span> <span class="token keyword">file</span> <span class="token keyword">of</span> char<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    assignFile<span class="token punctuation">(</span>f<span class="token punctuation">,</span>’a<span class="token punctuation">.</span>dat’<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">{инициализация ф. п.}</span>
    <span class="token comment">{$I-}</span>  <span class="token comment">{отключение контроля ошибок ввода-вывода}</span>
    reSet<span class="token punctuation">(</span>f<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">{открытие файла для чтения}</span>
    <span class="token comment">{$I+}</span>  <span class="token comment">{включение контроля ошибок ввода-вывода}</span>
    <span class="token keyword">if</span> IOResult <span class="token operator">&lt;&gt;</span> <span class="token number">0</span> <span class="token keyword">then</span>
        writeLn<span class="token punctuation">(</span><span class="token string">'File was not found'</span><span class="token punctuation">)</span>
    <span class="token keyword">else</span>
        writeLn<span class="token punctuation">(</span><span class="token string">'File was found'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token comment">{...}</span>
</code></pre>
<h4 id="обработка-компонентов-файла">Обработка компонентов файла</h4>
<p>Основные операции над компонентами – операции записи и чтения. На базе этих операций выполняют более сложные операции:</p>
<ul>
<li><em>создание файла</em> – занесение в файл требуемых записей;</li>
<li><em>модификация файла</em> – изменение всех или нескольких записей, добавление и удаление записей;</li>
<li>поиск нужной информации в файле.</li>
</ul>
<p>Операции записи и чтения для каждого типа файла осуществляется по-своему.</p>
<h4 id="закрытие-файла">Закрытие файла</h4>
<p>Процедура <code>close</code> или <code>closeFile(var f)</code> - выполняет закрытие файла. При этом вновь созданный файл регистрируется в каталоге.</p>
<p>Процедура закрытия файла обеспечивает <strong>вывод оставшихся компонентов из буфера в файл</strong>.</p>
<p>Связь файловой переменной с файлом при закрытии сохраняется, поэтому при продолжении обработки повторно процедуру <code>assignFile()</code> можно не выполнять.</p>
<h3 id="стандартные-процедуры-и-функции-обслуживания-файлов-библ.-system">Стандартные процедуры и функции обслуживания файлов (библ. <code>System</code>)</h3>
<ol>
<li>
<p>Процедура <code>reName(var f; name: string)</code> – выполняет переименование файла <code>f</code>, где <code>name</code> – новое имя файла.<br>
При совпадении нового имени файла с ранее существовавшим выдается сообщение об ошибке.</p>
</li>
<li>
<p>Процедура <code>erase(var f)</code> – выполняет удаление файла. Перед уничтожением файл должен быть закрыт.</p>
</li>
<li>
<p>Функция <code>EOF(var f): Boolean</code> – проверяет конец файла, возвращает <code>TRUE</code>, если указатель стоит после последней записи и <code>FALSE</code>, если нет.</p>
</li>
</ol>
<p>Другие функции обслуживания файлов см. <code>Help</code>.</p>
<h3 id="текстовые-файлы">Текстовые файлы</h3>
<p><strong>Текстовый  файл</strong> –  файл, компонентами которого являются символьные строки переменной длины, заканчивающиеся специальным маркером – <strong>маркером «Конец строки»</strong>.</p>
<p>Текстовые файлы используют для хранения и обработки символов, строк, символьных массивов. Числовые и логические данные при записи в текстовые файлы должны преобразовываться в символьные строки.</p>
<p>Текстовый файл можно открыть для записи, чтения и добавления записей в конец. Файл, открытый для записи, не может использоваться для чтения и наоборот.</p>
<h3 id="стандартные-текстовые-файлы">Стандартные текстовые файлы</h3>
<p>Программе, работающей в консольном режиме, без объявления, инициализации файловой переменной и открытия доступны два стандартных текстовых файла, связанных с логическими устройствами ввода и вывода:</p>
<p><code>INPUT</code> – файловая переменная для обозначения файла данных, вводимых с клавиатуры;<br>
<code>OUTPUT</code> – файловая переменная для обозначения файла данных, выводимых на экран.</p>
<h3 id="процедуры-и-функции-обработки-текстовых-файлов">Процедуры и функции обработки текстовых файлов</h3>
<ol>
<li>
<p>Функция <code>EOLn([var f]): Boolean</code> – возвращает <code>TRUE</code>, если во входном текстовом файле достигнут маркер конца строки; при отсутствии файловой переменной проверяется файл <code>INPUT</code>, связанный с клавиатурой.</p>
<ul>
<li>При работе  с <em>клавиатурой</em>  функция <code>EOLn</code> возвращает <code>TRUE</code>,  если  <strong>последним</strong> считанным  был символ <code>#13</code>.</li>
<li>При работе  с <em>диском</em>  функция <code>EOLn</code> возвращает <code>TRUE</code>, если  <strong>следующим</strong> считанным  будет символ <code>#13</code>.</li>
</ul>
</li>
<li>
<p>Процедура <code>read([var f: text;] v1, v2, {...} vn)</code> – обеспечивает ввод символов, строк и чисел. При вводе чисел пробелы и символы табуляции игнорируются. Если файловая переменная не указана, то ввод осуществляется из файла <code>INPUT</code>.</p>
</li>
<li>
<p>Процедура <code>readLn([var f: text;] v1, v2, {...} vn)</code> – осуществляет ввод символов, строк и чисел. После чтения последней переменной оставшаяся часть строки до маркера конца строки пропускается так, что следующее обращение к <code>readLn</code> или <code>read</code> начинается с первого символа новой строки.</p>
</li>
<li>
<p>Процедура <code>write([var f: text;] v1, v2, {...} vn)</code> – осуществляет вывод одного или более выражений типа <code>CHAR</code>, <code>STRING</code>, <code>BOOLEAN</code>, а также целого или вещественного типов. При выводе числовых значений последние преобразуются в символьное представление. Если файловая переменная не указана, то вывод осуществляется в файл <code>OUTPUT</code>.<br>
Любой параметр из списка вывода может иметь формат:<br>
<code>&lt;Параметр&gt; [: &lt;Целое1&gt; [: &lt;Целое2&gt; ]]</code>.</p>
</li>
<li>
<p>Процедура <code>writeLn([var f: text;] v1, v2, {...} vn)</code> – осуществляет вывод в текстовый файл. Если файловая переменная не указана, то вывод осуществляется в файл <code>OUTPUT</code>.<br>
Выводимая строка символов завершается маркером конца строки. Если список вывода не указан, то в файл передается только маркер конца строки.</p>
</li>
<li>
<p>Процедура <code>seekEOLn([var f]): Boolean</code> – пропускает пробелы и знаки табуляции до маркера конца строки или до первого значащего символа и возвращает <code>TRUE</code>, при обнаружении маркера. Если файловая переменная не указана, то функция проверяет файл <code>INPUT</code>.</p>
</li>
<li>
<p>Процедура <code>SeekEOF([var f]): Boolean</code> – пропускает все пробелы, знаки табуляции и маркеры конца строки до маркера конца файла или до первого значащего символа и возвращает <code>TRUE</code> при обнаружении маркера. Если файловая переменная отсутствует, то функция проверяет файл <code>INPUT</code>.</p>
</li>
</ol>
<h3 id="типизированные-файлы">Типизированные файлы</h3>
<p><strong>Типизированный файл</strong> – файл, все компоненты которого одного типа, заданного при объявлении файловой переменной.</p>
<p>Компоненты хранятся на диске во <em>внутреннем</em> (двоичном)  формате.</p>
<p>Типизированный файл можно открыть для записи и чтения. Файл, открытый для записи, может использоваться для чтения. В файл, открытый для чтения, можно писать.</p>
<p>Поскольку  размер компонентов <strong>одинаков</strong>,  принципиально возможен не только последовательный, но и <strong>прямой доступ</strong>.</p>
<h4 id="процедуры-и-функции-обработки-типизированных-файлов">Процедуры и функции обработки типизированных файлов</h4>
<ol>
<li>
<p>Процедура <code>read(var f; c1, c2, {...} cn)</code> – осуществляет чтение компонентов типизированного файла. Список ввода содержит одну или несколько переменных того же типа, что и компоненты файла. Если файл исчерпан, обращение к процедуре  вызывает ошибку ввода-вывода.</p>
</li>
<li>
<p>Процедура <code>write(var f; c1, c2, {...} cn)</code> – осуществляет запись компонентов в типизированный файл.  Список вывода  содержит одно или более выражений того же типа, что и компоненты файла.</p>
</li>
<li>
<p>Процедура <code>seek(var f; numcomp: LongInt)</code> – осуществляет установку указателя файла на компонент с номером <code>numcomp</code>.</p>
</li>
<li>
<p>Функция <code>fileSize(var f): LongInt</code> – возвращает количество компонентов файла. Может использоваться для установки на конец файла совместно с <code>seek()</code>:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">seek<span class="token punctuation">(</span>f<span class="token punctuation">,</span> fileSize<span class="token punctuation">(</span>f<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>Функция  <code>filePos(var f): LongInt</code> – возвращает порядковый номер компонента, который будет обрабатываться следующим</p>
</li>
<li>
<p>Процедура <code>truncate(var f)</code> – выполняет «<em>усечение</em>» файла.</p>
</li>
</ol>
<h3 id="нетипизированные-файлы">Нетипизированные файлы</h3>
<p><strong>Нетипизированными</strong>  называют файлы, объявленные без указания типа компонентов.</p>
<p>Операции чтения и записи с такими файлами осуществляются блоками, что позволяет организовать высокоскоростной обмен данными между диском и памятью. Отсутствие типа делает эти файлы совместимыми с любыми другими.</p>
<p>Нетипизированные файлы, как и типизированные,  допускают организацию прямого доступа.</p>
<p>Нетипизированный файл можно открыть для записи и для чтения:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">reSet<span class="token punctuation">(</span><span class="token keyword">var</span>  f<span class="token punctuation">[</span><span class="token punctuation">;</span> recsize<span class="token punctuation">:</span> Word<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal">reWrite<span class="token punctuation">(</span><span class="token keyword">var</span> f<span class="token punctuation">[</span><span class="token punctuation">;</span> recsize<span class="token punctuation">:</span> Word<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>где <code>recsize</code> – размер записи файла в байтах. Длину записи задают кратной 512 байт, например:  1024, 2048. Если длина записи не указана, она принимается равной 128.</p>
<h4 id="процедуры-и-функции-обработки-нетипизированных-файлов">Процедуры и функции обработки нетипизированных файлов</h4>
<ol>
<li>
<p>Процедура <code>blockRead(var f: file; var buf; count: Word[; var res: Word])</code> – осуществляет чтение блока записей из файла в буфер <code>buf</code>.<br>
Параметр <code>res</code> будет содержать количество фактически обработанных записей. Если последняя запись – неполная, то значение параметра <code>res</code> ее не учтет.</p>
</li>
<li>
<p>Процедура <code>blockWrite(var f: file; var buf; count: Word[; var res: Word])</code> – осуществляет запись блока из буфера <code>buf</code> в файл.</p>
</li>
</ol>
<h4 id="дополнительные-процедуры-и-функции-для-работы-с-файлами">Дополнительные процедуры и функции для работы с файлами</h4>
<ol>
<li>
<p><code>function changeFileExt(const fileName, extension: String): String</code> – изменяет существующее расширение файла на указанное.</p>
</li>
<li>
<p><code>procedure chDir(const s: String); overload;</code><br>
<code>procedure chDir(p: PChar); overload;</code> – изменяет текущий каталог (каталог по умолчанию).</p>
</li>
<li>
<p><code>function createDir(const dir: String): Boolean</code> – создает новый каталог.</p>
</li>
<li>
<p><code>function deleteFile(const fileName: String): Boolean</code> – удаляет указанный файл.</p>
</li>
<li>
<p><code>function directoryExists(const directory: String): Boolean</code> – проверяет существование каталога по указанному адресу.</p>
</li>
<li>
<p><code>function diskFree(drive: Byte): Int64</code> – возвращает объем в байтах свободного пространства на указанном диске:<br>
<code>0</code> – устройства по умолчанию; <code>1</code> – диск <code>А</code>; <code>2</code> – диск <code>В</code> и т.д. Функция возвращает <code>-1</code>, если указанный диск не существует.</p>
</li>
<li>
<p><code>function diskSize(drive: Byte): Int64</code> – возвращает объем памяти указанного диска.</p>
</li>
<li>
<p><code>function fileExists(const fileName: string): Boolean</code> – проверяет существование файла по указанному адресу.</p>
</li>
<li>
<p><code>function fileSearch(const name, dirList: String): String</code> – ищет файл в указанных через точку с запятой каталогах, если не находит, то возвращает пустую строку.</p>
</li>
<li>
<p><code>function findFirst(const path: string; attr: Integer; var f: TSearchRec): Integer</code> – ищет в каталоге первый файл с указанной маской и атрибутами;</p>
</li>
<li>
<p><code>function findNext(var F: TSearchRec): Integer</code> – ищет следующие файлы.</p>
</li>
<li>
<p><code>function getCurrentDir: String</code> – возвращает имя текущего каталога.</p>
</li>
<li>
<p><code>function forceDirectories(dir: String): Boolean</code> – создает каталоги и подкаталоги.</p>
</li>
<li>
<p><code>function removeDir(const dir: String): Boolean</code> – удаляет указанный пустой каталог.</p>
</li>
<li>
<p><code>function setCurrentDir(const dir: String): Boolean</code> – устанавливает текущий каталог.</p>
</li>
</ol>
<h2 id="основы-файловой-системы-файл-каталог-дисковод-полное-имя-файла-внутреннее-представление-информации-в-файле.-файловая-переменная.-операции-открытия-и-закрытия-файлов.-примеры.">22. Основы файловой системы: файл, каталог, дисковод, полное имя файла, внутреннее представление информации в файле. Файловая переменная. Операции открытия и закрытия файлов. Примеры.</h2>
<h2 id="текстовые-файлы.-внутреннее-представление-информации-в-файле.-операции-над--файлами.-пример.">23. Текстовые файлы. Внутреннее представление информации в файле. Операции над  файлами. Пример.</h2>
<h2 id="типизированные-файлы-внутреннее-представление-информации-в-файле.-операции--над-файлами.-пример.">24. Типизированные файлы: внутреннее представление информации в файле. Операции  над файлами. Пример.</h2>
<h2 id="нетипизированные-файлы.-внутреннее-представление-информации-в-файле.-операции-над-файлами.-пример.">25. Нетипизированные файлы. Внутреннее представление информации в файле. Операции над файлами. Пример.</h2>
<h1 id="объектно-ориентированное-программирование">Объектно-ориентированное программирование</h1>
<h2 id="история">История</h2>
<h3 id="«стихийное»-программирование">«Стихийное» программирование</h3>
<p><strong>«<em>Стихийное</em>» программирование</strong> – до середины 60-х годов ХХ века – технология отсутствует – программирование  – искусство создания программ – в конце периода появляется возможность создания подпрограмм – используется процедурная декомпозиция.</p>
<h3 id="структурный-подход">Структурный подход</h3>
<p>Структурный подход к программированию  - 60-70-е годы ХХ века – технология, представляющая собой набор рекомендаций и методов, базирующихся на большом опыте работы:</p>
<ul>
<li>нисходящая разработка;</li>
<li>декомпозиция методом пошаговой детализации;</li>
<li>структурное программирование;</li>
<li>сквозной структурный контроль и т. д.</li>
</ul>
<h3 id="модульный-подход">Модульный подход</h3>
<p><strong>Модульное программирование</strong> – выделение групп подпрограмм, использующих общие глобальные данные в модули – отдельно компилируемые части программы (многоуровневая декомпозиция).</p>
<h3 id="объектный-подход-к-программированию">Объектный подход к программированию</h3>
<p>C середины 80-х до наших дней.</p>
<p><strong>Объектно-ориентированное программирование</strong> – технология создания сложного программного обеспечения, основанная на представлении програм-мы в виде системы объек-тов, каждый из которых яв-ляется экземпляром опре-деленного типа (класса), а классы образуют иерар-хию с наследованием свойств.</p>
<h3 id="компонентный-подход">Компонентный подход</h3>
<p><strong>Компонентный подход</strong> – с  конца 90-х годов ХХ века (COM-технология, Corba, SOAP) – подключение объектов через универсальные интерфейсы – развитие сетевого программирования – появление CASE-технологий.</p>
<h2 id="диаграмма-состояний-интерфейса">Диаграмма состояний интерфейса</h2>
<p>пользователя</p>
<h2 id="структурная-декомпозиция">Структурная декомпозиция</h2>
<p><strong>Процедурная декомпозиция</strong> – процесс разбиения программы на подпрограммы.</p>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoic3RhdGVEaWFncmFtLXYyXG4gICAgaW5wdXQ6INCS0LLQvtC0INGE0YPQvdC60YbQuNC4XG4gICAgbWVudTog0JzQtdC90Y5cbiAgICB0YWJsZTog0KLQsNCx0LvQuNGG0LBcbiAgICByb290czog0JrQvtGA0L3QuFxuICAgIGV4OiDQrdC60YHRgtGA0LXQvNGD0LzRi1xuICAgIFsqXSAtLT4gaW5wdXRcbiAgICBpbnB1dCAtLT4gWypdXG4gICAgaW5wdXQgLS0-IG1lbnVcbiAgICBtZW51IC0tPiB0YWJsZVxuICAgIG1lbnUgLS0-IHJvb3RzXG4gICAgbWVudSAtLT4gZXhcbiAgICBtZW51IC0tPiBpbnB1dFxuICAgIHRhYmxlIC0tPiBtZW51XG4gICAgcm9vdHMgLS0-IG1lbnVcbiAgICBleCAtLT4gbWVudVxuICAgICAgICAgICAgIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQiLCJ0aGVtZVZhcmlhYmxlcyI6eyJiYWNrZ3JvdW5kIjoid2hpdGUiLCJwcmltYXJ5Q29sb3IiOiIjRUNFQ0ZGIiwic2Vjb25kYXJ5Q29sb3IiOiIjZmZmZmRlIiwidGVydGlhcnlDb2xvciI6ImhzbCg4MCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeUJvcmRlckNvbG9yIjoiaHNsKDI0MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJzZWNvbmRhcnlCb3JkZXJDb2xvciI6ImhzbCg2MCwgNjAlLCA4My41Mjk0MTE3NjQ3JSkiLCJ0ZXJ0aWFyeUJvcmRlckNvbG9yIjoiaHNsKDgwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInByaW1hcnlUZXh0Q29sb3IiOiIjMTMxMzAwIiwic2Vjb25kYXJ5VGV4dENvbG9yIjoiIzAwMDAyMSIsInRlcnRpYXJ5VGV4dENvbG9yIjoicmdiKDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEpIiwibGluZUNvbG9yIjoiIzMzMzMzMyIsInRleHRDb2xvciI6IiMzMzMiLCJtYWluQmtnIjoiI0VDRUNGRiIsInNlY29uZEJrZyI6IiNmZmZmZGUiLCJib3JkZXIxIjoiIzkzNzBEQiIsImJvcmRlcjIiOiIjYWFhYTMzIiwiYXJyb3doZWFkQ29sb3IiOiIjMzMzMzMzIiwiZm9udEZhbWlseSI6IlwidHJlYnVjaGV0IG1zXCIsIHZlcmRhbmEsIGFyaWFsIiwiZm9udFNpemUiOiIxNnB4IiwibGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsIm5vZGVCa2ciOiIjRUNFQ0ZGIiwibm9kZUJvcmRlciI6IiM5MzcwREIiLCJjbHVzdGVyQmtnIjoiI2ZmZmZkZSIsImNsdXN0ZXJCb3JkZXIiOiIjYWFhYTMzIiwiZGVmYXVsdExpbmtDb2xvciI6IiMzMzMzMzMiLCJ0aXRsZUNvbG9yIjoiIzMzMyIsImVkZ2VMYWJlbEJhY2tncm91bmQiOiIjZThlOGU4IiwiYWN0b3JCb3JkZXIiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJhY3RvckJrZyI6IiNFQ0VDRkYiLCJhY3RvclRleHRDb2xvciI6ImJsYWNrIiwiYWN0b3JMaW5lQ29sb3IiOiJncmV5Iiwic2lnbmFsQ29sb3IiOiIjMzMzIiwic2lnbmFsVGV4dENvbG9yIjoiIzMzMyIsImxhYmVsQm94QmtnQ29sb3IiOiIjRUNFQ0ZGIiwibGFiZWxCb3hCb3JkZXJDb2xvciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImxhYmVsVGV4dENvbG9yIjoiYmxhY2siLCJsb29wVGV4dENvbG9yIjoiYmxhY2siLCJub3RlQm9yZGVyQ29sb3IiOiIjYWFhYTMzIiwibm90ZUJrZ0NvbG9yIjoiI2ZmZjVhZCIsIm5vdGVUZXh0Q29sb3IiOiJibGFjayIsImFjdGl2YXRpb25Cb3JkZXJDb2xvciI6IiM2NjYiLCJhY3RpdmF0aW9uQmtnQ29sb3IiOiIjZjRmNGY0Iiwic2VxdWVuY2VOdW1iZXJDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yIjoicmdiYSgxMDIsIDEwMiwgMjU1LCAwLjQ5KSIsImFsdFNlY3Rpb25Ca2dDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yMiI6IiNmZmY0MDAiLCJ0YXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwidGFza0JrZ0NvbG9yIjoiIzhhOTBkZCIsInRhc2tUZXh0TGlnaHRDb2xvciI6IndoaXRlIiwidGFza1RleHRDb2xvciI6IndoaXRlIiwidGFza1RleHREYXJrQ29sb3IiOiJibGFjayIsInRhc2tUZXh0T3V0c2lkZUNvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dENsaWNrYWJsZUNvbG9yIjoiIzAwMzE2MyIsImFjdGl2ZVRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJhY3RpdmVUYXNrQmtnQ29sb3IiOiIjYmZjN2ZmIiwiZ3JpZENvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCa2dDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQm9yZGVyQ29sb3IiOiJncmV5IiwiY3JpdEJvcmRlckNvbG9yIjoiI2ZmODg4OCIsImNyaXRCa2dDb2xvciI6InJlZCIsInRvZGF5TGluZUNvbG9yIjoicmVkIiwibGFiZWxDb2xvciI6ImJsYWNrIiwiZXJyb3JCa2dDb2xvciI6IiM1NTIyMjIiLCJlcnJvclRleHRDb2xvciI6IiM1NTIyMjIiLCJjbGFzc1RleHQiOiIjMTMxMzAwIiwiZmlsbFR5cGUwIjoiI0VDRUNGRiIsImZpbGxUeXBlMSI6IiNmZmZmZGUiLCJmaWxsVHlwZTIiOiJoc2woMzA0LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTMiOiJoc2woMTI0LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTQiOiJoc2woMTc2LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTUiOiJoc2woLTQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNiI6ImhzbCg4LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTciOiJoc2woMTg4LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkifX0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9" alt=""></p>
<p><strong>Структурной</strong> называют декомпозицию,  если:</p>
<ul>
<li>каждая подпрограмма имеет один вход и один выход;</li>
<li>подпрограммы нижних уровней не вызывают подпрограмм верхних уровней;</li>
<li>размер подпрограммы не превышает 40-50 операторов;</li>
<li>в алгоритме использованы только структурные конструкции.</li>
</ul>
<h2 id="объектная-декомпозиция">Объектная декомпозиция</h2>
<p><strong>Объектная декомпозиция</strong> – процесс  представления предметной области задачи в виде отдельных функциональных элементов (объектов предметной области), обменивающихся в процессе выполнения программы входными воздействиями (сообщениями) .</p>
<p>Объект отвечает за выполнение некоторых действий, инициируемых сообщениями и зависящих от параметров объекта.</p>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-iK9XUtp8Bs21lpAW" width="100%" style="max-width: 485.515625px;" viewBox="0 0 485.515625 524"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M341.6796875,40L341.6796875,46.333333333333336C341.6796875,52.666666666666664,341.6796875,65.33333333333333,341.6796875,78C341.6796875,90.66666666666667,341.6796875,103.33333333333333,341.6796875,109.66666666666667L341.6796875,116" marker-end="url(#arrowhead464)" style="fill:none"></path><defs><marker id="arrowhead464" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M295.4469774590164,162L282.716231215847,168.33333333333334C269.9854849726776,174.66666666666666,244.52399248633878,187.33333333333334,231.7932462431694,200C219.0625,212.66666666666666,219.0625,225.33333333333334,219.0625,231.66666666666666L219.0625,238" marker-end="url(#arrowhead465)" style="fill:none"></path><defs><marker id="arrowhead465" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M186.765625,275.1353139013453L168.91927083333334,282.9460949177878C151.07291666666666,290.7568759342302,115.38020833333333,306.3784379671151,97.53385416666667,320.5225523168909C79.6875,334.6666666666667,79.6875,347.3333333333333,79.6875,353.6666666666667L79.6875,360" marker-end="url(#arrowhead466)" style="fill:none"></path><defs><marker id="arrowhead466" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M219.0625,284L219.0625,290.3333333333333C219.0625,296.6666666666667,219.0625,309.3333333333333,219.0625,322C219.0625,334.6666666666667,219.0625,347.3333333333333,219.0625,353.6666666666667L219.0625,360" marker-end="url(#arrowhead467)" style="fill:none"></path><defs><marker id="arrowhead467" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M251.359375,275.03930519986636L269.3645833333333,282.8660876665553C287.3697916666667,290.69287013324424,323.3802083333333,306.3464350666221,341.3854166666667,320.5065508666444C359.390625,334.6666666666667,359.390625,347.3333333333333,359.390625,353.6666666666667L359.390625,360" marker-end="url(#arrowhead468)" style="fill:none"></path><defs><marker id="arrowhead468" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M79.6875,406L79.6875,412.3333333333333C79.6875,418.6666666666667,79.6875,431.3333333333333,107.54166666666667,445.7754371574513C135.39583333333334,460.21754098156913,191.10416666666666,476.4350819631383,218.95833333333334,484.5438524539229L246.8125,492.6526229447075" marker-end="url(#arrowhead469)" style="fill:none"></path><defs><marker id="arrowhead469" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M219.0625,406L219.0625,412.3333333333333C219.0625,418.6666666666667,219.0625,431.3333333333333,226.34729337431693,444C233.6320867486339,456.6666666666667,248.20167349726776,469.3333333333333,255.48646687158472,475.6666666666667L262.77126024590166,482" marker-end="url(#arrowhead470)" style="fill:none"></path><defs><marker id="arrowhead470" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M359.390625,406L359.390625,412.3333333333333C359.390625,418.6666666666667,359.390625,431.3333333333333,352.1058316256831,444C344.82103825136613,456.6666666666667,330.2514515027322,469.3333333333333,322.9666581284153,475.6666666666667L315.68186475409834,482" marker-end="url(#arrowhead471)" style="fill:none"></path><defs><marker id="arrowhead471" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M387.9123975409836,162L400.643143784153,168.33333333333334C413.37389002732243,174.66666666666666,438.8353825136612,187.33333333333334,451.56612875683055,203.83333333333334C464.296875,220.33333333333334,464.296875,240.66666666666666,464.296875,261C464.296875,281.3333333333333,464.296875,301.6666666666667,464.296875,322C464.296875,342.3333333333333,464.296875,362.6666666666667,464.296875,383C464.296875,403.3333333333333,464.296875,423.6666666666667,442.1875,441.5369345649813C420.078125,459.407202463296,375.859375,474.81440492659203,353.75,482.51800615824004L331.640625,490.221607389888" marker-end="url(#arrowhead472)" style="fill:none"></path><defs><marker id="arrowhead472" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="translate(341.6796875,78)" style="opacity: 1;"><g transform="translate(-59.6875,-13)" class="label"><foreignObject width="119.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Активизировать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(219.0625,200)" style="opacity: 1;"><g transform="translate(-59.6875,-13)" class="label"><foreignObject width="119.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Активизировать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(79.6875,322)" style="opacity: 1;"><g transform="translate(-59.6875,-13)" class="label"><foreignObject width="119.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Активизировать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(219.0625,322)" style="opacity: 1;"><g transform="translate(-59.6875,-13)" class="label"><foreignObject width="119.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Активизировать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(359.390625,322)" style="opacity: 1;"><g transform="translate(-59.6875,-13)" class="label"><foreignObject width="119.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Активизировать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(79.6875,444)" style="opacity: 1;"><g transform="translate(-40.703125,-13)" class="label"><foreignObject width="81.40625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Рассчитать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(219.0625,444)" style="opacity: 1;"><g transform="translate(-40.703125,-13)" class="label"><foreignObject width="81.40625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Рассчитать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(359.390625,444)" style="opacity: 1;"><g transform="translate(-40.703125,-13)" class="label"><foreignObject width="81.40625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Рассчитать</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(464.296875,322)" style="opacity: 1;"><g transform="translate(-25.21875,-13)" class="label"><foreignObject width="50.4375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">Задать</span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="o" transform="translate(341.6796875,30)" style="opacity: 1;"><rect rx="0" ry="0" x="-10" y="-10" width="20" height="20"></rect><g class="label" transform="translate(0,0)"><g transform="translate(0,0)"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"></div></foreignObject></g></g></g><g class="node" id="base" transform="translate(341.6796875,139)" style="opacity: 1;"><rect rx="0" ry="0" x="-62.7578125" y="-23" width="125.515625" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-52.7578125,-13)"><foreignObject width="105.515625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Ввод функции</div></foreignObject></g></g></g><g class="node" id="menu" transform="translate(219.0625,261)" style="opacity: 1;"><rect rx="0" ry="0" x="-32.296875" y="-23" width="64.59375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-22.296875,-13)"><foreignObject width="44.59375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Меню</div></foreignObject></g></g></g><g class="node" id="table" transform="translate(79.6875,383)" style="opacity: 1;"><rect rx="0" ry="0" x="-40.453125" y="-23" width="80.90625" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-30.453125,-13)"><foreignObject width="60.90625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Таблица</div></foreignObject></g></g></g><g class="node" id="roots" transform="translate(219.0625,383)" style="opacity: 1;"><rect rx="0" ry="0" x="-33.1875" y="-23" width="66.375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-23.1875,-13)"><foreignObject width="46.375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Корни</div></foreignObject></g></g></g><g class="node" id="ex" transform="translate(359.390625,383)" style="opacity: 1;"><rect rx="0" ry="0" x="-57.140625" y="-23" width="114.28125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-47.140625,-13)"><foreignObject width="94.28125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Экстремумы</div></foreignObject></g></g></g><g class="node" id="func" transform="translate(289.2265625,505)" style="opacity: 1;"><rect rx="0" ry="0" x="-42.4140625" y="-23" width="84.828125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-32.4140625,-13)"><foreignObject width="64.828125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Функция</div></foreignObject></g></g></g></g></g></g></svg></div>
<h2 id="объект-предметной-области">Объект предметной области</h2>
<p><strong>Объект предметной области</strong> характеризуется:</p>
<ul>
<li>именем;</li>
<li>состоянием;</li>
<li>поведением.</li>
</ul>
<p><strong>Состояние</strong> – совокупность значений характеристик объекта, существенных с т. з. решаемой задачи.</p>
<p><strong>Поведение</strong> – совокупность реакций на сообщения.</p>
<h3 id="реализация-объектов-предметной-области">Реализация объектов предметной области</h3>
<!--- &#1050;&#1072;&#1088;&#1090;&#1080;&#1085;&#1082;&#1072; -->
<p><strong>Класс</strong> – это структурный тип данных, который включает описание полей данных, а также процедур и функций, работающих с этими полями данных.</p>
<p>Применительно к классам такие процедуры и функции получили название <strong>методов</strong>.</p>
<p><strong>Объект-переменная</strong> – переменная типа «класс».</p>
<h2 id="методы-построения-классов">Методы построения классов</h2>
<ol>
<li>
<p><strong>Наследование</strong> – механизм, позволяющий  строить класс на базе более простого посредством добавления полей и определения новых методов.</p>
<p>При этом исходный класс, на базе которого выполняется построение, называют <em>родительским</em> или <em>базовым</em>, а строящейся класс – <em>потомком</em> или <em>производным</em> классом.</p>
<p>Если при наследовании какие-либо методы переопределяются, то такое наследование называется полиморфным.</p>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAg0JrQu9Cw0YHRgdCg0L7QtNC40YLQtdC70YwgPHwtLSDQmtC70LDRgdGB0J_QvtGC0L7QvNC-0LoiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCIsInRoZW1lVmFyaWFibGVzIjp7ImJhY2tncm91bmQiOiJ3aGl0ZSIsInByaW1hcnlDb2xvciI6IiNFQ0VDRkYiLCJzZWNvbmRhcnlDb2xvciI6IiNmZmZmZGUiLCJ0ZXJ0aWFyeUNvbG9yIjoiaHNsKDgwLCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5Qm9yZGVyQ29sb3IiOiJoc2woMjQwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInNlY29uZGFyeUJvcmRlckNvbG9yIjoiaHNsKDYwLCA2MCUsIDgzLjUyOTQxMTc2NDclKSIsInRlcnRpYXJ5Qm9yZGVyQ29sb3IiOiJoc2woODAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeVRleHRDb2xvciI6IiMxMzEzMDAiLCJzZWNvbmRhcnlUZXh0Q29sb3IiOiIjMDAwMDIxIiwidGVydGlhcnlUZXh0Q29sb3IiOiJyZ2IoOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSkiLCJsaW5lQ29sb3IiOiIjMzMzMzMzIiwidGV4dENvbG9yIjoiIzMzMyIsIm1haW5Ca2ciOiIjRUNFQ0ZGIiwic2Vjb25kQmtnIjoiI2ZmZmZkZSIsImJvcmRlcjEiOiIjOTM3MERCIiwiYm9yZGVyMiI6IiNhYWFhMzMiLCJhcnJvd2hlYWRDb2xvciI6IiMzMzMzMzMiLCJmb250RmFtaWx5IjoiXCJ0cmVidWNoZXQgbXNcIiwgdmVyZGFuYSwgYXJpYWwiLCJmb250U2l6ZSI6IjE2cHgiLCJsYWJlbEJhY2tncm91bmQiOiIjZThlOGU4Iiwibm9kZUJrZyI6IiNFQ0VDRkYiLCJub2RlQm9yZGVyIjoiIzkzNzBEQiIsImNsdXN0ZXJCa2ciOiIjZmZmZmRlIiwiY2x1c3RlckJvcmRlciI6IiNhYWFhMzMiLCJkZWZhdWx0TGlua0NvbG9yIjoiIzMzMzMzMyIsInRpdGxlQ29sb3IiOiIjMzMzIiwiZWRnZUxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJhY3RvckJvcmRlciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImFjdG9yQmtnIjoiI0VDRUNGRiIsImFjdG9yVGV4dENvbG9yIjoiYmxhY2siLCJhY3RvckxpbmVDb2xvciI6ImdyZXkiLCJzaWduYWxDb2xvciI6IiMzMzMiLCJzaWduYWxUZXh0Q29sb3IiOiIjMzMzIiwibGFiZWxCb3hCa2dDb2xvciI6IiNFQ0VDRkYiLCJsYWJlbEJveEJvcmRlckNvbG9yIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwibGFiZWxUZXh0Q29sb3IiOiJibGFjayIsImxvb3BUZXh0Q29sb3IiOiJibGFjayIsIm5vdGVCb3JkZXJDb2xvciI6IiNhYWFhMzMiLCJub3RlQmtnQ29sb3IiOiIjZmZmNWFkIiwibm90ZVRleHRDb2xvciI6ImJsYWNrIiwiYWN0aXZhdGlvbkJvcmRlckNvbG9yIjoiIzY2NiIsImFjdGl2YXRpb25Ca2dDb2xvciI6IiNmNGY0ZjQiLCJzZXF1ZW5jZU51bWJlckNvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IiOiJyZ2JhKDEwMiwgMTAyLCAyNTUsIDAuNDkpIiwiYWx0U2VjdGlvbkJrZ0NvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IyIjoiI2ZmZjQwMCIsInRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJ0YXNrQmtnQ29sb3IiOiIjOGE5MGRkIiwidGFza1RleHRMaWdodENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dERhcmtDb2xvciI6ImJsYWNrIiwidGFza1RleHRPdXRzaWRlQ29sb3IiOiJibGFjayIsInRhc2tUZXh0Q2xpY2thYmxlQ29sb3IiOiIjMDAzMTYzIiwiYWN0aXZlVGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsImFjdGl2ZVRhc2tCa2dDb2xvciI6IiNiZmM3ZmYiLCJncmlkQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JrZ0NvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCb3JkZXJDb2xvciI6ImdyZXkiLCJjcml0Qm9yZGVyQ29sb3IiOiIjZmY4ODg4IiwiY3JpdEJrZ0NvbG9yIjoicmVkIiwidG9kYXlMaW5lQ29sb3IiOiJyZWQiLCJsYWJlbENvbG9yIjoiYmxhY2siLCJlcnJvckJrZ0NvbG9yIjoiIzU1MjIyMiIsImVycm9yVGV4dENvbG9yIjoiIzU1MjIyMiIsImNsYXNzVGV4dCI6IiMxMzEzMDAiLCJmaWxsVHlwZTAiOiIjRUNFQ0ZGIiwiZmlsbFR5cGUxIjoiI2ZmZmZkZSIsImZpbGxUeXBlMiI6ImhzbCgzMDQsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlMyI6ImhzbCgxMjQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNCI6ImhzbCgxNzYsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNSI6ImhzbCgtNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU2IjoiaHNsKDgsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNyI6ImhzbCgxODgsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSJ9fSwidXBkYXRlRWRpdG9yIjpmYWxzZX0" alt=""></p>
</li>
<li>
<p><strong>Композиция</strong> –  механизм, позволяющий включать несколько объектов других классов в конструируемый.<br>
<img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAg0J7RgdC90L7QstC90L7QudCa0LvQsNGB0YEgXCIxXCIgKi0tIFwiMVwiINCa0LvQsNGB0YHQp9Cw0YHRgtGMIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQiLCJ0aGVtZVZhcmlhYmxlcyI6eyJiYWNrZ3JvdW5kIjoid2hpdGUiLCJwcmltYXJ5Q29sb3IiOiIjRUNFQ0ZGIiwic2Vjb25kYXJ5Q29sb3IiOiIjZmZmZmRlIiwidGVydGlhcnlDb2xvciI6ImhzbCg4MCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeUJvcmRlckNvbG9yIjoiaHNsKDI0MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJzZWNvbmRhcnlCb3JkZXJDb2xvciI6ImhzbCg2MCwgNjAlLCA4My41Mjk0MTE3NjQ3JSkiLCJ0ZXJ0aWFyeUJvcmRlckNvbG9yIjoiaHNsKDgwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInByaW1hcnlUZXh0Q29sb3IiOiIjMTMxMzAwIiwic2Vjb25kYXJ5VGV4dENvbG9yIjoiIzAwMDAyMSIsInRlcnRpYXJ5VGV4dENvbG9yIjoicmdiKDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEpIiwibGluZUNvbG9yIjoiIzMzMzMzMyIsInRleHRDb2xvciI6IiMzMzMiLCJtYWluQmtnIjoiI0VDRUNGRiIsInNlY29uZEJrZyI6IiNmZmZmZGUiLCJib3JkZXIxIjoiIzkzNzBEQiIsImJvcmRlcjIiOiIjYWFhYTMzIiwiYXJyb3doZWFkQ29sb3IiOiIjMzMzMzMzIiwiZm9udEZhbWlseSI6IlwidHJlYnVjaGV0IG1zXCIsIHZlcmRhbmEsIGFyaWFsIiwiZm9udFNpemUiOiIzMnB4IiwibGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsIm5vZGVCa2ciOiIjRUNFQ0ZGIiwibm9kZUJvcmRlciI6IiM5MzcwREIiLCJjbHVzdGVyQmtnIjoiI2ZmZmZkZSIsImNsdXN0ZXJCb3JkZXIiOiIjYWFhYTMzIiwiZGVmYXVsdExpbmtDb2xvciI6IiMzMzMzMzMiLCJ0aXRsZUNvbG9yIjoiIzMzMyIsImVkZ2VMYWJlbEJhY2tncm91bmQiOiIjZThlOGU4IiwiYWN0b3JCb3JkZXIiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJhY3RvckJrZyI6IiNFQ0VDRkYiLCJhY3RvclRleHRDb2xvciI6ImJsYWNrIiwiYWN0b3JMaW5lQ29sb3IiOiJncmV5Iiwic2lnbmFsQ29sb3IiOiIjMzMzIiwic2lnbmFsVGV4dENvbG9yIjoiIzMzMyIsImxhYmVsQm94QmtnQ29sb3IiOiIjRUNFQ0ZGIiwibGFiZWxCb3hCb3JkZXJDb2xvciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImxhYmVsVGV4dENvbG9yIjoiYmxhY2siLCJsb29wVGV4dENvbG9yIjoiYmxhY2siLCJub3RlQm9yZGVyQ29sb3IiOiIjYWFhYTMzIiwibm90ZUJrZ0NvbG9yIjoiI2ZmZjVhZCIsIm5vdGVUZXh0Q29sb3IiOiJibGFjayIsImFjdGl2YXRpb25Cb3JkZXJDb2xvciI6IiM2NjYiLCJhY3RpdmF0aW9uQmtnQ29sb3IiOiIjZjRmNGY0Iiwic2VxdWVuY2VOdW1iZXJDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yIjoicmdiYSgxMDIsIDEwMiwgMjU1LCAwLjQ5KSIsImFsdFNlY3Rpb25Ca2dDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yMiI6IiNmZmY0MDAiLCJ0YXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwidGFza0JrZ0NvbG9yIjoiIzhhOTBkZCIsInRhc2tUZXh0TGlnaHRDb2xvciI6IndoaXRlIiwidGFza1RleHRDb2xvciI6IndoaXRlIiwidGFza1RleHREYXJrQ29sb3IiOiJibGFjayIsInRhc2tUZXh0T3V0c2lkZUNvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dENsaWNrYWJsZUNvbG9yIjoiIzAwMzE2MyIsImFjdGl2ZVRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJhY3RpdmVUYXNrQmtnQ29sb3IiOiIjYmZjN2ZmIiwiZ3JpZENvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCa2dDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQm9yZGVyQ29sb3IiOiJncmV5IiwiY3JpdEJvcmRlckNvbG9yIjoiI2ZmODg4OCIsImNyaXRCa2dDb2xvciI6InJlZCIsInRvZGF5TGluZUNvbG9yIjoicmVkIiwibGFiZWxDb2xvciI6ImJsYWNrIiwiZXJyb3JCa2dDb2xvciI6IiM1NTIyMjIiLCJlcnJvclRleHRDb2xvciI6IiM1NTIyMjIiLCJjbGFzc1RleHQiOiIjMTMxMzAwIiwiZmlsbFR5cGUwIjoiI0VDRUNGRiIsImZpbGxUeXBlMSI6IiNmZmZmZGUiLCJmaWxsVHlwZTIiOiJoc2woMzA0LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTMiOiJoc2woMTI0LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTQiOiJoc2woMTc2LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTUiOiJoc2woLTQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNiI6ImhzbCg4LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTciOiJoc2woMTg4LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkifX0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9" alt=""></p>
</li>
<li>
<p><strong>Наполнение</strong> – механизм, позволяющих включать указатели на объекты других классов в конструируемый.<br>
<img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAg0JrQu9Cw0YHRgdCQ0LPRgNC10LPQsNGCIG8tLSBcIjAuLipcIiDQmtC70LDRgdGB0KfQsNGB0YLRjCIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0IiwidGhlbWVWYXJpYWJsZXMiOnsiYmFja2dyb3VuZCI6IndoaXRlIiwicHJpbWFyeUNvbG9yIjoiI0VDRUNGRiIsInNlY29uZGFyeUNvbG9yIjoiI2ZmZmZkZSIsInRlcnRpYXJ5Q29sb3IiOiJoc2woODAsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsInByaW1hcnlCb3JkZXJDb2xvciI6ImhzbCgyNDAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwic2Vjb25kYXJ5Qm9yZGVyQ29sb3IiOiJoc2woNjAsIDYwJSwgODMuNTI5NDExNzY0NyUpIiwidGVydGlhcnlCb3JkZXJDb2xvciI6ImhzbCg4MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5VGV4dENvbG9yIjoiIzEzMTMwMCIsInNlY29uZGFyeVRleHRDb2xvciI6IiMwMDAwMjEiLCJ0ZXJ0aWFyeVRleHRDb2xvciI6InJnYig5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxKSIsImxpbmVDb2xvciI6IiMzMzMzMzMiLCJ0ZXh0Q29sb3IiOiIjMzMzIiwibWFpbkJrZyI6IiNFQ0VDRkYiLCJzZWNvbmRCa2ciOiIjZmZmZmRlIiwiYm9yZGVyMSI6IiM5MzcwREIiLCJib3JkZXIyIjoiI2FhYWEzMyIsImFycm93aGVhZENvbG9yIjoiIzMzMzMzMyIsImZvbnRGYW1pbHkiOiJcInRyZWJ1Y2hldCBtc1wiLCB2ZXJkYW5hLCBhcmlhbCIsImZvbnRTaXplIjoiMzJweCIsImxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJub2RlQmtnIjoiI0VDRUNGRiIsIm5vZGVCb3JkZXIiOiIjOTM3MERCIiwiY2x1c3RlckJrZyI6IiNmZmZmZGUiLCJjbHVzdGVyQm9yZGVyIjoiI2FhYWEzMyIsImRlZmF1bHRMaW5rQ29sb3IiOiIjMzMzMzMzIiwidGl0bGVDb2xvciI6IiMzMzMiLCJlZGdlTGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsImFjdG9yQm9yZGVyIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwiYWN0b3JCa2ciOiIjRUNFQ0ZGIiwiYWN0b3JUZXh0Q29sb3IiOiJibGFjayIsImFjdG9yTGluZUNvbG9yIjoiZ3JleSIsInNpZ25hbENvbG9yIjoiIzMzMyIsInNpZ25hbFRleHRDb2xvciI6IiMzMzMiLCJsYWJlbEJveEJrZ0NvbG9yIjoiI0VDRUNGRiIsImxhYmVsQm94Qm9yZGVyQ29sb3IiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJsYWJlbFRleHRDb2xvciI6ImJsYWNrIiwibG9vcFRleHRDb2xvciI6ImJsYWNrIiwibm90ZUJvcmRlckNvbG9yIjoiI2FhYWEzMyIsIm5vdGVCa2dDb2xvciI6IiNmZmY1YWQiLCJub3RlVGV4dENvbG9yIjoiYmxhY2siLCJhY3RpdmF0aW9uQm9yZGVyQ29sb3IiOiIjNjY2IiwiYWN0aXZhdGlvbkJrZ0NvbG9yIjoiI2Y0ZjRmNCIsInNlcXVlbmNlTnVtYmVyQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvciI6InJnYmEoMTAyLCAxMDIsIDI1NSwgMC40OSkiLCJhbHRTZWN0aW9uQmtnQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvcjIiOiIjZmZmNDAwIiwidGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsInRhc2tCa2dDb2xvciI6IiM4YTkwZGQiLCJ0YXNrVGV4dExpZ2h0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0RGFya0NvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dE91dHNpZGVDb2xvciI6ImJsYWNrIiwidGFza1RleHRDbGlja2FibGVDb2xvciI6IiMwMDMxNjMiLCJhY3RpdmVUYXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwiYWN0aXZlVGFza0JrZ0NvbG9yIjoiI2JmYzdmZiIsImdyaWRDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQmtnQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JvcmRlckNvbG9yIjoiZ3JleSIsImNyaXRCb3JkZXJDb2xvciI6IiNmZjg4ODgiLCJjcml0QmtnQ29sb3IiOiJyZWQiLCJ0b2RheUxpbmVDb2xvciI6InJlZCIsImxhYmVsQ29sb3IiOiJibGFjayIsImVycm9yQmtnQ29sb3IiOiIjNTUyMjIyIiwiZXJyb3JUZXh0Q29sb3IiOiIjNTUyMjIyIiwiY2xhc3NUZXh0IjoiIzEzMTMwMCIsImZpbGxUeXBlMCI6IiNFQ0VDRkYiLCJmaWxsVHlwZTEiOiIjZmZmZmRlIiwiZmlsbFR5cGUyIjoiaHNsKDMwNCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGUzIjoiaHNsKDEyNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU0IjoiaHNsKDE3NiwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU1IjoiaHNsKC00LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTYiOiJoc2woOCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU3IjoiaHNsKDE4OCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIn19LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ" alt=""></p>
</li>
</ol>
<h2 id="средства-объектно-ориентированного-программирования">Средства объектно-ориентированного программирования</h2>
<p>C точки зрения синтаксиса <strong>класс</strong> – структурный тип данных, в котором помимо полей разрешается описывать <em>прототипы</em> (заголовки) процедур и функций, работающих с этими полями данных.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span> 
    TRoom <span class="token operator">=</span> <span class="token keyword">object</span>
        length<span class="token punctuation">,</span> width<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>  <span class="token comment">{прототип функции}</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TRoom<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>
<span class="token keyword">End</span><span class="token punctuation">;</span>
</code></pre>
<p>Любой метод неявно получает параметр <strong><code>self</code></strong> – ссылку (адрес) на поля объекта, и обращение к полям происходит через это имя.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">function</span> TRoom<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> <span class="token keyword">self</span><span class="token punctuation">.</span>length <span class="token operator">*</span> <span class="token keyword">self</span><span class="token punctuation">.</span>width<span class="token punctuation">;</span>
<span class="token keyword">End</span><span class="token punctuation">;</span>
</code></pre>
<p>При необходимости эту ссылку можно указывать явно:</p>
<p><code>@self</code> – адрес области полей данных объекта.</p>
<h3 id="объявление-объектов-класса">Объявление объектов класса</h3>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span> 
    a<span class="token punctuation">:</span> TRoom<span class="token punctuation">;</span> <span class="token comment">{объект А класса TRoom}</span>
    b<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">]</span> <span class="token keyword">of</span> TRoom<span class="token punctuation">;</span>  <span class="token comment">{массив  объектов  типа  TRoom}</span>

<span class="token keyword">type</span> pTRoom<span class="token operator">=</span><span class="token string">^T</span>Room<span class="token punctuation">;</span>  <span class="token comment">{тип указателя на объекты класса TRoom}</span>

<span class="token keyword">var</span>  pC<span class="token punctuation">:</span> pTRoom<span class="token punctuation">;</span>  <span class="token comment">{указатель на объекта класса TRoom}</span>
</code></pre>
<p>Для динамического объекта необходимо выделить память:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">new</span><span class="token punctuation">(</span>pC<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>, а после его использования – освободить память:</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">dispose</span><span class="token punctuation">(</span>pC<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>Обращение к полям и методам аналогично доступу к полям записей:<br>
Примеры:</p>
<pre class=" language-pascal"><code class="prism  language-pascal">v <span class="token operator">:=</span> a<span class="token punctuation">.</span>length<span class="token punctuation">;</span>
s <span class="token operator">:=</span> a<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
s <span class="token operator">:=</span> s <span class="token operator">+</span> b<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">.</span>square<span class="token punctuation">;</span>
pC<span class="token operator">^</span><span class="token punctuation">.</span>length <span class="token operator">:=</span> <span class="token number">3</span><span class="token punctuation">;</span>
</code></pre>
<p>Над объектами одного класса определена операция <strong>присваивания</strong>. Физически при этом происходит копирование полей одного объекта в другой методом «поле за полем»:</p>
<h3 id="инкапсуляция----ограничение-доступа-к-полям-и-методам">Инкапсуляция – ограничение доступа к полям и методам</h3>

<table>
<thead>
<tr>
<th>Модификатор доступа</th>
<th>Доступность</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>public</code></td>
<td>поля и методы, доступны из других модулей</td>
</tr>
<tr>
<td><code>private</code></td>
<td>поля и методы, доступны только в пределах модуля</td>
</tr>
<tr>
<td><code>protected</code></td>
<td>поля и методы, доступны только в классах потомках</td>
</tr>
<tr>
<td><code>published</code></td>
<td>поля и методы, видимы в инспекторе объектов</td>
</tr>
</tbody>
</table><!--- published ???-->
<p>По умолчанию для всех полей испаользуется модификатор <code>public</code>.</p>
<p><s><strong>Ограничение только в пределах модуля!</strong></s></p>
<blockquote>
<p>Хотя, вроде, нет. Наоборот, только в пределах модуля можно пользоваться приватными полями.</p>
</blockquote>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgY2xhc3MgVFJvb217XG4gICAgICAgICAtbGVuZ3RoLCB3aWR0aDogU2luZ2xlXG4gICAgICAgICtzcXVhcmUoKTogU2luZ2xlXG4gICAgICAgICtpbml0KGwsIHcpXG4gICAgfSIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0IiwidGhlbWVWYXJpYWJsZXMiOnsiYmFja2dyb3VuZCI6IndoaXRlIiwicHJpbWFyeUNvbG9yIjoiI0VDRUNGRiIsInNlY29uZGFyeUNvbG9yIjoiI2ZmZmZkZSIsInRlcnRpYXJ5Q29sb3IiOiJoc2woODAsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsInByaW1hcnlCb3JkZXJDb2xvciI6ImhzbCgyNDAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwic2Vjb25kYXJ5Qm9yZGVyQ29sb3IiOiJoc2woNjAsIDYwJSwgODMuNTI5NDExNzY0NyUpIiwidGVydGlhcnlCb3JkZXJDb2xvciI6ImhzbCg4MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5VGV4dENvbG9yIjoiIzEzMTMwMCIsInNlY29uZGFyeVRleHRDb2xvciI6IiMwMDAwMjEiLCJ0ZXJ0aWFyeVRleHRDb2xvciI6InJnYig5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxKSIsImxpbmVDb2xvciI6IiMzMzMzMzMiLCJ0ZXh0Q29sb3IiOiIjMzMzIiwibWFpbkJrZyI6IiNFQ0VDRkYiLCJzZWNvbmRCa2ciOiIjZmZmZmRlIiwiYm9yZGVyMSI6IiM5MzcwREIiLCJib3JkZXIyIjoiI2FhYWEzMyIsImFycm93aGVhZENvbG9yIjoiIzMzMzMzMyIsImZvbnRGYW1pbHkiOiJcInRyZWJ1Y2hldCBtc1wiLCB2ZXJkYW5hLCBhcmlhbCIsImZvbnRTaXplIjoiMzJweCIsImxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJub2RlQmtnIjoiI0VDRUNGRiIsIm5vZGVCb3JkZXIiOiIjOTM3MERCIiwiY2x1c3RlckJrZyI6IiNmZmZmZGUiLCJjbHVzdGVyQm9yZGVyIjoiI2FhYWEzMyIsImRlZmF1bHRMaW5rQ29sb3IiOiIjMzMzMzMzIiwidGl0bGVDb2xvciI6IiMzMzMiLCJlZGdlTGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsImFjdG9yQm9yZGVyIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwiYWN0b3JCa2ciOiIjRUNFQ0ZGIiwiYWN0b3JUZXh0Q29sb3IiOiJibGFjayIsImFjdG9yTGluZUNvbG9yIjoiZ3JleSIsInNpZ25hbENvbG9yIjoiIzMzMyIsInNpZ25hbFRleHRDb2xvciI6IiMzMzMiLCJsYWJlbEJveEJrZ0NvbG9yIjoiI0VDRUNGRiIsImxhYmVsQm94Qm9yZGVyQ29sb3IiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJsYWJlbFRleHRDb2xvciI6ImJsYWNrIiwibG9vcFRleHRDb2xvciI6ImJsYWNrIiwibm90ZUJvcmRlckNvbG9yIjoiI2FhYWEzMyIsIm5vdGVCa2dDb2xvciI6IiNmZmY1YWQiLCJub3RlVGV4dENvbG9yIjoiYmxhY2siLCJhY3RpdmF0aW9uQm9yZGVyQ29sb3IiOiIjNjY2IiwiYWN0aXZhdGlvbkJrZ0NvbG9yIjoiI2Y0ZjRmNCIsInNlcXVlbmNlTnVtYmVyQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvciI6InJnYmEoMTAyLCAxMDIsIDI1NSwgMC40OSkiLCJhbHRTZWN0aW9uQmtnQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvcjIiOiIjZmZmNDAwIiwidGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsInRhc2tCa2dDb2xvciI6IiM4YTkwZGQiLCJ0YXNrVGV4dExpZ2h0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0RGFya0NvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dE91dHNpZGVDb2xvciI6ImJsYWNrIiwidGFza1RleHRDbGlja2FibGVDb2xvciI6IiMwMDMxNjMiLCJhY3RpdmVUYXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwiYWN0aXZlVGFza0JrZ0NvbG9yIjoiI2JmYzdmZiIsImdyaWRDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQmtnQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JvcmRlckNvbG9yIjoiZ3JleSIsImNyaXRCb3JkZXJDb2xvciI6IiNmZjg4ODgiLCJjcml0QmtnQ29sb3IiOiJyZWQiLCJ0b2RheUxpbmVDb2xvciI6InJlZCIsImxhYmVsQ29sb3IiOiJibGFjayIsImVycm9yQmtnQ29sb3IiOiIjNTUyMjIyIiwiZXJyb3JUZXh0Q29sb3IiOiIjNTUyMjIyIiwiY2xhc3NUZXh0IjoiIzEzMTMwMCIsImZpbGxUeXBlMCI6IiNFQ0VDRkYiLCJmaWxsVHlwZTEiOiIjZmZmZmRlIiwiZmlsbFR5cGUyIjoiaHNsKDMwNCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGUzIjoiaHNsKDEyNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU0IjoiaHNsKDE3NiwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU1IjoiaHNsKC00LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTYiOiJoc2woOCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU3IjoiaHNsKDE4OCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIn19LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ" alt=""></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">unit</span> Room<span class="token punctuation">;</span>

<span class="token keyword">interface</span>
    <span class="token keyword">type</span> TRoom <span class="token operator">=</span> <span class="token keyword">object</span>
        <span class="token keyword">private</span>                     <span class="token comment">// !!!</span>
            length<span class="token punctuation">,</span> width<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">public</span> 
            <span class="token keyword">function</span> square<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
            <span class="token keyword">procedure</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">implementation</span>
    <span class="token keyword">function</span> TRoom<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
    <span class="token keyword">begin</span>
        <span class="token keyword">result</span> <span class="token operator">:=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span> 
    <span class="token keyword">end</span><span class="token punctuation">;</span>
    
    <span class="token keyword">procedure</span> TRoom<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
    <span class="token keyword">begin</span> 
        length <span class="token operator">:=</span> l<span class="token punctuation">;</span>
        width <span class="token operator">:=</span> w<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>
    
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span>  Ex_7_02<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>

<span class="token keyword">uses</span>  SysUtils<span class="token punctuation">,</span> Room  <span class="token operator">in</span> <span class="token string">'Room.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> a<span class="token punctuation">:</span> TRoom<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    a<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Room: length = '</span><span class="token punctuation">,</span> a<span class="token punctuation">.</span>length<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">,</span> 
            <span class="token string">'; width = '</span><span class="token punctuation">,</span> a<span class="token punctuation">.</span>width<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square = '</span><span class="token punctuation">,</span> a<span class="token punctuation">.</span>square<span class="token punctuation">:</span><span class="token number">8</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h3 id="наследование">Наследование</h3>
<p><strong>Наследование</strong> - конструирование новых более сложных производных классов из уже имеющихся базовых посредством добавления полей и методов.</p>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgY2xhc3MgVFJvb217XG4gICAgICAgICNsZW5ndGgsIHdpZHRoOiBTaW5nbGVcbiAgICAgICAgK3NxdWFyZSgpOiBTaW5nbGVcbiAgICAgICAgK2luaXQobCwgdylcbiAgICB9XG5cbiAgICBjbGFzcyBUVlJvb217XG4gICAgICAgICNoZWlnaHQ6IFNpbmdsZVxuICAgICAgICArVigpOiBTaW5nbGVcbiAgICAgICAgK25ld0luaXQobCwgdywgaClcbiAgICB9XG5cbiAgICBUUm9vbSA8LS0gVFZSb29tIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQiLCJ0aGVtZVZhcmlhYmxlcyI6eyJiYWNrZ3JvdW5kIjoid2hpdGUiLCJwcmltYXJ5Q29sb3IiOiIjRUNFQ0ZGIiwic2Vjb25kYXJ5Q29sb3IiOiIjZmZmZmRlIiwidGVydGlhcnlDb2xvciI6ImhzbCg4MCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeUJvcmRlckNvbG9yIjoiaHNsKDI0MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJzZWNvbmRhcnlCb3JkZXJDb2xvciI6ImhzbCg2MCwgNjAlLCA4My41Mjk0MTE3NjQ3JSkiLCJ0ZXJ0aWFyeUJvcmRlckNvbG9yIjoiaHNsKDgwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInByaW1hcnlUZXh0Q29sb3IiOiIjMTMxMzAwIiwic2Vjb25kYXJ5VGV4dENvbG9yIjoiIzAwMDAyMSIsInRlcnRpYXJ5VGV4dENvbG9yIjoicmdiKDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEpIiwibGluZUNvbG9yIjoiIzMzMzMzMyIsInRleHRDb2xvciI6IiMzMzMiLCJtYWluQmtnIjoiI0VDRUNGRiIsInNlY29uZEJrZyI6IiNmZmZmZGUiLCJib3JkZXIxIjoiIzkzNzBEQiIsImJvcmRlcjIiOiIjYWFhYTMzIiwiYXJyb3doZWFkQ29sb3IiOiIjMzMzMzMzIiwiZm9udEZhbWlseSI6IlwidHJlYnVjaGV0IG1zXCIsIHZlcmRhbmEsIGFyaWFsIiwiZm9udFNpemUiOiIzMnB4IiwibGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsIm5vZGVCa2ciOiIjRUNFQ0ZGIiwibm9kZUJvcmRlciI6IiM5MzcwREIiLCJjbHVzdGVyQmtnIjoiI2ZmZmZkZSIsImNsdXN0ZXJCb3JkZXIiOiIjYWFhYTMzIiwiZGVmYXVsdExpbmtDb2xvciI6IiMzMzMzMzMiLCJ0aXRsZUNvbG9yIjoiIzMzMyIsImVkZ2VMYWJlbEJhY2tncm91bmQiOiIjZThlOGU4IiwiYWN0b3JCb3JkZXIiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJhY3RvckJrZyI6IiNFQ0VDRkYiLCJhY3RvclRleHRDb2xvciI6ImJsYWNrIiwiYWN0b3JMaW5lQ29sb3IiOiJncmV5Iiwic2lnbmFsQ29sb3IiOiIjMzMzIiwic2lnbmFsVGV4dENvbG9yIjoiIzMzMyIsImxhYmVsQm94QmtnQ29sb3IiOiIjRUNFQ0ZGIiwibGFiZWxCb3hCb3JkZXJDb2xvciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImxhYmVsVGV4dENvbG9yIjoiYmxhY2siLCJsb29wVGV4dENvbG9yIjoiYmxhY2siLCJub3RlQm9yZGVyQ29sb3IiOiIjYWFhYTMzIiwibm90ZUJrZ0NvbG9yIjoiI2ZmZjVhZCIsIm5vdGVUZXh0Q29sb3IiOiJibGFjayIsImFjdGl2YXRpb25Cb3JkZXJDb2xvciI6IiM2NjYiLCJhY3RpdmF0aW9uQmtnQ29sb3IiOiIjZjRmNGY0Iiwic2VxdWVuY2VOdW1iZXJDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yIjoicmdiYSgxMDIsIDEwMiwgMjU1LCAwLjQ5KSIsImFsdFNlY3Rpb25Ca2dDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yMiI6IiNmZmY0MDAiLCJ0YXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwidGFza0JrZ0NvbG9yIjoiIzhhOTBkZCIsInRhc2tUZXh0TGlnaHRDb2xvciI6IndoaXRlIiwidGFza1RleHRDb2xvciI6IndoaXRlIiwidGFza1RleHREYXJrQ29sb3IiOiJibGFjayIsInRhc2tUZXh0T3V0c2lkZUNvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dENsaWNrYWJsZUNvbG9yIjoiIzAwMzE2MyIsImFjdGl2ZVRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJhY3RpdmVUYXNrQmtnQ29sb3IiOiIjYmZjN2ZmIiwiZ3JpZENvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCa2dDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQm9yZGVyQ29sb3IiOiJncmV5IiwiY3JpdEJvcmRlckNvbG9yIjoiI2ZmODg4OCIsImNyaXRCa2dDb2xvciI6InJlZCIsInRvZGF5TGluZUNvbG9yIjoicmVkIiwibGFiZWxDb2xvciI6ImJsYWNrIiwiZXJyb3JCa2dDb2xvciI6IiM1NTIyMjIiLCJlcnJvclRleHRDb2xvciI6IiM1NTIyMjIiLCJjbGFzc1RleHQiOiIjMTMxMzAwIiwiZmlsbFR5cGUwIjoiI0VDRUNGRiIsImZpbGxUeXBlMSI6IiNmZmZmZGUiLCJmaWxsVHlwZTIiOiJoc2woMzA0LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTMiOiJoc2woMTI0LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTQiOiJoc2woMTc2LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTUiOiJoc2woLTQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNiI6ImhzbCg4LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTciOiJoc2woMTg4LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkifX0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9" alt=""></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_07_03<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>

<span class="token keyword">uses</span>  SysUtils<span class="token punctuation">,</span> Room  <span class="token operator">in</span> <span class="token string">'Ex_08_02\Room.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">type</span>  
    TVRoom <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoom<span class="token punctuation">)</span>
        height<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> V<span class="token punctuation">:</span> single<span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> newInit<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">,</span> h<span class="token punctuation">:</span> single<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TVRoom<span class="token punctuation">.</span>newInit<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>
    height <span class="token operator">:=</span> h<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TVRoom<span class="token punctuation">.</span>V<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> square <span class="token operator">*</span> height<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TVRoom<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    a<span class="token punctuation">.</span>newInit<span class="token punctuation">(</span><span class="token number">3.4</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.8</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square = '</span><span class="token punctuation">,</span> a<span class="token punctuation">.</span>square<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'V = '</span><span class="token punctuation">,</span> a<span class="token punctuation">.</span>V<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h4 id="присваивание-объектов-иерархии">Присваивание объектов иерархии</h4>
<p>Допустимо присваивать переменной типа базового класса значение переменной типа объекта производного класса.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TRoom<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> TVRoom<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
a <span class="token operator">:=</span> b<span class="token punctuation">;</span> <span class="token comment">{допустимо}</span>
b <span class="token operator">:=</span> a<span class="token punctuation">;</span> <span class="token comment">{не допустимо!}</span>
</code></pre>
<h4 id="присваивание-указателей-в-иерархии">Присваивание указателей в иерархии</h4>
<p><strong>Допустимо указателю на объект базового класса присваивать адреса объекта производного класса.</strong><br>
Однако при этом возникает проблема «невидимых» полей.</p>
<p><img src="https://i.imgur.com/O26KMSe.png" alt="Проблема «невидимых» полей"></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    pC<span class="token punctuation">:</span> <span class="token string">^T</span>Room<span class="token punctuation">;</span>
    e<span class="token punctuation">:</span> TVRoom<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
pC <span class="token operator">:=</span> <span class="token operator">@</span>e<span class="token punctuation">;</span>
pC<span class="token operator">^</span><span class="token punctuation">.</span>length <span class="token operator">:=</span> <span class="token number">3.1</span><span class="token punctuation">;</span>
pC<span class="token operator">^</span><span class="token punctuation">.</span>height <span class="token operator">:=</span> <span class="token number">2.7</span><span class="token punctuation">;</span>  <span class="token comment">{ошибка!}</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">type</span>
    pTVRoom <span class="token operator">=</span> <span class="token string">^T</span>VRoom<span class="token punctuation">;</span>

<span class="token keyword">var</span>
    pC<span class="token punctuation">:</span> <span class="token string">^T</span>Room<span class="token punctuation">;</span>
    e<span class="token punctuation">:</span> TVRoom<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
pC <span class="token operator">:=</span> <span class="token operator">@</span>e<span class="token punctuation">;</span>
pTVRoom<span class="token punctuation">(</span>pC<span class="token punctuation">)</span><span class="token operator">^</span><span class="token punctuation">.</span>height <span class="token operator">:=</span> <span class="token number">2.7</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="композиция">Композиция</h3>
<p><strong>Композиция</strong>  – включение объектов одного класса в объекты другого. Реализуется механизмом поддержки объектных полей.</p>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgY2xhc3MgVFJvb217XG4gICAgICAgICBsZW5ndGhcbiAgICAgICAgIHdpZHRoXG4gICAgICAgICArc3F1YXJlKClcbiAgICAgICAgICtpbml0KClcbiAgICB9XG5cbiAgICBjbGFzcyBURmxhdHtcbiAgICAgICAgIG5cbiAgICAgICAgIHJvb21zOiBUUm9vbVtuXVxuICAgICAgICAgK2ZsYXRTcXVhcmUoKVxuICAgICAgICAgK2luaXQoKVxuICAgIH1cblxuICAgIFRSb29tIFwiMTVcIiAtLSogVEZsYXQiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCIsInRoZW1lVmFyaWFibGVzIjp7ImJhY2tncm91bmQiOiJ3aGl0ZSIsInByaW1hcnlDb2xvciI6IiNFQ0VDRkYiLCJzZWNvbmRhcnlDb2xvciI6IiNmZmZmZGUiLCJ0ZXJ0aWFyeUNvbG9yIjoiaHNsKDgwLCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5Qm9yZGVyQ29sb3IiOiJoc2woMjQwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInNlY29uZGFyeUJvcmRlckNvbG9yIjoiaHNsKDYwLCA2MCUsIDgzLjUyOTQxMTc2NDclKSIsInRlcnRpYXJ5Qm9yZGVyQ29sb3IiOiJoc2woODAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeVRleHRDb2xvciI6IiMxMzEzMDAiLCJzZWNvbmRhcnlUZXh0Q29sb3IiOiIjMDAwMDIxIiwidGVydGlhcnlUZXh0Q29sb3IiOiJyZ2IoOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSkiLCJsaW5lQ29sb3IiOiIjMzMzMzMzIiwidGV4dENvbG9yIjoiIzMzMyIsIm1haW5Ca2ciOiIjRUNFQ0ZGIiwic2Vjb25kQmtnIjoiI2ZmZmZkZSIsImJvcmRlcjEiOiIjOTM3MERCIiwiYm9yZGVyMiI6IiNhYWFhMzMiLCJhcnJvd2hlYWRDb2xvciI6IiMzMzMzMzMiLCJmb250RmFtaWx5IjoiXCJ0cmVidWNoZXQgbXNcIiwgdmVyZGFuYSwgYXJpYWwiLCJmb250U2l6ZSI6IjE2cHgiLCJsYWJlbEJhY2tncm91bmQiOiIjZThlOGU4Iiwibm9kZUJrZyI6IiNFQ0VDRkYiLCJub2RlQm9yZGVyIjoiIzkzNzBEQiIsImNsdXN0ZXJCa2ciOiIjZmZmZmRlIiwiY2x1c3RlckJvcmRlciI6IiNhYWFhMzMiLCJkZWZhdWx0TGlua0NvbG9yIjoiIzMzMzMzMyIsInRpdGxlQ29sb3IiOiIjMzMzIiwiZWRnZUxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJhY3RvckJvcmRlciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImFjdG9yQmtnIjoiI0VDRUNGRiIsImFjdG9yVGV4dENvbG9yIjoiYmxhY2siLCJhY3RvckxpbmVDb2xvciI6ImdyZXkiLCJzaWduYWxDb2xvciI6IiMzMzMiLCJzaWduYWxUZXh0Q29sb3IiOiIjMzMzIiwibGFiZWxCb3hCa2dDb2xvciI6IiNFQ0VDRkYiLCJsYWJlbEJveEJvcmRlckNvbG9yIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwibGFiZWxUZXh0Q29sb3IiOiJibGFjayIsImxvb3BUZXh0Q29sb3IiOiJibGFjayIsIm5vdGVCb3JkZXJDb2xvciI6IiNhYWFhMzMiLCJub3RlQmtnQ29sb3IiOiIjZmZmNWFkIiwibm90ZVRleHRDb2xvciI6ImJsYWNrIiwiYWN0aXZhdGlvbkJvcmRlckNvbG9yIjoiIzY2NiIsImFjdGl2YXRpb25Ca2dDb2xvciI6IiNmNGY0ZjQiLCJzZXF1ZW5jZU51bWJlckNvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IiOiJyZ2JhKDEwMiwgMTAyLCAyNTUsIDAuNDkpIiwiYWx0U2VjdGlvbkJrZ0NvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IyIjoiI2ZmZjQwMCIsInRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJ0YXNrQmtnQ29sb3IiOiIjOGE5MGRkIiwidGFza1RleHRMaWdodENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dERhcmtDb2xvciI6ImJsYWNrIiwidGFza1RleHRPdXRzaWRlQ29sb3IiOiJibGFjayIsInRhc2tUZXh0Q2xpY2thYmxlQ29sb3IiOiIjMDAzMTYzIiwiYWN0aXZlVGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsImFjdGl2ZVRhc2tCa2dDb2xvciI6IiNiZmM3ZmYiLCJncmlkQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JrZ0NvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCb3JkZXJDb2xvciI6ImdyZXkiLCJjcml0Qm9yZGVyQ29sb3IiOiIjZmY4ODg4IiwiY3JpdEJrZ0NvbG9yIjoicmVkIiwidG9kYXlMaW5lQ29sb3IiOiJyZWQiLCJsYWJlbENvbG9yIjoiYmxhY2siLCJlcnJvckJrZ0NvbG9yIjoiIzU1MjIyMiIsImVycm9yVGV4dENvbG9yIjoiIzU1MjIyMiIsImNsYXNzVGV4dCI6IiMxMzEzMDAiLCJmaWxsVHlwZTAiOiIjRUNFQ0ZGIiwiZmlsbFR5cGUxIjoiI2ZmZmZkZSIsImZpbGxUeXBlMiI6ImhzbCgzMDQsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlMyI6ImhzbCgxMjQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNCI6ImhzbCgxNzYsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNSI6ImhzbCgtNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU2IjoiaHNsKDgsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNyI6ImhzbCgxODgsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSJ9fSwidXBkYXRlRWRpdG9yIjpmYWxzZX0" alt=""></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_04<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span>
    Room <span class="token operator">in</span> <span class="token string">'Ex_08_02\Room.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">type</span>
    TFlat <span class="token operator">=</span> <span class="token keyword">object</span>
        n<span class="token punctuation">:</span> byte<span class="token punctuation">;</span>
        rooms<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">15</span><span class="token punctuation">]</span> <span class="token keyword">of</span> TRoom<span class="token punctuation">;</span>
        <span class="token keyword">function</span> flatSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> init<span class="token punctuation">(</span>an<span class="token punctuation">:</span> Byte<span class="token punctuation">;</span> <span class="token keyword">const</span> ar<span class="token punctuation">:</span> <span class="token keyword">array</span> <span class="token keyword">of</span> TRoom<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TFlat<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">var</span>
    i<span class="token punctuation">:</span> Byte<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    n <span class="token operator">:=</span> an<span class="token punctuation">;</span>
    <span class="token keyword">for</span> i <span class="token operator">:=</span> <span class="token number">1</span> <span class="token keyword">to</span> n <span class="token keyword">do</span>
        rooms<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">.</span>init<span class="token punctuation">(</span>ar<span class="token punctuation">[</span>i <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">.</span>length<span class="token punctuation">,</span> ar<span class="token punctuation">[</span>i <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">.</span>width<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TFlat<span class="token punctuation">.</span>flatSquare<span class="token punctuation">;</span>
<span class="token keyword">var</span>
    s<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
    i<span class="token punctuation">:</span> Integer<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    s <span class="token operator">:=</span> <span class="token number">0</span><span class="token punctuation">;</span>
    <span class="token keyword">for</span> i <span class="token operator">:=</span> <span class="token number">1</span> <span class="token keyword">to</span> n <span class="token keyword">do</span>
        s <span class="token operator">:=</span> s <span class="token operator">+</span> rooms<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> s<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    mas<span class="token punctuation">:</span> <span class="token keyword">array</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">]</span> <span class="token keyword">of</span> TRoom <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">(</span>length<span class="token punctuation">:</span> <span class="token number">2.5</span><span class="token punctuation">;</span> width<span class="token punctuation">:</span> <span class="token number">3.75</span><span class="token punctuation">)</span><span class="token punctuation">,</span> 
                                 <span class="token punctuation">(</span>length<span class="token punctuation">:</span> <span class="token number">2.85</span><span class="token punctuation">;</span> width<span class="token punctuation">:</span> <span class="token number">4.1</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
                                 <span class="token punctuation">(</span>length<span class="token punctuation">:</span> <span class="token number">2.3</span><span class="token punctuation">;</span> width<span class="token punctuation">:</span> <span class="token number">2.8</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    f<span class="token punctuation">:</span> TFlat<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    f<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">,</span> mas<span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'S flast = '</span><span class="token punctuation">,</span> f<span class="token punctuation">.</span>flatSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h3 id="наполнение-агрегация">Наполнение (агрегация)</h3>
<p><strong>Наполнение</strong> – способ конструирования классов, при котором объекты строящегося класса могут включать неопределенное количество: от 0 до сравнительно больших значений (на практике обычно до нескольких десятков), объектов других классов.</p>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgIGNsYXNzIFRSb29te1xuICAgICAgICAgIGxlbmd0aFxuICAgICAgICAgIHdpZHRoXG4gICAgICAgICAgK3NxdWFyZSgpXG4gICAgICAgICAgK2luaXQoKVxuICAgICB9XG5cbiAgICAgY2xhc3MgVEJSb29te1xuICAgICAgICAgIC1wQjogXlRSb29tXG4gICAgICAgICAgK0JTcXVhcmUoKVxuICAgICAgICAgICtpbml0QWxsKClcbiAgICAgfVxuXG4gICAgIFRCUm9vbSAtLT4gVFJvb21cbiAgICAgVFJvb20gXCIwLi4xXCIgLS1vIFRCUm9vbSIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0IiwidGhlbWVWYXJpYWJsZXMiOnsiYmFja2dyb3VuZCI6IndoaXRlIiwicHJpbWFyeUNvbG9yIjoiI0VDRUNGRiIsInNlY29uZGFyeUNvbG9yIjoiI2ZmZmZkZSIsInRlcnRpYXJ5Q29sb3IiOiJoc2woODAsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsInByaW1hcnlCb3JkZXJDb2xvciI6ImhzbCgyNDAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwic2Vjb25kYXJ5Qm9yZGVyQ29sb3IiOiJoc2woNjAsIDYwJSwgODMuNTI5NDExNzY0NyUpIiwidGVydGlhcnlCb3JkZXJDb2xvciI6ImhzbCg4MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5VGV4dENvbG9yIjoiIzEzMTMwMCIsInNlY29uZGFyeVRleHRDb2xvciI6IiMwMDAwMjEiLCJ0ZXJ0aWFyeVRleHRDb2xvciI6InJnYig5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxKSIsImxpbmVDb2xvciI6IiMzMzMzMzMiLCJ0ZXh0Q29sb3IiOiIjMzMzIiwibWFpbkJrZyI6IiNFQ0VDRkYiLCJzZWNvbmRCa2ciOiIjZmZmZmRlIiwiYm9yZGVyMSI6IiM5MzcwREIiLCJib3JkZXIyIjoiI2FhYWEzMyIsImFycm93aGVhZENvbG9yIjoiIzMzMzMzMyIsImZvbnRGYW1pbHkiOiJcInRyZWJ1Y2hldCBtc1wiLCB2ZXJkYW5hLCBhcmlhbCIsImZvbnRTaXplIjoiMTZweCIsImxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJub2RlQmtnIjoiI0VDRUNGRiIsIm5vZGVCb3JkZXIiOiIjOTM3MERCIiwiY2x1c3RlckJrZyI6IiNmZmZmZGUiLCJjbHVzdGVyQm9yZGVyIjoiI2FhYWEzMyIsImRlZmF1bHRMaW5rQ29sb3IiOiIjMzMzMzMzIiwidGl0bGVDb2xvciI6IiMzMzMiLCJlZGdlTGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsImFjdG9yQm9yZGVyIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwiYWN0b3JCa2ciOiIjRUNFQ0ZGIiwiYWN0b3JUZXh0Q29sb3IiOiJibGFjayIsImFjdG9yTGluZUNvbG9yIjoiZ3JleSIsInNpZ25hbENvbG9yIjoiIzMzMyIsInNpZ25hbFRleHRDb2xvciI6IiMzMzMiLCJsYWJlbEJveEJrZ0NvbG9yIjoiI0VDRUNGRiIsImxhYmVsQm94Qm9yZGVyQ29sb3IiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJsYWJlbFRleHRDb2xvciI6ImJsYWNrIiwibG9vcFRleHRDb2xvciI6ImJsYWNrIiwibm90ZUJvcmRlckNvbG9yIjoiI2FhYWEzMyIsIm5vdGVCa2dDb2xvciI6IiNmZmY1YWQiLCJub3RlVGV4dENvbG9yIjoiYmxhY2siLCJhY3RpdmF0aW9uQm9yZGVyQ29sb3IiOiIjNjY2IiwiYWN0aXZhdGlvbkJrZ0NvbG9yIjoiI2Y0ZjRmNCIsInNlcXVlbmNlTnVtYmVyQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvciI6InJnYmEoMTAyLCAxMDIsIDI1NSwgMC40OSkiLCJhbHRTZWN0aW9uQmtnQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvcjIiOiIjZmZmNDAwIiwidGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsInRhc2tCa2dDb2xvciI6IiM4YTkwZGQiLCJ0YXNrVGV4dExpZ2h0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0RGFya0NvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dE91dHNpZGVDb2xvciI6ImJsYWNrIiwidGFza1RleHRDbGlja2FibGVDb2xvciI6IiMwMDMxNjMiLCJhY3RpdmVUYXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwiYWN0aXZlVGFza0JrZ0NvbG9yIjoiI2JmYzdmZiIsImdyaWRDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQmtnQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JvcmRlckNvbG9yIjoiZ3JleSIsImNyaXRCb3JkZXJDb2xvciI6IiNmZjg4ODgiLCJjcml0QmtnQ29sb3IiOiJyZWQiLCJ0b2RheUxpbmVDb2xvciI6InJlZCIsImxhYmVsQ29sb3IiOiJibGFjayIsImVycm9yQmtnQ29sb3IiOiIjNTUyMjIyIiwiZXJyb3JUZXh0Q29sb3IiOiIjNTUyMjIyIiwiY2xhc3NUZXh0IjoiIzEzMTMwMCIsImZpbGxUeXBlMCI6IiNFQ0VDRkYiLCJmaWxsVHlwZTEiOiIjZmZmZmRlIiwiZmlsbFR5cGUyIjoiaHNsKDMwNCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGUzIjoiaHNsKDEyNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU0IjoiaHNsKDE3NiwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU1IjoiaHNsKC00LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTYiOiJoc2woOCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU3IjoiaHNsKDE4OCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIn19LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ" alt="agregation"></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_05<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span>
    Room <span class="token operator">in</span> <span class="token string">'Ex_08_02\Room.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">type</span>
    TBRoom <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoom<span class="token punctuation">)</span>
        pB<span class="token punctuation">:</span> <span class="token string">^T</span>Room<span class="token punctuation">;</span>
        <span class="token keyword">function</span> BSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> initAll<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> single<span class="token punctuation">;</span> lb<span class="token punctuation">:</span> single <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> wb<span class="token punctuation">:</span> single <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TBRoom<span class="token punctuation">.</span>initAll<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>lb <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token operator">or</span> <span class="token punctuation">(</span>wb <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token keyword">then</span>
        pB <span class="token operator">:=</span> <span class="token keyword">nil</span>
    <span class="token keyword">else</span>
	    <span class="token keyword">begin</span>
	        <span class="token keyword">new</span><span class="token punctuation">(</span>pB<span class="token punctuation">)</span><span class="token punctuation">;</span>
	        pB<span class="token operator">^</span><span class="token punctuation">.</span>init<span class="token punctuation">(</span>lb<span class="token punctuation">,</span> wb<span class="token punctuation">)</span><span class="token punctuation">;</span>
	    <span class="token keyword">end</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TBRoom<span class="token punctuation">.</span>BSquare<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">if</span> pB <span class="token operator">=</span> <span class="token keyword">nil</span> <span class="token keyword">then</span>
        <span class="token keyword">result</span> <span class="token operator">:=</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span>
    <span class="token keyword">else</span>
        <span class="token keyword">result</span> <span class="token operator">:=</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> pB<span class="token operator">^</span><span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    b<span class="token punctuation">:</span> TBRoom<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    b<span class="token punctuation">.</span>initAll<span class="token punctuation">(</span><span class="token number">3.4</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">1.8</span><span class="token punctuation">,</span> <span class="token number">0.8</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'BSquare ='</span><span class="token punctuation">,</span> b<span class="token punctuation">.</span>BSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">8</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h2 id="простой-полиморфизм">Простой полиморфизм</h2>
<p><strong>Простой полиморфизм</strong> – механизм переопределения методов при наследовании, при котором связь метода с объектом выполняется на этапе компиляции (<em>раннее связывание</em>).</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_06<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span>
    Room <span class="token operator">in</span> <span class="token string">'Ex_08_02\Room.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">type</span>
    TVRoom2 <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoom<span class="token punctuation">)</span>
        height<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">,</span> h<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TVRoom2<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">inherited</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>     <span class="token comment">{ TRoom.init(l,w);}</span>
    Height <span class="token operator">:=</span> h<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TVRoom2<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> <span class="token number">2</span> <span class="token operator">*</span> <span class="token punctuation">(</span><span class="token keyword">inherited</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> height <span class="token operator">*</span> <span class="token punctuation">(</span>length <span class="token operator">+</span> width<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TVRoom2<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    a<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.4</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.8</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square = '</span><span class="token punctuation">,</span> a<span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h3 id="обращение-объекта-производного-класса-к-переопределенному-методу-базового-класса-в-программе">Обращение объекта производного класса к переопределенному методу базового класса в программе</h3>
<p>При необходимости обращении к переопределенному методу базового класса явно меняют тип переменной – объекта класса, например так</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TVRoom2<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> TRoom<span class="token punctuation">;</span>

<span class="token comment">{...}</span>
b <span class="token operator">:=</span> a<span class="token punctuation">;</span>
b<span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="сложный-полиморфизм.-конструкторы">Сложный полиморфизм. Конструкторы</h2>
<p>Существует три ситуации, в которых определение <em><strong>типа</strong></em> объекта на этапе компиляции программы невозможно, и, следовательно, невозможно правильное подключение переопределенного метода.</p>
<h3 id="случая-обязательного-использования-сложного-полиморфизма">3 случая обязательного использования сложного полиморфизма</h3>
<p><strong>1-й случай</strong> – если наследуемый метод для объекта производного класса вызывает метод, переопределенный в производном классе.</p>
<p><strong>2-й случай</strong> – если объект производного класса через указатель базового класса обращается к методу, переопределенному производным классом.</p>
<p><strong>3-й случай</strong> – если процедура вызывает переопределенный метод для объекта производного класса, переданного в процедуру через параметр-переменную, описанный как объект базового класса («процедура с полиморфным объектом»).</p>
<h4 id="й-случай">1-й случай</h4>
<p><img src="https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgIGNsYXNzIFRSb29tUHtcbiAgICAgICAgICBsZW5ndGhcbiAgICAgICAgICB3aWR0aFxuICAgICAgICAgICtzcXVhcmUoKVxuICAgICAgICAgICtpbml0KClcbiAgICAgICAgICAraW5pdFAoKVxuICAgICB9XG5cbiAgICAgY2xhc3MgVFZSb29tUHtcbiAgICAgICAgICBoZWlnaHRcbiAgICAgICAgICArc3F1YXJlKClcbiAgICAgICAgICAraW5pdCgpXG4gICAgIH1cblxuICAgICBUUm9vbVAgPC0tIFRWUm9vbVAiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCIsInRoZW1lVmFyaWFibGVzIjp7ImJhY2tncm91bmQiOiJ3aGl0ZSIsInByaW1hcnlDb2xvciI6IiNFQ0VDRkYiLCJzZWNvbmRhcnlDb2xvciI6IiNmZmZmZGUiLCJ0ZXJ0aWFyeUNvbG9yIjoiaHNsKDgwLCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5Qm9yZGVyQ29sb3IiOiJoc2woMjQwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInNlY29uZGFyeUJvcmRlckNvbG9yIjoiaHNsKDYwLCA2MCUsIDgzLjUyOTQxMTc2NDclKSIsInRlcnRpYXJ5Qm9yZGVyQ29sb3IiOiJoc2woODAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeVRleHRDb2xvciI6IiMxMzEzMDAiLCJzZWNvbmRhcnlUZXh0Q29sb3IiOiIjMDAwMDIxIiwidGVydGlhcnlUZXh0Q29sb3IiOiJyZ2IoOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSkiLCJsaW5lQ29sb3IiOiIjMzMzMzMzIiwidGV4dENvbG9yIjoiIzMzMyIsIm1haW5Ca2ciOiIjRUNFQ0ZGIiwic2Vjb25kQmtnIjoiI2ZmZmZkZSIsImJvcmRlcjEiOiIjOTM3MERCIiwiYm9yZGVyMiI6IiNhYWFhMzMiLCJhcnJvd2hlYWRDb2xvciI6IiMzMzMzMzMiLCJmb250RmFtaWx5IjoiXCJ0cmVidWNoZXQgbXNcIiwgdmVyZGFuYSwgYXJpYWwiLCJmb250U2l6ZSI6IjE2cHgiLCJsYWJlbEJhY2tncm91bmQiOiIjZThlOGU4Iiwibm9kZUJrZyI6IiNFQ0VDRkYiLCJub2RlQm9yZGVyIjoiIzkzNzBEQiIsImNsdXN0ZXJCa2ciOiIjZmZmZmRlIiwiY2x1c3RlckJvcmRlciI6IiNhYWFhMzMiLCJkZWZhdWx0TGlua0NvbG9yIjoiIzMzMzMzMyIsInRpdGxlQ29sb3IiOiIjMzMzIiwiZWRnZUxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJhY3RvckJvcmRlciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImFjdG9yQmtnIjoiI0VDRUNGRiIsImFjdG9yVGV4dENvbG9yIjoiYmxhY2siLCJhY3RvckxpbmVDb2xvciI6ImdyZXkiLCJzaWduYWxDb2xvciI6IiMzMzMiLCJzaWduYWxUZXh0Q29sb3IiOiIjMzMzIiwibGFiZWxCb3hCa2dDb2xvciI6IiNFQ0VDRkYiLCJsYWJlbEJveEJvcmRlckNvbG9yIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwibGFiZWxUZXh0Q29sb3IiOiJibGFjayIsImxvb3BUZXh0Q29sb3IiOiJibGFjayIsIm5vdGVCb3JkZXJDb2xvciI6IiNhYWFhMzMiLCJub3RlQmtnQ29sb3IiOiIjZmZmNWFkIiwibm90ZVRleHRDb2xvciI6ImJsYWNrIiwiYWN0aXZhdGlvbkJvcmRlckNvbG9yIjoiIzY2NiIsImFjdGl2YXRpb25Ca2dDb2xvciI6IiNmNGY0ZjQiLCJzZXF1ZW5jZU51bWJlckNvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IiOiJyZ2JhKDEwMiwgMTAyLCAyNTUsIDAuNDkpIiwiYWx0U2VjdGlvbkJrZ0NvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IyIjoiI2ZmZjQwMCIsInRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJ0YXNrQmtnQ29sb3IiOiIjOGE5MGRkIiwidGFza1RleHRMaWdodENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dERhcmtDb2xvciI6ImJsYWNrIiwidGFza1RleHRPdXRzaWRlQ29sb3IiOiJibGFjayIsInRhc2tUZXh0Q2xpY2thYmxlQ29sb3IiOiIjMDAzMTYzIiwiYWN0aXZlVGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsImFjdGl2ZVRhc2tCa2dDb2xvciI6IiNiZmM3ZmYiLCJncmlkQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JrZ0NvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCb3JkZXJDb2xvciI6ImdyZXkiLCJjcml0Qm9yZGVyQ29sb3IiOiIjZmY4ODg4IiwiY3JpdEJrZ0NvbG9yIjoicmVkIiwidG9kYXlMaW5lQ29sb3IiOiJyZWQiLCJsYWJlbENvbG9yIjoiYmxhY2siLCJlcnJvckJrZ0NvbG9yIjoiIzU1MjIyMiIsImVycm9yVGV4dENvbG9yIjoiIzU1MjIyMiIsImNsYXNzVGV4dCI6IiMxMzEzMDAiLCJmaWxsVHlwZTAiOiIjRUNFQ0ZGIiwiZmlsbFR5cGUxIjoiI2ZmZmZkZSIsImZpbGxUeXBlMiI6ImhzbCgzMDQsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlMyI6ImhzbCgxMjQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNCI6ImhzbCgxNzYsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNSI6ImhzbCgtNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU2IjoiaHNsKDgsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNyI6ImhzbCgxODgsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSJ9fSwidXBkYXRlRWRpdG9yIjpmYWxzZX0" alt=""></p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_07<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">;</span>

<span class="token comment">// ================ TRoomP ================</span>
<span class="token keyword">type</span>
    TRoomP <span class="token operator">=</span> <span class="token keyword">object</span>
        length<span class="token punctuation">,</span> width<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> print<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TRoomP<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TRoomP<span class="token punctuation">.</span>print<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    writeln<span class="token punctuation">(</span><span class="token string">'Square = '</span><span class="token punctuation">,</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TRoomP<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    length <span class="token operator">:=</span> l<span class="token punctuation">;</span>
    width <span class="token operator">:=</span> w<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token comment">// ================ TVRoomP ================</span>
<span class="token keyword">type</span>
    TVRoomP <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoomP<span class="token punctuation">)</span>
        height<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">procedure</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">,</span> h<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> TVRoomP<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">inherited</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>
    height <span class="token operator">:=</span> h<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TVRoomP<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    square <span class="token operator">:=</span> <span class="token number">2</span> <span class="token operator">*</span> <span class="token punctuation">(</span><span class="token keyword">inherited</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> height <span class="token operator">*</span> <span class="token punctuation">(</span>length <span class="token operator">+</span> width<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token comment">// ================  ================</span>
<span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TRoomP<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> TVRoomP<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    a<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    a<span class="token punctuation">.</span>print<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>               <span class="token comment">// `Square =  17.85` -- верно</span>
    
    b<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.7</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    b<span class="token punctuation">.</span>print<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>               <span class="token comment">// `Square =  17.85` -- неверно, должно быть: `82.14`</span>
    writeLn<span class="token punctuation">(</span>b<span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// `82.14`           -- верно</span>
    readln<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h5 id="пояснение-к-ошибке">Пояснение к ошибке</h5>
<p><img src="https://i.imgur.com/BX04rP7.png" alt="explanation"><br>
При <strong>позднем связывании</strong> нужный аспект полиморфного метода определяется на этапе выполнения программы по типу объекта, для которого вызывается метод.</p>
<h5 id="реализация-сложного-полиморфизма">Реализация сложного полиморфизма</h5>
<p>Для организации сложного полиморфизма необходимо:</p>
<ol>
<li>переопределяемые методы описать служебным словом <strong><code>virtual</code></strong>;</li>
<li>к методам класса с виртуальными полиморфными методами добавить специальный метод-процедуру – <em><strong>конструктор</strong></em>, в котором служебное слово <code>procedure</code> заменено служебным словом <strong><code>constructor</code></strong>;</li>
<li>вызвать конструктор прежде, чем произойдет первое обращение к виртуальным полиморфным методам.</li>
</ol>
<p>Подключение осуществляется с использованием <em><strong>таблицы виртуальных методов</strong></em> (ТВМ), которая создается при выполнении конструктора.</p>
<p><img src="https://i.imgur.com/MHpwCZp.png" alt="tbm"></p>
<h5 id="различие-раннего-и-позднего-связывания">Различие раннего и позднего связывания</h5>
<p><strong>Раннее связывание</strong> – адрес метода определяется на этапе компиляции по объявленному типу переменной.</p>
<p><img src="https://i.imgur.com/qVIESir.png" alt="early"></p>
<p><strong>Позднее связывание</strong> – адрес метода определяется на этапе выполнения по фактическому типу объекта через таблицу виртуальных методов класса, адрес которой хранится в объекте.</p>
<p><img src="https://i.imgur.com/wXILqBN.png" alt="lately"></p>
<h5 id="исправленный-пример">Исправленный пример</h5>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">unit</span> RoomP<span class="token punctuation">;</span>

<span class="token keyword">interface</span>
	<span class="token keyword">type</span>
	    TRoomP <span class="token operator">=</span> <span class="token keyword">object</span>
	        length<span class="token punctuation">,</span> sidth<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
	        <span class="token keyword">function</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>    <span class="token comment">// !!!</span>
	        <span class="token keyword">procedure</span> print<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	        <span class="token keyword">constructor</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
	    <span class="token keyword">end</span><span class="token punctuation">;</span>

	<span class="token keyword">type</span>
	    TVRoomP <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoomP<span class="token punctuation">)</span>
	        height<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
	        <span class="token keyword">function</span> square<span class="token punctuation">:</span> Single<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>      <span class="token comment">// !!!</span>
	        <span class="token keyword">constructor</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">,</span> h<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
	    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">implementation</span>
	<span class="token keyword">function</span> TRoomP<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
	<span class="token keyword">begin</span>
	    <span class="token keyword">result</span> <span class="token operator">:=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>
	<span class="token keyword">end</span><span class="token punctuation">;</span>

	<span class="token keyword">procedure</span> TRoomP<span class="token punctuation">.</span>print<span class="token punctuation">;</span>
	<span class="token keyword">begin</span>
	    writeln<span class="token punctuation">(</span><span class="token string">'Square = '</span><span class="token punctuation">,</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">end</span><span class="token punctuation">;</span>

	<span class="token keyword">constructor</span> TRoomP<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
	<span class="token keyword">begin</span>
	    length <span class="token operator">:=</span> l<span class="token punctuation">;</span>
	    width <span class="token operator">:=</span> w<span class="token punctuation">;</span>
	<span class="token keyword">end</span><span class="token punctuation">;</span>

	<span class="token keyword">constructor</span> TVRoomP<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
	<span class="token keyword">begin</span>
	    <span class="token keyword">inherited</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>
	    height <span class="token operator">:=</span> h<span class="token punctuation">;</span>
	<span class="token keyword">end</span><span class="token punctuation">;</span>

	<span class="token keyword">function</span> TVRoomP<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
	<span class="token keyword">begin</span>
	    square <span class="token operator">:=</span> <span class="token number">2</span> <span class="token operator">*</span> <span class="token punctuation">(</span><span class="token keyword">inherited</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> height <span class="token operator">*</span> <span class="token punctuation">(</span>length <span class="token operator">+</span> width<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_07a<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span>
    RoomP <span class="token operator">in</span> <span class="token string">'RoomP.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TRoomP<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> TVRoomP<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    a<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    a<span class="token punctuation">.</span>print<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>                <span class="token comment">// `Square = 17.85`</span>
    b<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.7</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    b<span class="token punctuation">.</span>print<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>                <span class="token comment">// `Square =  82.14`</span>
    readln<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h4 id="й-случай-1">2-й случай</h4>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_07b<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span>
    RoomP <span class="token operator">in</span> <span class="token string">'Ex_07_07\RoomP.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    pA<span class="token punctuation">:</span> <span class="token string">^T</span>RoomP<span class="token punctuation">;</span>
    B<span class="token punctuation">:</span> TVRoomP<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    B<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.7</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square ='</span><span class="token punctuation">,</span> B<span class="token punctuation">.</span>Square<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>    <span class="token comment">// `Square = 82.14`</span>
    pA <span class="token operator">:=</span> <span class="token operator">@</span>B<span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square ='</span><span class="token punctuation">,</span> pA<span class="token operator">^</span><span class="token punctuation">.</span>Square<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// `Square = 82.14`</span>
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h4 id="й-случай-2">3-й случай</h4>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_07c<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">,</span>
    RoomP <span class="token operator">in</span> <span class="token string">'Ex_08_07\RoomP.pas'</span><span class="token punctuation">;</span>

<span class="token keyword">procedure</span> print<span class="token punctuation">(</span><span class="token keyword">var</span> r<span class="token punctuation">:</span> TRoomP<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    writeln<span class="token punctuation">(</span><span class="token string">'Square ='</span><span class="token punctuation">,</span> r<span class="token punctuation">.</span>square<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    a<span class="token punctuation">:</span> TRoomP<span class="token punctuation">;</span>
    b<span class="token punctuation">:</span> TVRoomP<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    a<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    b<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.7</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    print<span class="token punctuation">(</span>a<span class="token punctuation">)</span><span class="token punctuation">;</span>
    print<span class="token punctuation">(</span>b<span class="token punctuation">)</span><span class="token punctuation">;</span>
    readln<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h3 id="функция-определения-типа-полиморфного-объекта">Функция определения типа полиморфного объекта</h3>
<p><code>typeOf(&lt;имя_класса_или_объекта&gt;): pointer</code> – возвращает адрес ТВМ класса или класса объекта. Если адрес <em>ТВМ</em> объекта и класса совпадают, то объект является переменной данного класса.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">if</span> typeOf<span class="token punctuation">(</span><span class="token keyword">self</span><span class="token punctuation">)</span> <span class="token operator">=</span> typeOf<span class="token punctuation">(</span><span class="token operator">&lt;</span>имя_класса<span class="token operator">&gt;</span><span class="token punctuation">)</span> <span class="token keyword">then</span>
    <span class="token comment">{Объект принадлежит класс}</span><span class="token operator">&gt;</span>
<span class="token keyword">else</span>
    <span class="token comment">{Объект не принадлежит классу}</span>
</code></pre>
<h3 id="свойства-виртуальных-методов-класса">Свойства виртуальных методов класса</h3>
<ol>
<li>позднее связывание требует построения ТВМ, а следовательно <strong>больше памяти</strong>;</li>
<li>вызов виртуальных полиморфных методов происходит через ТВМ, а следовательно <strong>медленнее</strong>;</li>
<li><strong>список параметров</strong> одноименных виртуальных полиморфных методов <strong>должен совпадать</strong>, а статических полиморфных – не обязательно;</li>
<li>статический полиморфный метод не может переопределить виртуальный полиморфный метод.</li>
</ol>
<h2 id="динамические-полиморфные-объекты.-деструкторы">Динамические полиморфные объекты. Деструкторы</h2>
<h3 id="создание-полиморфных-объектов">Создание полиморфных объектов:</h3>
<p>Функция <code>new(&lt;тип_указателя&gt;)</code> – возвращает адрес размещенного и, возможно, сконструированного объекта. После необходим вызов конструктора.<br>
Или <code>new(&lt;тип_указателя&gt;, &lt;конструктор&gt;)</code>.</p>
<p><strong>Деструктор</strong> – метод класса, который используется для корректного уничтожения полиморфного объекта, содержащего невидимое поле. Деструктор можно переопределять.</p>
<h3 id="уничтожение-полиморфных-объектов">Уничтожение полиморфных объектов</h3>
<p>Процедура <code>dispose(&lt;указатель&gt;)</code> – освобождает память, на которую указывает указатель. Перед вызовом процедуры необходим вызов деструктора, если он указан, и затем – выполняется освобождение памяти.<br>
Или <code>dispose(&lt;указатель&gt;, &lt;деконструктор&gt;)</code>.</p>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_08<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">;</span>

<span class="token keyword">type</span>
    pTRoomD <span class="token operator">=</span> <span class="token string">^T</span>RoomD<span class="token punctuation">;</span>

    TRoomD <span class="token operator">=</span> <span class="token keyword">object</span>
        length<span class="token punctuation">,</span> width<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>
        <span class="token keyword">constructor</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">destructor</span> done<span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">type</span>
    pTVRoomD <span class="token operator">=</span> <span class="token string">^T</span>VRoomD<span class="token punctuation">;</span>
    TVRoomD <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoomD<span class="token punctuation">)</span>
        height<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>
        <span class="token keyword">constructor</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">,</span> h<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TRoomD<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">constructor</span> TRoomD<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    length <span class="token operator">:=</span> l<span class="token punctuation">;</span>
    width <span class="token operator">:=</span> w<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">destructor</span> TRoomD<span class="token punctuation">.</span>done<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">constructor</span> TVRoomD<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">inherited</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>
    height <span class="token operator">:=</span> h<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TVRoomD<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">result</span> <span class="token operator">:=</span> <span class="token number">2</span> <span class="token operator">*</span> <span class="token punctuation">(</span><span class="token keyword">inherited</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> height <span class="token operator">*</span> <span class="token punctuation">(</span>length <span class="token operator">+</span> width<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    pA<span class="token punctuation">:</span> pTRoomD<span class="token punctuation">;</span>
    pB<span class="token punctuation">:</span> pTVRoomD<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    <span class="token comment">{указатель базового типа, объект базового типа}</span>
    pA <span class="token operator">:=</span> <span class="token keyword">new</span><span class="token punctuation">(</span>pTRoomD<span class="token punctuation">)</span><span class="token punctuation">;</span>
    pA<span class="token operator">^</span><span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square ='</span><span class="token punctuation">,</span> pA<span class="token operator">^</span><span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// `Square = 17.85`</span>
    pA<span class="token operator">^</span><span class="token punctuation">.</span>done<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">dispose</span><span class="token punctuation">(</span>pA<span class="token punctuation">)</span><span class="token punctuation">;</span>

    <span class="token comment">{указатель производного типа, объект производного типа}</span>
    pB <span class="token operator">:=</span> <span class="token keyword">new</span><span class="token punctuation">(</span>pTVRoomD<span class="token punctuation">)</span><span class="token punctuation">;</span>
    pB<span class="token operator">^</span><span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.7</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square ='</span><span class="token punctuation">,</span> pB<span class="token operator">^</span><span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// `Square = 82.14`</span>
    <span class="token keyword">Dispose</span><span class="token punctuation">(</span>pB<span class="token punctuation">,</span> done<span class="token punctuation">)</span><span class="token punctuation">;</span>

    <span class="token comment">{указатель базового типа, объект производного типа}</span>
    pA <span class="token operator">:=</span> <span class="token keyword">new</span><span class="token punctuation">(</span>pTVRoomD<span class="token punctuation">,</span> init<span class="token punctuation">(</span><span class="token number">3.5</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.7</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span><span class="token string">'Square ='</span><span class="token punctuation">,</span> pA<span class="token operator">^</span><span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// `Square = 82.14`</span>
    <span class="token keyword">dispose</span><span class="token punctuation">(</span>pA<span class="token punctuation">,</span> done<span class="token punctuation">)</span><span class="token punctuation">;</span>

    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h3 id="динамические-поля-в-объектах">Динамические поля в объектах</h3>
<pre class=" language-pascal"><code class="prism  language-pascal"><span class="token keyword">program</span> Ex_7_09<span class="token punctuation">;</span>

<span class="token comment">{$APPTYPE CONSOLE}</span>
<span class="token keyword">uses</span>
    SysUtils<span class="token punctuation">;</span>

<span class="token keyword">type</span>
    pTRoomD <span class="token operator">=</span> <span class="token string">^T</span>RoomD<span class="token punctuation">;</span>

    TRoomD <span class="token operator">=</span> <span class="token keyword">object</span>
        length<span class="token punctuation">,</span> width<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Single<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>
        <span class="token keyword">constructor</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">destructor</span> done<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">type</span>
    pTBRoomD <span class="token operator">=</span> <span class="token string">^T</span>BRoomD<span class="token punctuation">;</span>

    TBRoomD <span class="token operator">=</span> <span class="token keyword">object</span><span class="token punctuation">(</span>TRoomD<span class="token punctuation">)</span>
        pB<span class="token punctuation">:</span> pTRoomD<span class="token punctuation">;</span>
        <span class="token keyword">function</span> square<span class="token punctuation">:</span> Single<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>
        <span class="token keyword">function</span> BSquare<span class="token punctuation">:</span> Single<span class="token punctuation">;</span>
        <span class="token keyword">constructor</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">:</span> Single<span class="token punctuation">;</span> lb<span class="token punctuation">,</span> wb<span class="token punctuation">:</span> Single<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">destructor</span> done<span class="token punctuation">;</span> <span class="token keyword">virtual</span><span class="token punctuation">;</span>
    <span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TRoomD<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    square <span class="token operator">:=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">constructor</span> TRoomD<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    length <span class="token operator">:=</span> l<span class="token punctuation">;</span>
    width <span class="token operator">:=</span> w<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">destructor</span> TRoomD<span class="token punctuation">.</span>done<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">constructor</span> TBRoomD<span class="token punctuation">.</span>init<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">inherited</span> init<span class="token punctuation">(</span>l<span class="token punctuation">,</span> w<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>lb <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token operator">or</span> <span class="token punctuation">(</span>wb <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token keyword">then</span>
        pB <span class="token operator">:=</span> <span class="token keyword">nil</span>
    <span class="token keyword">else</span>
        pB <span class="token operator">:=</span> <span class="token keyword">new</span><span class="token punctuation">(</span>pTRoomD<span class="token punctuation">,</span> init<span class="token punctuation">(</span>lb<span class="token punctuation">,</span> wb<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TBRoomD<span class="token punctuation">.</span>BSquare<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">if</span> pB <span class="token operator">&lt;&gt;</span> <span class="token keyword">nil</span> <span class="token keyword">then</span>
        BSquare <span class="token operator">:=</span> pB<span class="token operator">^</span><span class="token punctuation">.</span>square
    <span class="token keyword">else</span>
        BSquare <span class="token operator">:=</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> TBRoomD<span class="token punctuation">.</span>square<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    square <span class="token operator">:=</span> <span class="token keyword">inherited</span> square<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> BSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">destructor</span> TBRoomD<span class="token punctuation">.</span>done<span class="token punctuation">;</span>
<span class="token keyword">begin</span>
    <span class="token keyword">if</span> pB <span class="token operator">&lt;&gt;</span> <span class="token keyword">nil</span> <span class="token keyword">then</span>
        <span class="token keyword">Dispose</span><span class="token punctuation">(</span>pB<span class="token punctuation">,</span> done<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">;</span>

<span class="token keyword">var</span>
    A<span class="token punctuation">:</span> TBRoomD<span class="token punctuation">;</span>
    pB1<span class="token punctuation">:</span> pTBRoomD<span class="token punctuation">;</span>
    pB2<span class="token punctuation">:</span> pTRoomD<span class="token punctuation">;</span>

<span class="token keyword">begin</span>
    <span class="token comment">{статический объект с динамическим полем}</span>
    A<span class="token punctuation">.</span>init<span class="token punctuation">(</span><span class="token number">3.2</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.5</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>A<span class="token punctuation">.</span>Square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">,</span> A<span class="token punctuation">.</span>BSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>                <span class="token comment">// ` 18.82  2.50`</span>
    A<span class="token punctuation">.</span>done<span class="token punctuation">;</span>
    
    <span class="token comment">{динамический полиморфный объект с динамическим полем}</span>
    pB1 <span class="token operator">:=</span> <span class="token keyword">new</span><span class="token punctuation">(</span>pTBRoomD<span class="token punctuation">,</span> init<span class="token punctuation">(</span><span class="token number">3.2</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.5</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>pB1<span class="token operator">^</span><span class="token punctuation">.</span>square<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">,</span> pB1<span class="token operator">^</span><span class="token punctuation">.</span>BSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>          <span class="token comment">// ` 18.82  2.50`</span>
    <span class="token keyword">dispose</span><span class="token punctuation">(</span>pB1<span class="token punctuation">,</span> Done<span class="token punctuation">)</span><span class="token punctuation">;</span>
    
    <span class="token comment">{динамический полиморфный объект с динамическим полем}</span>
    pB2 <span class="token operator">:=</span> <span class="token keyword">new</span><span class="token punctuation">(</span>pTBRoomD<span class="token punctuation">,</span> init<span class="token punctuation">(</span><span class="token number">3.2</span><span class="token punctuation">,</span> <span class="token number">5.1</span><span class="token punctuation">,</span> <span class="token number">2.5</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    writeLn<span class="token punctuation">(</span>pB2<span class="token operator">^</span><span class="token punctuation">.</span>square<span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">,</span> pTBRoomD<span class="token punctuation">(</span>pB2<span class="token punctuation">)</span><span class="token operator">^</span><span class="token punctuation">.</span>BSquare<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// ` 18.82  2.50`</span>
    <span class="token keyword">dispose</span><span class="token punctuation">(</span>pB2<span class="token punctuation">,</span> done<span class="token punctuation">)</span><span class="token punctuation">;</span>
    
    readLn<span class="token punctuation">;</span>
<span class="token keyword">end</span><span class="token punctuation">.</span>
</code></pre>
<h1 id="технология-событийного-программирования.-события-windows-сообщения-и-события-delphi.-основные-события-delphi.-примеры.">Технология событийного программирования. События Windows, сообщения и события Delphi. Основные события Delphi. Примеры.</h1>
<p><em><strong>Приложение</strong>  (в отличие от программы)</em> – набор подпрограмм, вызываемых при наступлении некоторого события, которым считается любое изменение в системе, касающееся данного приложения.</p>
<h2 id="события-delphi-и-их-обработчики">События Delphi и их обработчики</h2>
<p>Обработчики сообщений <em>Windows</em> предусмотрены у объектов класса <code>TForm</code> и классов управляющих компонентов, таких как кнопки, редакторы и т. п.</p>
<p>Обработка выполняется следующим образом:</p>
<ol>
<li>В системе происходит событие, например, пользователь передвинул мышь или нажал на клавишу клавиатуры, в результате генерируется сообщение об этом событии – <em><strong>сообщение Windows</strong></em>.</li>
<li>Сообщение <em>Windows</em> диспетчируется конкретному приложению.</li>
<li>В приложении сообщение передается активному компоненту (окну или управляющему элементу).</li>
<li>Метод обработки сообщения <em>Windows</em> компонента  инициирует заранее предусмотренные <em><strong>события Delphi</strong></em>.</li>
<li>Если в приложении предусмотрен соответствующий обработчик события <em>Delphi</em>, то он вызывается, если нет – то продолжается обработка сообщения <em>Windows</em>.</li>
</ol>
<h3 id="события-delphi">События <em>Delphi</em></h3>
<p>Обработчики сообщений <em>Windows</em>, встроенные в классы компонентов VCL, инициируют множество событий <em>Delphi</em>.</p>
<p>Например, обработчик события клавиатуры <code>WM_CHAR</code> класса <code>TForm</code>  инициирует три события <strong>Delphi</strong>.</p>
<p><img src="https://i.imgur.com/ZmOBN8n.png" alt="enter image description here"></p>
<h3 id="обработчики-событий-delphi">Обработчики событий Delphi</h3>
<p>Для каждого обработчика событий предусмотрен заголовок и определённый список передаваемых ему параметров.<br>
<code>procedure &lt;компонент&gt;.&lt;Имя_компонента&gt;&lt;Имя_события_delphi&gt;(Sender: TObject[, {...}]);</code></p>
<ol>
<li><code>procedure TForm1.FormActivate(Sender:TObject);</code><br>
Параметр <code>Sender</code> – отправитель (инициатор события).</li>
<li><code>procedure TForm1.Edit1KeyPress(Sender: TObject; var Key: Char);</code><br>
Параметр  Key  –  символ ANSI.</li>
<li><code>procedure TForm1.Edit1KeyDown(Sender: TObject; var Key: Word; Shift: TShiftState);</code><br>
Параметры:  Key  – виртуальный код, Shift  – управляющие клав.</li>
<li><code>procedure TForm1.Edit1KeyUp(Sender: TObject; var Key: Word; Shift: TShiftState);</code></li>
</ol>
<h2 id="примеры-событий-delphi-обрабатываемые-объектами-класса-tform">Примеры событий Delphi, обрабатываемые объектами класса <em>TForm</em></h2>
<ol>
<li>
<p>при изменении состояния формы:</p>
<ul>
<li><code>OnCreate</code> – в начальной стадии создания формы - используется при необходимости задания параметров (цвет или размер);</li>
<li><code>OnActivate</code> – при получении формой фокуса ввода (окно становится активным и ему адресуется весь ввод с клавиатуры);</li>
<li><code>OnShow</code> – когда форма (окно) становится видимой;</li>
<li><code>OnPaint</code> – при необходимости нарисовать или перерисовать форму;</li>
<li><code>OnResize</code> - при изменении размеров формы на экране;</li>
<li><code>OnDeactivate</code> – при потере формой фокуса ввода (окно становится неактивным);</li>
<li><code>OnHide</code> – при удалении формы с экрана (окно становится невидимым);</li>
<li><code>OnCloseQuery</code> – при попытке закрыть форму - обычно используется для создания запроса-подтверждения необходимости закрытия окна;</li>
<li><code>OnClose</code> – при закрытии формы;</li>
<li><code>OnDestroy</code> – при уничтожении формы;</li>
</ul>
</li>
<li>
<p>от клавиатуры и мыши:</p>
<ul>
<li><code>OnKeyPressed</code> – при нажатии клавиш, которым соответствует код ANSI;</li>
<li><code>OnKeyDown</code>, <code>OnKeyUp</code> – при нажатии и отпускании любых клавиш;</li>
<li><code>OnClick</code>, <code>OnDblClick</code> – при обычном и двойном нажатии клавиш мыши;</li>
<li><code>OnMouseMove</code> – при перемещении мыши (многократно);</li>
<li><code>OnMouseDown</code>, <code>OnMouseUp</code> – при нажатии и отпускании клавиш мыши;</li>
</ul>
</li>
<li>
<p>при перетаскивании объекта мышью:</p>
<ul>
<li><code>OnDragDrop</code> – в момент опускания объекта на форму;</li>
<li><code>OnDragOver</code> – в процессе перетаскивания объекта над формой (многократно);</li>
</ul>
</li>
<li>
<p>другие:</p>
<ul>
<li><code>OnHelp</code> – при вызове подсказки;</li>
<li><code>OnChange</code> – при изменении содержимого компонент.</li>
</ul>
</li>
</ol>
<hr>
<hr>
<h1 id="ещё-полезные-вещи">Ещё полезные вещи</h1>
<h2 id="некоторые-опциидирективы-компилятора">Некоторые опции/директивы компилятора</h2>
<p>Каждая из них может быть включена директивой <code>{$@+}</code> или <code>{$&lt;dir&gt; On}</code> и отключена директивой <code>{$@-}</code> или <code>{$&lt;dir&gt; Off}</code> , где <code>@</code> – одна из допустимых букв, <code>&lt;dir&gt;</code> – полное имя директивы (см. таблицу)</p>

<table>
<thead>
<tr>
<th>Краткая форма</th>
<th>Полная форма</th>
<th>По умолчанию*</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>{$X}</code></td>
<td><code>{$ExtendedSyntax}</code></td>
<td><code>+</code></td>
<td>Если включено можно: использовать <code>result</code> в функциях для возврата значений; вызывать функции как процедуры (никуда не возвращая результат); Обрабатывать массив <code>char</code>'ов как строки</td>
</tr>
<tr>
<td><code>{$I}</code></td>
<td><code>{$IOChecks}</code></td>
<td><code>+</code></td>
<td>Если включено: проверяет правильность завершения операций ввода-вывода, если ошибка – вызывает ошибку выполнения программы; иначе – функция <code>IOResult(): Word</code> возвращает код статуса последней операции ввода-вывода</td>
</tr>
<tr>
<td><code>{$H}</code></td>
<td><code>{$LongStrings}</code></td>
<td><code>+</code></td>
<td>Если включено: тип <code>string</code> присваивается к <code>AnsiString</code>, иначе к <code>ShortString</code>. (<em>Хотя, кажется, с Delphi 2009 <code>string</code> всегда считается <code>UnicodeString</code></em>)</td>
</tr>
<tr>
<td><code>{$Q}</code>**</td>
<td><code>{$OverFlowChecks}</code>**</td>
<td><code>-</code></td>
<td>Если включено: проверяет наличие переполнения при выполнении некоторых арифметических операций. При переполнении программа аварийно завершается</td>
</tr>
<tr>
<td><code>{$R}</code>**</td>
<td><code>{$RangeChecks}</code>**</td>
<td><code>-</code></td>
<td>Если включено: проверяет правильность вычисленных индексов массивов. При выходе за рамки программа аварийно завершается</td>
</tr>
</tbody>
</table><p>* – в <em>Delphi Pascal 2009</em><br>
** – являются отладочными директивами, поэтому с ними выполнение программы потребует больше времени и/или памяти</p>
<h6 id="источник-delphibasics.co.uk">Источник: <a href="http://www.delphibasics.co.uk/ByType.asp?Type=Compiler%20Directive">delphibasics.co.uk</a></h6>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>
