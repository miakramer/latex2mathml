![version](https://img.shields.io/pypi/v/latex2mathml.svg)![license](https://img.shields.io/pypi/l/latex2mathml.svg)![status](https://img.shields.io/pypi/status/latex2mathml.svg)

# latex2mathml
Pure Python library for LaTeX to MathML conversion.

## Demo
[latex2mathml Demo](http://www.roniemartinez.space/latex2mathml)

## Usage

```python
import latex2mathml.converter

latex_input = "<your_latex_string>"
mathml_output = latex2mathml.converter.convert(latex_input)
```

## Examples

### Identifiers, Numbers and Operators

<table>
    <tr>
        <th width="33%">LaTeX Input</th>
        <th width="33%">MathML Output</th>
        <th width="33%">Preview</th>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">x</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mi&gt;x&lt;/mi&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mi>x</mi>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">xyz</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mi&gt;x&lt;/mi&gt;
        &lt;mi&gt;y&lt;/mi&gt;
        &lt;mi&gt;z&lt;/mi&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mi>x</mi>
                    <mi>y</mi>
                    <mi>z</mi>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">3</pre></td>
        <td valign="top"><pre lang="html">     
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mn&gt;3&lt;/mn&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mn>3</mn>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">444</pre></td>
        <td valign="top"><pre lang="html">     
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mn&gt;444&lt;/mn&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mn>444</mn>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">12.34</pre></td>
        <td valign="top"><pre lang="html">     
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mn&gt;12.34&lt;/mn&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mn>12.34</mn>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">12x</pre></td>
        <td valign="top"><pre lang="html">     
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mn&gt;12&lt;/mn&gt;
        &lt;mi&gt;x&lt;/mi&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mn>12</mn>
                    <mi>x</mi>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">3-2</pre></td>
        <td valign="top"><pre lang="html">     
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mn&gt;3&lt;/mn&gt;
        &lt;mo&gt;&#x02212;&lt;/mo&gt;
        &lt;mn&gt;2&lt;/mn&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mn>3</mn>
                    <mo>−</mo>
                    <mn>2</mn>
                </mrow>
            </math>
        </td>
    </tr>
</table>

### Subscripts and Superscripts

<table>
    <tr>
        <th width="33%">LaTeX Input</th>
        <th width="33%">MathML Output</th>
        <th width="33%">Preview</th>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">a_b</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;msub&gt;
            &lt;mi&gt;a&lt;/mi&gt;
            &lt;mi&gt;b&lt;/mi&gt;
        &lt;/msub&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <msub>
                        <mi>a</mi>
                        <mi>b</mi>
                    </msub>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">a^b</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;msup&gt;
            &lt;mi&gt;a&lt;/mi&gt;
            &lt;mi&gt;b&lt;/mi&gt;
        &lt;/msup&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <msup>
                        <mi>a</mi>
                        <mi>b</mi>
                    </msup>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">a_b^c</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;msubsup&gt;
            &lt;mi&gt;a&lt;/mi&gt;
            &lt;mi&gt;b&lt;/mi&gt;
            &lt;mi&gt;c&lt;/mi&gt;
        &lt;/msubsup&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <msubsup>
                        <mi>a</mi>
                        <mi>b</mi>
                        <mi>c</mi>
                    </msubsup>
                </mrow>
            </math>
        </td>
    </tr>
</table>

### Fractions

<table>
    <tr>
        <th width="33%">LaTeX Input</th>
        <th width="33%">MathML Output</th>
        <th width="33%">Preview</th>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">\frac{1}{2}</pre></td>
        <td valign="top"><pre lang="html">      
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mfrac&gt;
            &lt;mrow&gt;
                &lt;mn&gt;1&lt;/mn&gt;
            &lt;/mrow&gt;
            &lt;mrow&gt;
                &lt;mn&gt;2&lt;/mn&gt;
            &lt;/mrow&gt;
        &lt;/mfrac&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mfrac>
                        <mrow>
                            <mn>1</mn>
                        </mrow>
                        <mrow>
                            <mn>2</mn>
                        </mrow>
                    </mfrac>
                </mrow>
            </math>
        </td>
    </tr>
</table>

### Roots

<table>
    <tr>
        <th width="33%">LaTeX Input</th>
        <th width="33%">MathML Output</th>
        <th width="33%">Preview</th>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">\sqrt{2}</pre></td>
        <td valign="top"><pre lang="html">      
&lt;math&gt;
    &lt;mrow&gt;
        &lt;msqrt&gt;
            &lt;mrow&gt;
                &lt;mn&gt;2&lt;/mn&gt;
            &lt;/mrow&gt;
        &lt;/msqrt&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <msqrt>
                        <mrow>
                            <mn>2</mn>
                        </mrow>
                    </msqrt>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">\sqrt[3]{2}</pre></td>
        <td valign="top"><pre lang="html"> 
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mroot&gt;
            &lt;mrow&gt;
                &lt;mn&gt;2&lt;/mn&gt;
            &lt;/mrow&gt;
            &lt;mrow&gt;
                &lt;mn&gt;3&lt;/mn&gt;
            &lt;/mrow&gt;
        &lt;/mroot&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mroot>
                        <mrow>
                            <mn>2</mn>
                        </mrow>
                        <mrow>
                            <mn>3</mn>
                        </mrow>
                    </mroot>
                </mrow>
            </math>
        </td>
    </tr>
</table>

### Matrices

<table>
    <tr>
        <th width="20%">LaTeX Input</th>
        <th width="30%">MathML Output</th>
        <th width="50%">Preview</th>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">\begin{matrix}a & b \\ c & d \end{matrix}</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mtable&gt;
            &lt;mtr&gt;
                &lt;mtd&gt;
                    &lt;mi&gt;a&lt;/mi&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mi&gt;b&lt;/mi&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
            &lt;mtr&gt;
                &lt;mtd&gt;
                    &lt;mi&gt;c&lt;/mi&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mi&gt;d&lt;/mi&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
        &lt;/mtable&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mtable>
                        <mtr>
                            <mtd>
                                <mi>a</mi>
                            </mtd>
                            <mtd>
                                <mi>b</mi>
                            </mtd>
                        </mtr>
                        <mtr>
                            <mtd>
                                <mi>c</mi>
                            </mtd>
                            <mtd>
                                <mi>d</mi>
                            </mtd>
                        </mtr>
                    </mtable>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">\begin{matrix*}[r]a & b \\ c & d \end{matrix*}</pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;mtable&gt;
            &lt;mtr&gt;
                &lt;mtd columnalign='right'&gt;
                    &lt;mi&gt;a&lt;/mi&gt;
                &lt;/mtd&gt;
                &lt;mtd columnalign='right'&gt;
                    &lt;mi&gt;b&lt;/mi&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
            &lt;mtr&gt;
                &lt;mtd columnalign='right'&gt;
                    &lt;mi&gt;c&lt;/mi&gt;
                &lt;/mtd&gt;
                &lt;mtd columnalign='right'&gt;
                    &lt;mi&gt;d&lt;/mi&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
        &lt;/mtable&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top">
            <math>
                <mrow>
                    <mtable>
                        <mtr>
                            <mtd columnalign='right'>
                                <mi>a</mi>
                            </mtd>
                            <mtd columnalign='right'>
                                <mi>b</mi>
                            </mtd>
                        </mtr>
                        <mtr>
                            <mtd columnalign='right'>
                                <mi>c</mi>
                            </mtd>
                            <mtd columnalign='right'>
                                <mi>d</mi>
                            </mtd>
                        </mtr>
                    </mtable>
                </mrow>
            </math>
        </td>
    </tr>
    <tr>
        <td valign="top"><pre lang="latex">
A_{m,n} = 
 \begin{bmatrix}
  a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
  a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
  \vdots  & \vdots  & \ddots & \vdots  \\
  a_{m,1} & a_{m,2} & \cdots & a_{m,n} 
 \end{bmatrix}
        </pre></td>
        <td valign="top"><pre lang="html">
&lt;math&gt;
    &lt;mrow&gt;
        &lt;msub&gt;
            &lt;mi&gt;A&lt;/mi&gt;
            &lt;mrow&gt;
                &lt;mi&gt;m&lt;/mi&gt;
                &lt;mi&gt;,&lt;/mi&gt;
                &lt;mi&gt;n&lt;/mi&gt;
            &lt;/mrow&gt;
        &lt;/msub&gt;
        &lt;mo&gt;&#x0003D;&lt;/mo&gt;
        &lt;mo&gt;&#x0005B;&lt;/mo&gt;
        &lt;mtable&gt;
            &lt;mtr&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mn&gt;1&lt;/mn&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mn&gt;1&lt;/mn&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mn&gt;1&lt;/mn&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mn&gt;2&lt;/mn&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022EF;&lt;/mo&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mn&gt;1&lt;/mn&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mi&gt;n&lt;/mi&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
            &lt;mtr&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mn&gt;2&lt;/mn&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mn&gt;1&lt;/mn&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mn&gt;2&lt;/mn&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mn&gt;2&lt;/mn&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022EF;&lt;/mo&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mn&gt;2&lt;/mn&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mi&gt;n&lt;/mi&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
            &lt;mtr&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022EE;&lt;/mo&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022EE;&lt;/mo&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022F1;&lt;/mo&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022EE;&lt;/mo&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
            &lt;mtr&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mi&gt;m&lt;/mi&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mn&gt;1&lt;/mn&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mi&gt;m&lt;/mi&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mn&gt;2&lt;/mn&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;mo&gt;&#x022EF;&lt;/mo&gt;
                &lt;/mtd&gt;
                &lt;mtd&gt;
                    &lt;msub&gt;
                        &lt;mi&gt;a&lt;/mi&gt;
                        &lt;mrow&gt;
                            &lt;mi&gt;m&lt;/mi&gt;
                            &lt;mi&gt;,&lt;/mi&gt;
                            &lt;mi&gt;n&lt;/mi&gt;
                        &lt;/mrow&gt;
                    &lt;/msub&gt;
                &lt;/mtd&gt;
            &lt;/mtr&gt;
        &lt;/mtable&gt;
        &lt;mo&gt;&#x0005D;&lt;/mo&gt;
    &lt;/mrow&gt;
&lt;/math&gt;
        </pre></td>
        <td valign="top"><math>
                <mrow>
                    <msub>
                        <mi>A</mi>
                        <mrow>
                            <mi>m</mi>
                            <mi>,</mi>
                            <mi>n</mi>
                        </mrow>
                    </msub>
                    <mo>=</mo>
                    <mo>[</mo>
                    <mtable>
                        <mtr>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mn>1</mn>
                                        <mi>,</mi>
                                        <mn>1</mn>
                                    </mrow>
                                </msub>
                            </mtd>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mn>1</mn>
                                        <mi>,</mi>
                                        <mn>2</mn>
                                    </mrow>
                                </msub>
                            </mtd>
                            <mtd>
                                <mo>⋯</mo>
                            </mtd>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mn>1</mn>
                                        <mi>,</mi>
                                        <mi>n</mi>
                                    </mrow>
                                </msub>
                            </mtd>
                        </mtr>
                        <mtr>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mn>2</mn>
                                        <mi>,</mi>
                                        <mn>1</mn>
                                    </mrow>
                                </msub>
                            </mtd>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mn>2</mn>
                                        <mi>,</mi>
                                        <mn>2</mn>
                                    </mrow>
                                </msub>
                            </mtd>
                            <mtd>
                                <mo>⋯</mo>
                            </mtd>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mn>2</mn>
                                        <mi>,</mi>
                                        <mi>n</mi>
                                    </mrow>
                                </msub>
                            </mtd>
                        </mtr>
                        <mtr>
                            <mtd>
                                <mo>⋮</mo>
                            </mtd>
                            <mtd>
                                <mo>⋮</mo>
                            </mtd>
                            <mtd>
                                <mo>⋱</mo>
                            </mtd>
                            <mtd>
                                <mo>⋮</mo>
                            </mtd>
                        </mtr>
                        <mtr>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mi>m</mi>
                                        <mi>,</mi>
                                        <mn>1</mn>
                                    </mrow>
                                </msub>
                            </mtd>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mi>m</mi>
                                        <mi>,</mi>
                                        <mn>2</mn>
                                    </mrow>
                                </msub>
                            </mtd>
                            <mtd>
                                <mo>⋯</mo>
                            </mtd>
                            <mtd>
                                <msub>
                                    <mi>a</mi>
                                    <mrow>
                                        <mi>m</mi>
                                        <mi>,</mi>
                                        <mi>n</mi>
                                    </mrow>
                                </msub>
                            </mtd>
                        </mtr>
                    </mtable>
                    <mo>]</mo>
                </mrow>
            </math>
        </td>
    </tr>
</table>

### References
#### LaTeX
* https://en.wikibooks.org/wiki/LaTeX/Mathematics
* http://artofproblemsolving.com/wiki/index.php?title=Main_Page
* http://milde.users.sourceforge.net/LUCR/Math/
* http://www.forkosh.com/mimetextutorial.html

#### MathML
* http://www.xmlmind.com/tutorials/MathML/


### Author
* [Ronie Martinez](mailto:ronmarti18@gmail.com)
