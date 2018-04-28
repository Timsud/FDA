# FDA

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[181]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1">####### Timur Sudak a1277687 ##################################</span>
install.packages<span class="p">(</span><span class="s">&quot;nlme&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;ISLR&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;dummy&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;MASS&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;qqtest&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;caret&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;hydroGOF&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;data.table&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;leaps&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&#39;VIF&#39;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;rpart&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;randomForest&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;olsrr&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;fmsb&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>  
install.packages<span class="p">(</span><span class="s">&quot;forecast&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;ridge&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;car&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
install.packages<span class="p">(</span><span class="s">&quot;xlsx&quot;</span><span class="p">,</span>repos <span class="o">=</span> <span class="s">&quot;http://cran.us.r-project.org&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;nlme&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;ISLR&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;dummy&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;MASS&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;qqtest&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;caret&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;hydroGOF&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;data.table&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;leaps&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;VIF&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;rpart&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;randomForest&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;olsrr&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;fmsb&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;forecast&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;ridge&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
Warning message:
&#34;package &#39;car&#39; is in use and will not be installed&#34;Installing package into &#39;C:/Users/User/Documents/R/win-library/3.4&#39;
(as &#39;lib&#39; is unspecified)
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>package &#39;xlsx&#39; successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\User\AppData\Local\Temp\RtmpKq8TcV\downloaded_packages
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[182]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kn">library</span><span class="p">(</span><span class="s">&quot;randomForest&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;rpart&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;VIF&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;leaps&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;data.table&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;MASS&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;hydroGOF&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;ISLR&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;qqtest&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;nlme&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;caret&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;dummy&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;olsrr&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;fmsb&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;forecast&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;ridge&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;car&quot;</span><span class="p">)</span>
<span class="kn">library</span><span class="p">(</span><span class="s">&quot;xlsx&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>Loading required package: rJava
Loading required package: xlsxjars
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">setwd</span><span class="p">(</span><span class="s">&quot;C:/Users/User/Documents/Data for R/Going through Timw Series/Projects in time series/from Nastia&quot;</span><span class="p">)</span>
ant_d <span class="o">=</span> read.csv<span class="p">(</span><span class="s">&quot;Anti-Depressiva.csv&quot;</span><span class="p">,</span> header<span class="o">=</span><span class="kc">TRUE</span><span class="p">,</span> sep<span class="o">=</span> <span class="s">&quot;;&quot;</span><span class="p">)</span>
ant_d
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th scope=col>y</th><th scope=col>age</th><th scope=col>TRT</th></tr></thead>
<tbody>
	<tr><td>56</td><td>21</td><td>A </td></tr>
	<tr><td>41</td><td>23</td><td>B </td></tr>
	<tr><td>40</td><td>30</td><td>B </td></tr>
	<tr><td>28</td><td>19</td><td>C </td></tr>
	<tr><td>55</td><td>28</td><td>A </td></tr>
	<tr><td>25</td><td>23</td><td>C </td></tr>
	<tr><td>46</td><td>33</td><td>B </td></tr>
	<tr><td>71</td><td>67</td><td>C </td></tr>
	<tr><td>48</td><td>42</td><td>B </td></tr>
	<tr><td>63</td><td>33</td><td>A </td></tr>
	<tr><td>52</td><td>33</td><td>A </td></tr>
	<tr><td>62</td><td>56</td><td>C </td></tr>
	<tr><td>50</td><td>45</td><td>C </td></tr>
	<tr><td>45</td><td>43</td><td>B </td></tr>
	<tr><td>58</td><td>38</td><td>A </td></tr>
	<tr><td>46</td><td>37</td><td>C </td></tr>
	<tr><td>58</td><td>43</td><td>B </td></tr>
	<tr><td>34</td><td>27</td><td>C </td></tr>
	<tr><td>65</td><td>43</td><td>A </td></tr>
	<tr><td>55</td><td>45</td><td>B </td></tr>
	<tr><td>57</td><td>48</td><td>B </td></tr>
	<tr><td>59</td><td>47</td><td>C </td></tr>
	<tr><td>64</td><td>48</td><td>A </td></tr>
	<tr><td>61</td><td>53</td><td>A </td></tr>
	<tr><td>62</td><td>58</td><td>B </td></tr>
	<tr><td>36</td><td>29</td><td>C </td></tr>
	<tr><td>69</td><td>53</td><td>A </td></tr>
	<tr><td>47</td><td>29</td><td>B </td></tr>
	<tr><td>73</td><td>58</td><td>A </td></tr>
	<tr><td>64</td><td>66</td><td>B </td></tr>
	<tr><td>60</td><td>67</td><td>B </td></tr>
	<tr><td>62</td><td>63</td><td>A </td></tr>
	<tr><td>71</td><td>59</td><td>C </td></tr>
	<tr><td>62</td><td>51</td><td>C </td></tr>
	<tr><td>70</td><td>67</td><td>A </td></tr>
	<tr><td>71</td><td>63</td><td>C </td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Construct a predictive model with “y” as target variable!
Apply different contrasting strategies and interpret the parameter estimates!
Now we want to do these two points in one exercise.
We will do two contrasting strategies and will fit the model for every strategy.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">options</span><span class="p">(</span>contrasts<span class="o">=</span><span class="kt">c</span><span class="p">(</span><span class="s">&quot;contr.treatment&quot;</span><span class="p">,</span> <span class="s">&quot;contr.poly&quot;</span><span class="p">))</span>
contrasts<span class="p">(</span>ant_d<span class="p">[,</span><span class="m">3</span><span class="p">])</span>
<span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>y<span class="o">~</span>age<span class="o">+</span>TRT<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>B</th><th scope=col>C</th></tr></thead>
<tbody>
	<tr><th scope=row>A</th><td>0</td><td>0</td></tr>
	<tr><th scope=row>B</th><td>1</td><td>0</td></tr>
	<tr><th scope=row>C</th><td>0</td><td>1</td></tr>
</tbody>
</table>

</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = y ~ age + TRT, data = ant_d)

Residuals:
     Min       1Q   Median       3Q      Max 
-12.5732  -3.3922   0.9829   3.9613   9.5062 

Coefficients:
             Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)  32.54335    3.58105   9.088 2.23e-10 ***
age           0.66446    0.06978   9.522 7.42e-11 ***
TRTB         -9.80758    2.46471  -3.979 0.000371 ***
TRTC        -10.25276    2.46542  -4.159 0.000224 ***
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 6.035 on 32 degrees of freedom
Multiple R-squared:  0.784,	Adjusted R-squared:  0.7637 
F-statistic: 38.71 on 3 and 32 DF,  p-value: 9.287e-11
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>All Coefficients are signifikant at significance level of 0.05. The model explains 76.37 %  of the variation.</p>
<p>Interpretation of the treatment contrast:</p>
<p>For the group A the model would be the baseline. We would get our model for group B if we add our coefficient
TRTB it means that measurement success for group B would be on -9.80758 smaller. And if we add TRTC our measurement success would be smaller on -10.25276 than our baseline.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">options</span><span class="p">(</span>contrasts<span class="o">=</span><span class="kt">c</span><span class="p">(</span><span class="s">&quot;contr.sum&quot;</span><span class="p">,</span> <span class="s">&quot;contr.poly&quot;</span><span class="p">))</span>
contrasts<span class="p">(</span>ant_d<span class="p">[,</span><span class="m">3</span><span class="p">])</span>
<span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>y<span class="o">~</span>age<span class="o">+</span>TRT<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<tbody>
	<tr><th scope=row>A</th><td> 1</td><td> 0</td></tr>
	<tr><th scope=row>B</th><td> 0</td><td> 1</td></tr>
	<tr><th scope=row>C</th><td>-1</td><td>-1</td></tr>
</tbody>
</table>

</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = y ~ age + TRT, data = ant_d)

Residuals:
     Min       1Q   Median       3Q      Max 
-12.5732  -3.3922   0.9829   3.9613   9.5062 

Coefficients:
            Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) 25.85657    3.23845   7.984 4.10e-09 ***
age          0.66446    0.06978   9.522 7.42e-11 ***
TRT1         6.68678    1.42341   4.698 4.77e-05 ***
TRT2        -3.12080    1.42259  -2.194   0.0356 *  
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 6.035 on 32 degrees of freedom
Multiple R-squared:  0.784,	Adjusted R-squared:  0.7637 
F-statistic: 38.71 on 3 and 32 DF,  p-value: 9.287e-11
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>All Coefficients are signifikant at  level of 0.05. The model explains 76.37 %  of the variation.</p>
<p>Interpretation of the sum contrast:</p>
<p>Intercept is the overall mean across all groups.It means that overall measurement sucess is 25.85657.   The second coefficient is the average slope between overall mean  and age. If we increase age by one unit then our overall mesurement sucess  will increase on 0.66446 across all groups. The coefficient TRT1 is the difference between overall mean and  group 1. Measurement sucess for group 1 would be higher on 6.68678 than our overall measurement sucess.
 And TRT2 coefficient is the difference between overall mean and group 2. Measurement sucess for group 2 would be smaller on -3.12080 than our averall measurement sucess.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Which conclusions do you reach regarding the predictor “TRT”, which indicates three different treatments?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We showed that a predictor TRT does improve our Adjusted R^(2), it means increased explanation of 
the variation. So therefore we have to include this predictor in our model.</p>
<p>Here we see some examples of three different models and their comparison of Adjusted R2 values:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>y<span class="o">~</span>age<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">))</span> <span class="c1">#Here our Adjusted R2 is 0.624.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = y ~ age, data = ant_d)

Residuals:
     Min       1Q   Median       3Q      Max 
-15.8916  -5.7463  -0.4105   4.7013  16.4607 

Coefficients:
            Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) 25.33935    4.08258   6.207 4.65e-07 ***
age          0.67619    0.08797   7.687 6.15e-09 ***
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 7.613 on 34 degrees of freedom
Multiple R-squared:  0.6347,	Adjusted R-squared:  0.624 
F-statistic: 59.08 on 1 and 34 DF,  p-value: 6.155e-09
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>y<span class="o">~</span>age<span class="o">+</span>TRT<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">))</span> <span class="c1"># Here our Adjusted R2 is 0.7637.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = y ~ age + TRT, data = ant_d)

Residuals:
     Min       1Q   Median       3Q      Max 
-12.5732  -3.3922   0.9829   3.9613   9.5062 

Coefficients:
            Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) 25.85657    3.23845   7.984 4.10e-09 ***
age          0.66446    0.06978   9.522 7.42e-11 ***
TRT1         6.68678    1.42341   4.698 4.77e-05 ***
TRT2        -3.12080    1.42259  -2.194   0.0356 *  
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 6.035 on 32 degrees of freedom
Multiple R-squared:  0.784,	Adjusted R-squared:  0.7637 
F-statistic: 38.71 on 3 and 32 DF,  p-value: 9.287e-11
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>y<span class="o">~</span>age<span class="o">*</span>TRT<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">))</span> <span class="c1"># here our Adjusted R2 is 0.9001.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = y ~ age * TRT, data = ant_d)

Residuals:
    Min      1Q  Median      3Q     Max 
-6.4366 -2.7637  0.1887  2.9075  6.5634 

Coefficients:
            Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) 27.54839    2.12264  12.978 7.68e-14 ***
age          0.62919    0.04574  13.757 1.71e-14 ***
TRT1        19.96720    3.06317   6.518 3.31e-07 ***
TRT2         1.36981    3.06673   0.447    0.658    
age:TRT1    -0.29869    0.06562  -4.552 8.23e-05 ***
age:TRT2    -0.10551    0.06641  -1.589    0.123    
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 3.925 on 30 degrees of freedom
Multiple R-squared:  0.9143,	Adjusted R-squared:  0.9001 
F-statistic: 64.04 on 5 and 30 DF,  p-value: 4.264e-15
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1">#Compare and interpret models with and without interaction terms!</span>
einf_mod <span class="o">=</span> lm<span class="p">(</span>y<span class="o">~</span>age<span class="o">+</span>TRT<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">)</span>
mod_int <span class="o">&lt;-</span>  lm<span class="p">(</span>y<span class="o">~</span>age<span class="o">*</span>TRT<span class="p">,</span> data <span class="o">=</span> ant_d<span class="p">)</span>
<span class="kp">summary</span><span class="p">(</span>mod_int<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = y ~ age * TRT, data = ant_d)

Residuals:
    Min      1Q  Median      3Q     Max 
-6.4366 -2.7637  0.1887  2.9075  6.5634 

Coefficients:
            Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) 27.54839    2.12264  12.978 7.68e-14 ***
age          0.62919    0.04574  13.757 1.71e-14 ***
TRT1        19.96720    3.06317   6.518 3.31e-07 ***
TRT2         1.36981    3.06673   0.447    0.658    
age:TRT1    -0.29869    0.06562  -4.552 8.23e-05 ***
age:TRT2    -0.10551    0.06641  -1.589    0.123    
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 3.925 on 30 degrees of freedom
Multiple R-squared:  0.9143,	Adjusted R-squared:  0.9001 
F-statistic: 64.04 on 5 and 30 DF,  p-value: 4.264e-15
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">

<pre><code>                          This is our model with interaction effects.
</code></pre>
<p>Age: if we increase one unit of age our sucess will increase on 0.33051 for all groups.</p>
<p>TRTB: Our Sucess for Group B Would be smaller on -18.59739 than in group A.</p>
<p>TRTC: Our Sucess for Group C would be smaller on -14.30421 than in group A.</p>
<p>age:TRTB: If we increase one unit of age our sucess for group B would be higher on 0.19318.It means that difference betwenn 
group A and B increases on 0.19318.</p>
<p>age:TRTC: If we increase one unit of age our sucess for group C would be higher  on  0.70288. It means that difference betwenn group A and C increases on 0.70288.</p>
<p>All our coefficients are siginificant except of one coefficient age:TRTB.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>anova<span class="p">(</span>einf_mod<span class="p">,</span>mod_int<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th scope=col>Res.Df</th><th scope=col>RSS</th><th scope=col>Df</th><th scope=col>Sum of Sq</th><th scope=col>F</th><th scope=col>Pr(&gt;F)</th></tr></thead>
<tbody>
	<tr><td>32          </td><td>1165.5747   </td><td>NA          </td><td>     NA     </td><td>      NA    </td><td>          NA</td></tr>
	<tr><td>30          </td><td> 462.1477   </td><td> 2          </td><td>703.427     </td><td>22.83124    </td><td>9.410457e-07</td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We see that we have significant difference between two models, our p&lt;0.05. Normally bigger models explain the same amount of variation than smaller model. And in our case because of significance it makes sense to include the interaction term.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1">#Visualize the data and the different models estimated</span>
plot<span class="p">(</span>ant_d<span class="o">$</span>y <span class="o">~</span> ant_d<span class="o">$</span>age<span class="p">,</span> col <span class="o">=</span> <span class="kp">as.numeric</span><span class="p">(</span>ant_d<span class="o">$</span>TRT<span class="p">),</span> pch <span class="o">=</span> <span class="m">5</span><span class="p">)</span>
abline<span class="p">(</span>lm<span class="p">(</span>ant_d<span class="o">$</span>y <span class="o">~</span> ant_d<span class="o">$</span>age<span class="p">,</span> subset <span class="o">=</span> ant_d<span class="o">$</span>TRT <span class="o">==</span> <span class="s">&quot;A&quot;</span><span class="p">),</span> col <span class="o">=</span> <span class="s">&quot;black&quot;</span><span class="p">)</span>
abline<span class="p">(</span>lm<span class="p">(</span>ant_d<span class="o">$</span>y <span class="o">~</span> ant_d<span class="o">$</span>age<span class="p">,</span> subset <span class="o">=</span> ant_d<span class="o">$</span>TRT <span class="o">==</span> <span class="s">&quot;B&quot;</span><span class="p">),</span> col <span class="o">=</span> <span class="s">&quot;red&quot;</span><span class="p">)</span>
abline<span class="p">(</span>lm<span class="p">(</span>ant_d<span class="o">$</span>y <span class="o">~</span> ant_d<span class="o">$</span>age<span class="p">,</span> subset <span class="o">=</span> ant_d<span class="o">$</span>TRT <span class="o">==</span> <span class="s">&quot;C&quot;</span><span class="p">),</span> col <span class="o">=</span> <span class="s">&quot;blue&quot;</span><span class="p">)</span>
abline<span class="p">(</span>lm<span class="p">(</span>ant_d<span class="o">$</span>y <span class="o">~</span> ant_d<span class="o">$</span>age<span class="p">),</span> lty <span class="o">=</span> <span class="m">2</span><span class="p">,</span>col <span class="o">=</span> <span class="s">&quot;yellow&quot;</span><span class="p">)</span>
legend<span class="p">(</span><span class="s">&quot;bottomright&quot;</span><span class="p">,</span> legend <span class="o">=</span> <span class="kt">c</span><span class="p">(</span><span class="s">&quot;A&quot;</span><span class="p">,</span><span class="s">&quot;B&quot;</span><span class="p">,</span><span class="s">&quot;C&quot;</span><span class="p">),</span> col <span class="o">=</span> <span class="kt">c</span><span class="p">(</span><span class="s">&quot;black&quot;</span><span class="p">,</span> <span class="s">&quot;red&quot;</span><span class="p">,</span> <span class="s">&quot;blue&quot;</span><span class="p">),</span> lty <span class="o">=</span> <span class="kp">rep</span><span class="p">(</span><span class="m">1</span><span class="p">,</span><span class="m">3</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAPFBMVEUAAAAAAP8AzQBNTU1o
aGh8fHyMjIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD/AAD//wD///86BDjZAAAA
CXBIWXMAABJ0AAASdAHeZh94AAAgAElEQVR4nO3diXqaTBhA4Ym4JkZNuf97reAGyjLLNxtz
3uf5W9u/Ck08BYYRVA3AmYq9AsASEBIggJAAAYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAA
AYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAAAYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAA
AYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAAAYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAA
AYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAAAYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAA
AYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAAAYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAA
AYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAAAYQECCAkQAAhAQIICRBASIAAQgIEEBIggJAA
AYQECCAkQAAhAQIICRBASIAAQgIEBAhJAWn5mvsDFu9y+XAiLALQ9/U19ycICZgzmxEhAbM0
OiIkYIZOR4QETNPqiJCASXodERIwRbMjQgIm6HZESMA47Y4ICRil3xEhAWMMOiIkYIRJR4QE
DDPqiJCAIfPTVPsICfhkmBEhIUu+3yDGHRESMqQ8v0PMOyIk5EfVft8iFh0RErKjOj/6YNMR
ISE7qveTOKuOCAm5UR8PRNl1REjIjBp8KMayI0JCXtToL0TYdkRIyIzXLZJ1R4SE3Hg8RrLv
iJCQnfvwt/ibxHR6XQ8hITt+Tsi6ZERIyJGPKUJuHREScpRcR4QE1O4dERIg0BEhAQIdERIg
0BEhoXgSHRESSifSUf3P/CmEhAUR6ejfP7ZIKJpMR+zaoWwy+3U1IaFkTtNU7+4HR4SE7K0s
n2Se0ceS/j0GGQgJuVvZlHR9kk1Hb0t6jdUREjK3qi22Sc32yOZJ/SV1xrwJCXlbdX40edKX
zZPGl0RIyNqq95P+s77Mn9Vf1NsZWEJCzlYfD/Se9WX+rN6i/r3PZCAkZGw1+HD+WV+vh1aL
+pwQREjI12r0F9PP+ur+wmJRAxPrCAkZs9siWXQ0u6igIf0etqqx3f/6WgTKYnOM9GV3ZHX7
s9eDo8EnBQzpslYvGy+LQHFWxsPfX88/vjIetWsyGn5SwJD2qvo5tY/Ox0rtfSwCBTI8Iftl
86T7kv6NPylgSJU6PR+fVOVjESiRyRSh5zRVu3lFavRJAUPqXWN2+oKzhAQDBh3ZPOlFrUbf
mWyRUA6HT038+zd9qeSwx0jHc/uIYyTEYN9RO5HhfvH+wT9gc0l/63f5pjNqt754WQQwyqGj
9sf7u/Ljzdm8nwOfR9q355Gq7YHzSAhN7Ore/ZsGqqkNld4L+kNIkCZ4lfxXUmq4LuNXlKS6
/CwC5bLt6N/QNRnaUYf+2zTk8Hc1s0PnvghgmGVH/wY/S67qz3/rg55HUtvJIQb3RQCDbDvq
/mJoh27g/+qzD6kZ9dZKiZAgSebqdQM7dP3/afF6Vuuh6stWqd3R3yKAAVYdDX3maGKYO/QU
oVMzAL79Pk1vmAhp0cJ+e62uAvn5UfJbRSlMEbpvE0/7anZgjpCWzMetlMdJbI6eb9fxFY8y
afX0vV0TUqmmZqzJc+9I72xMrNnffhaB9FlPBLDiOMygf06TkBDU7D6SKIuOOmeOTCYGpDOz
IfAiEIXLlBpz5h29LopvOL2GkBDQ0IQ1fyw6an+0maRGSAjnY8KaV3YdWc70JCQEFHKLZDPO
YD9fmpAQUrhjJNOO/rl96oCQEJT95+DMGHZkdVvyLkJCYEFOyJp0dN0SDUysM0RICC3AFCH9
jtr9OfeOCAnh+f72ak9TFfwsNiFhafQyuo8tfEzztkRIWBidjh6bIqmMCAlLM9/Ra4dOLCNC
wsLMdOTtElWEhCWZ7Mjndd4ICQsy3tH7pkju6Oj++kGekuAisEBjHX1siqQzIiQsyHBHAzt0
4hkREpZjoKNwl78mJCzER0dBryFPSFiGt47GKpI/OrovL8hTElwEFqU3vW58h85XRoSERehk
NLVD5y0jQsISPDqKeGstQkL2bh3FvT8dISF3TUezFfk7OrohJGTuS2OHzndGhITMqS+NN4v3
jAgJObtuimRuxueOkJCn2w7dfEcBtkYNQkKGHkdFsx35Pzi6IyTk5jW2MN+R51V5ISTkpDdC
l1BHhIR8vA1zpzLO0CIkZOHjZNHcVSADbo0ahIT0DZxxncsocEeEhNQNzltIa3NUExKSNjb7
J7mOCAnJGp9Cl9Qwww0hIUlTE1EnO4qwNWoQEpIzM517qqPggwwPhIS0zH4mYrIj0VUxQUhI
h85HxdPsiJCQCr2Piic4ztAipKIk+4XVveDCaEfRDo7uCKkkAW6DbMHg2j9jHcXOiJCKour0
vrQm1/4ZnV4XPSNCKsntqxr1olVvzK6glerhUYuQiqE+HkRlfDHHpDsipGKowYeRWFzMcaSj
+EdHN4RUCDX6i9Dsris83FEqGdV/f+bPIaQspbFFsr2u8EhHLqsi6JoRW6RixD9Gsr86d9LH
R+3WiJDKoXo/hV64yzXuU+7ovlNHSOVQnR8DL9ltzH2oo0SOjp7HRoRUkDgnZJ1vtzLQUWoZ
EVJZJKYIGb2CxJ2/hjpyfU0D48NxvZE6QiqKREfaryFz56/Ix0d/YyW9DXgTEkzo7h2K3YQy
ekeD26S/j/NGhAQDetP15G5C+TlNNezR0S2X92qGzr4SEvTpnIqSvJVr5Ixe26JuOcOTGAgJ
2mYnRwjfVfyzI8EX1/A38HBsLhAhQdfMdD3xu4rHPg379/mL8Sl1hARtE1sk8Yo+Oopw5uh9
izQ1M5WQoG/4GEl4h+6u31GcM7C9Y6TpCd6EBAOf0/W8RFR/dORlGfP+nj/NfU6CkGDgbbqe
r4pS6eh5ZDT/cSNCgonXCVk/O3R3sccZnub36e4IKZSF/J1uU4R8RlT3O4o8PVVjY9QipEDS
vKScBeV1U9TqdBR7mrduR4QUSJxPMMjzHlHd78j7wiYZXImBkILQm6OWuhAV9abXxe3I6IIm
hBRC/MslOPO/Q3eTzjCD2XWBCCmA2TlqqQsUUd3tKKOtUYOQ/JuZo5a6cBV1Ooo6yKA9wtBB
SAHku0UKtUN39+oo4ELf2VzrkZDCyPMYKWxEdRod2WVESIF8zlFLXOBNUSuBcQbbjAgpkLc5
aomLEFH96CjmwZF9RoQUSj4nZONUdO8o14wIKZgspghJ7tCtzP74rSPdl3B6z9+8/UXdMiKk
cJL/O8luilZmJQ0dH42/xOjF5vT1/2FzzYiQcCO9Q7eqjbZJwx2NvcTIxeZMdHe1bU4bDb6g
/6ckuAg8eRihuwWw0k3p6/Po6P7coVeYuw6Jhs7cR4mKakIqnpexhdXHgylfX5+DDBOvMHix
OTOv83pCGRFS0XydLFoNPhzzNXACduIVhi42Z+j5l/77E/v7E1Kp/A1zr0Z/MWTs8GjkFQYu
NmfqdWxUy73VCKlIfk8WmWyRhqczBNgi3Xbq2CLBVoDZP/rHSF8jp2B9HyPZ37By9CVDPCXB
RRQq0LyFVe+nceMzGSZe4a/3k43HEIPg14KQChJu9s/42HXP1ISg2eFv45V6PP2akfzcR0Iq
RODp3FonZKene/s5IdvZpxP9ehBSCSJMRJ2aInRfmbmPTXiYIvQ6bSQ995GQFi/SdO6pjlRz
dDT/8SPpSauud0+eQkiLFuPzeXOaFfr3L/zH+MQmMQwipOVKMKL7/LZ/tQrdkd+MCGmpUtwU
NR4r9RV27XxnREiLlGhEdfuNbYa8m6upBlxF/xkR0vKkW1HzfW3PwH7dfxGEyKeN5hHSkqS6
Q/fUnoEN2VGYiurAIf0etu1NQbb7X1+LKFjqEdXtIEPQjoJlFDSky1q9bLwsolwZVHSjwnUU
MKOgIe1V9XNqH52Pldr7WESZkt+ha93n1X3JT3MbFjSjoCFV6vR8fFKVj0UUKIuIXtO8vzxM
cxsSOKOgIfW+49Pf/izeG/HlsSlqPKZ5t/t1/i/x5y2j8ddli5SrbCKq3zry/e31ON49MVk2
7DHS8dw+4hjJVU4VvYSYFuRzn27q4xshh783nVG79cXLIkqQzw5do/MZ2AAdeT00mryeXtjz
SPv2PFK1PXAeyVJWEfU/Su6/I78jDNPXimBmQ0Yyq6j3UfIv7x15HqibuXpROiGpLj+LyFnm
X5XcM5q9nl7IkC77ZqjusFZq8+NpEQuVd0S1/44CnDZKZ4t0rq5vh0vFFCEzmW6Kehfa8txR
mLOvyRwj7dT2cv1hd742tWP4W0ueEb1fr85rR4E+JlGnM2qn1OX+w3UvjxOy83Kt6P16dT47
CjoVKJHzSO3bolKdX4gvYjky3aEb4rGj0DPq0pjZsGumCB1u84Qu0wdJS3kPWUotIsPbwfb5
6yj4xNRE5tqdVLU/1dvqWtJxrY4+FrEEqVVkeDvY96t5e+soQkZTQg5/H6vXiaKDn0VkLskd
OpPbwX5cFN9XR4llFPqE7M+u/ZTs9nD2toh8pRjR5L1cP31cFN9TR8lllNLMhsCLSEyaFZne
Dfadn44SzIiQUpDkDt2N2d1g3/noKNxpIzOEFFm6EdVGd4P9vGWYj2mqiVZUE1JUCW+K7nS3
SAN33isqI0KKJ/mIWnrHSAN33pPvKOWMCCmSPCpqGI3avYh3lHZGhBRB+jt0fTPnkQbvAyvd
UeoZEVJomUXUmprZMHxbcuGO0s+IkIJyrcj9y2L3jpzoaPB3ZTvKISNCCkZgh879worWNzEe
4b+jVE8bfSCkEER26Nwv9Tv1eRo5gh3lUlFNSP4JjS3cX8TlpSY/4WlseGsk2VFGGRGSZ2Jj
C+rjgbHpaw4YGh5kqAU7yiojQvJJcIRODT40MnMVHDNjGYl1lFlGhOSL7MkiNfoLbXPXZTMy
ujkS6ii7jAjJC/mTRaltkYaVmxEhyfNzyjWdY6TRvTqhjrLMiJBkeZz9k8io3eggg0xH2Zw2
+kBIYnzP/knhPNJ4RhIdZVtRTUhCgkxEjT+zwWtHOWdESBKCTUSNNddO4yWcO8o7I0JyluN0
bhuPg6PhjZprR7lnREhOcvtkkb3nGMPwYZZjR/lnREj2iomo7hwbDQ/8uXW0hIwIyVJJFXUM
n4py6mgZGRGShXJ26N4NT45w6Cjf00YfCMlMcRF1zsAOT9ez72g5FdWEZKLATVF/IsPAFsl+
muqiMiIkbeVFVH+egP04RiKjB0LSUWRFQ95G7Ww7WlxGhDSvwB26Cb3zSJYdLTAjQppRbkRj
07z/XDtaZEZLCkl+tcqtaOrTEm4dLTSjBYXkPjW6/3IFVzQ5y/vJoqMFnTb6sJSQ3D+s032x
kiPSZN7RgiuqFxPS/eOjMheQo6J5xh0tO6OlhCRwRYPb06lo4uiow7SjpWe0kJAErrFTsylq
6GVk2tHyM1pGSAJXfWNT1NLLyLCjEjJaRkiuWyQiMmI2va6MjBYSkssxEhXdaW6NzDZHpWS0
lJAsR+3YoXvSPDgy6mjJp40+LCQki/NIRNShm5FBRyVVVC8nJMOZDaYVLby5piOt9712R4Vl
tKCQ9J9jsUMnPP8oRVrXjtTtqLiMlhSS5ivb7NCJzj9KzW2vTutqxpodFZhRWSHZji2ozo9L
8+/V0WxJeh0VmVFBITmMLajeT4vSve5jPVOSVkeFZlRKSE4jdFIT+RL01tFkSTodFZtRCSG5
niySmciXNJ2b+c13VNRpow8LD8n9ZJHARL40zV2vrm+2o6Irqpcdkswp12VukXozGea3SHMd
lZ7RckMSnP2zxGOkt5kMM8dIc9NUyWihIQnP/hH8+G0iPmYETd5elow0LC4kHxNRF31C9mbi
hOx0R2R0s6yQfE1EXdAUIY3r1fVNdkRGDwsKyed07qV0pHO9ur6pjsjoZSEh8ckiLdqflnga
76js00YflhASEXkz2hEVvck+JCryaKwjMvqQdUjs0OnT/ix5x0hHZDQg35CIyIBNRiMdkdGg
TEOiIiM2GQ13REYjMgyJHboghjoio1G5hUREYQxNryOjCTmFxKbIgtXR0cDmiNNG07IJiYhs
2GX02REVzckjJCqyY5fRR0dkNC/9kNihC+2tIzLSkXhIRBRevyMy0pNySFTkwPLo6K0jMtKV
akjs0DmxzqjXERnpSzQkInJinVG3IzIykWhI/heBIc+OOG1kiJCWxn5r9OqIiowR0rLYHxzV
z47IyAIhLYpLRveOyMgKIS2J0+ao7YiMLBESWmTkhpBC8f13ctqrazsiIweEFIjna0w6DTK0
HZGRE0IKw/NVj90yqr84beSKkIJQnR89cO5IZjVKRkhBqN5PafnTvFk5phBSCOrjgRzHrdEf
HYkgpADU4EMRjoMM10MjOhLhGNL6cBZblZFF5E+N/sKZc0Z0JMQxJKWUj5aWFZK/LZJTR+1A
HR0JcQzp8rPz0dLCQvJ6jGTpNt5NR1IEjpF+D2vpltJ5vwl5fHZe7hWdDo7up43mbrIMfTKD
Dafqul36dl+biUVkTviErGNGt5/JSJBISMdNc4kFtRFYn7FFZE90ipBERnQkyj2ky+G6OVof
L9eatjLrtMiQEvk7vaYC0ZEo15B+m8GG/en2P8TeK2m86ZanM6OOjmS5nke6boy+L4//UUms
0fsi0ONwdNSdmEpHwlzPI22PYqsysgh0CGVER+JczyOJrcjoIvBindHbxyToSJxTSPt2X+57
raq92Aq9LQIC3j9sREfyHEK6VO3owrYd+q5Et02EJOjjM3t05IFDSHu1udbzq9aX+rJRotsk
Qvpge3T0+dFXOvLBIaRKNVuhnWqGGy5aI3a/h9vma7v/FV+rZZPLiI78sA9JfZh53mXd+bPT
syAIqU8uIzryxHWLdLzt0+lskfaq+rmduT0fq+ldQUISMJgRHXniENLuGsN1K9O0cdlqHCNV
6vR8fJoOj5BeBLdGk5ujld1ycOMQ0rndR9u1v6Wq+U9R9Pb9pncECenB7uBo5Opa0x1RkguX
80inzeMEUrXTGP1mi2TOMqPh35/bHlGSg4AXP7keIx1v2y2OkTTZdDR6qcf5/TpKshfyKkKb
zqjdenITRki2xq+YOjnMsOr9BHMOIZkNfjd+9+15pGp74DzSLNGtkV5HlGQvaEg+12phbAYZ
pq7frdcRJVlz3bXbVs3Eht9q574mvqrMkXBG2h1Rki3HkPb3kbiT/ly777Wa/RRT6SGZdzR9
N4mZ07Bskdw5XyDy/cHE89o/ch9xmO6u9JAMzd2UZXY6A8dIzhxDqp5bpPkpQm1Ie7W/1PV5
P33xrpJDMt4azd7aSGNa0H34m46sOe/aVc0A3LFSh/nnNU+8TRmvL2otvFYLYTzIMH+HMK3p
dZyQdeQ62PA4N6RxJa42pMcuIFOEBnnISHOaKlOE3DifkP1pTg1pXQKlbWf3CIkpQgMMO9K4
X6X+bG86chJwZsO1t8P3Uf1cH172TBFypnPbVz41EYpkSDMjd51zRHPXeCgwJNODI627J9NR
MAFDqk+n7+/tth1y2E/PFi8uJC8Z0VFAIUMSWMRCmWU0d9rogY4CIqTcaFZER2ERUl60M6Kj
sAgpMqOjI/2M6CgwQorKV0Z0FBohxeQrIzoKjpDyYJQRHYVHSDkwzKjXkdFTYYuQItE/OtI9
bfTQ3xz9UVIQIa8ilNQi4jLJyPCl3ztimxSE1CdkK7H7x74vYon8ZTTQkc2rwJRQSGeuIuSB
RQBDHdVslPxzCOnYu+7P5CdeA6zV8thsR0Y6oiTvXLZI3fsdrWcu+eh9rXKhe3RktTs22hEl
+SZ1jCRrsSF5zejj9BFbpHAYtQvJa0YDp2E5RgqGkFJjetroaWg6w1/vJ/jjGtJh3fkEuZgl
hqS3NbIfqR6cFvTX+RE+OYZ04CL6evQOjhxO+IxMr+OEbCDOV1qdvGKqrcRDMn9n+s5ofJoq
U4TCYNTOnPl7U6cjp4wmpnvTURCOIW2Vxs1j3RaRHC97S06zePjURHyOIZ2rjeiZ2IFFJObP
9Pjd99aIjpLgvGtX2GCD6ZkZnUEGxzmldJQCQjJiOldgPiPr00YPdJQETsiaMJ29NtuR+wcc
6CgNhGREdvaawOeE6CgRUiH9atwgyXERSdA/RgqwNaKjdLiGtC/rGEl79trsIIPIp1bpKBmO
Ib060rnVmNUiUqM1/B0kIzpKiPMUoZ96o87njSrng30aJ2RnOhK6hgIdJURgitDhujU6qY3Y
KtWJh2Q5fe11dGXw7Kn7UdJRSgRCOjYTV4s5RmpMlTB2cHSvz+y00cQdknVvsowwnOfa/dRn
ta5/iwpp3OgYw21/0HCfblWPbpPIKDGOIR2bgDbNYMNObJXqfEMaPTay2Bo9GloNpURHqXH+
hGzzq52avkm52yIWoN0emc4aX308eKKj5DCzIYC/1wiDfkmrwYctOkoPIQmZOAPbOzbSLWk1
+gs6ShEhiZicyNA9NBLYItFRighJwlxGVteXGzlGoqMkEZJXf/0P1NqM2tFRFgjJo7+3LZHh
hIhV58cHOkoUITkaPzrqnTWyumLK5wlZOkoVITnRzKi2nKD3PkXIuSOuzeULIbnQzqi2fA+L
d0RJnhCSB35uNek+TZXrF/tDSOI83bHV/fCIG8p6REiWRj8u4el9KtVRzUbJC0KyMpKR80Xq
Rgl2REk+EJKNsYy8LVC0I0rygJCk+Dz2kDh9xBbJK0IyFXxrJHUalmMknwjJzPDBkd+RMKnp
DNxQ1iNCMhIhI7lpQdxQ1iNCMjHUke/zMoLT6zgh6w8hufF+elN0mipThLwhJF0DWyN/p42e
hKd705EvhKRnYJAhwFwbrgKZDULSEiUjPn2UEULS8dFRkJmfdJQRQrIQZgI1HeWEkObE2RrR
UWYIadrHIEOoj/PQUV4IaVKsjOgoN4Q0pd9RgNNGD3SUG0LSFfIj2nSUHUIa8e99axRw2XSU
H0IaFDMjOsoRIQ2JmREdZYmQ5oS+fBUdZYmQpgXPiI7yREhvekdHwS+mSEa5IqSebkYBTxs9
0FG2CKmrl1H4xdNRvghpUJQLZNNRxghpQJzrzNNRzgjp7nV0FOl2DXSUNUJqRc+IjjJHSI3o
GdFR7gipI949uOgod4T0EOG00RMdZa/4kO5HR1FvCElH+Ss8pCQyoqMFKDukBDJic7QMZYfU
iHyXbzpahnJDSmFrREeLUWpIt4Oj2BnR0WIUGlKTUczx7js6WowyQ/qXwMaopqMlKTOkJDKi
oyUpL6REtkZ0tCxFhNTp5t+/RDKio2UpIaTOLYiTyYiOFqaAkP7q5zbpXyoZ0dHSLD6kezp/
nccJoKOlWXpIr526dLZGTFNdoIWH9GgnpYzYHC3RskN6dtQ5ToqOjpZo2SF1D43oCB4FDen3
sFWN7f7X1yLe/fVGGxJAR8sUMKTLWr1svCzi09/jM7Bir+iGjhYqYEh7Vf2c2kfnY6X2Phbx
rs2I4yP4FzCkSp2ej0+q8rGIvr+/x9aIjuBZwJCUGvuF2CI6up828tqRwYvT0XItdIsU7qyR
weaOjhYs7DHS8dw+8n2M1GT0dl9yXwwOwOhoyUIOf286o3bri5dFNAJmdG9Ia/tHR4sW9jzS
vj2PVG0P/s4jtW/qQBm9tkWzJTG9buEWNrMh7Iy6v8GHQ8ho6dIJSXXZvUTgial/o794R0eL
FyWk2VCsFnHLKNTRUbvEwYef6Gj5lhLSX/iMat1jJDoqQNATstp7b6aLeOzThc2o1hu1o6MS
BAzpt/IUUszP7M2fR6KjIoTctbts1aY9Iyu6axdta3RfPB2hDn2M9KPUTy0a0jOjSB2xPUIr
8GDDeaO2F7mQnjt10TKaQUelCD5qd1DVUSik17ERHSGy8MPfp/X8CVedRSR0WaAxdFSOGOeR
du4h/aW/NaKjoqQzRchgEZ2NUbxBhjlMUy1KhiF19+mSzYjNUWGyC6l3aERHSERmIWUwwtCi
o9JkFVImWyM6KlBGIfUzoiOkJJuQ+jt1KWdERyXKI6S/t2MjOkJicggplxGGGzoqUvohvW+M
kt4a0VGpUg8ps4zoqFRph/S+U5d6RnRUrJRDyuvYqEFHxUo3pAwzoqNypRrSR0bJHx2xOSpa
miFlmBEdlS3NkN4XkX5GdFS4PEJKHx0VjpBE0FHpkg8pg6MjOkLqIWWRER0h8ZCyyIiOkHpI
WaAjEJI7OkKdcEh5HB3REW4SDSmbjOgIrTRDyiQjNkd4SDOkTI6R6AgPhGSPjvBESNboCC+E
ZGHV/EBH6CAkc6umJDpCFyEZa7ZHKzpCDyGZuu3XrWKvBtJCSIbux0eEhB5CMvMcZ6AkdBGS
kc54HSWhg5BM9Ma9KQkvhGRk9ZqmSkfoICQzz2FvOkIXIRn5qle3gugIPYRkot0erWo6wjtC
MnDfr1vREd4Rkj6OjzCKkLQxvQ7jCEkXHWECIWmiI0whJD10hEmEpIWOMI2QdNARZhDSPK4C
iVmENIuMMI+Q5tARNBDSDDqCDkIac5sHREfQQkgjbjNT6Qh6CGnY7bMSdARNhDSI/TqYIaRB
XL0OZghpCFevgyFCGsDV62CKkD5x9ToYI6QBKzqCIUIawlUgYYiQBjyG61Z0BE2E9OkxXEdG
0EZIHx7DdXQEfYT0jsMjWCCkN0wLgg1C6qMjWCGkHjqCHULqoiNYIqQOOoItQnqhI1gjpCc6
gj1CuuMqkHBBSDdkBCeE1KIjuCGkBh3BESHVdAR3hERHEEBIdAQBhERHEFB8SHQECaWHREcQ
UXhIdAQZZYdERxBSdEh0BCkFh8Q01TKoMCxWTP7vGmERbI5KEWb3ptiQ6KgUhOQTHRWDkDyi
o3IQkj90VBBC8oaOSkJIvtBRUQjJEzoqCyH5QUeFWWBIv4dtexJ4u//1tYhZdFSaxYV0WXcm
VGy8LGIeHRVncV0gmQkAAAqUSURBVCHtVfVzah+dj5Xa+1jEHKbXFWhxIVXq9Hx8UpWPRcwg
oxItLqTeBNnp2bJ+/u50VKTFhRR7i0RHZVpcSNdjpOO5fRTlGImOCrW4kOpNZ9RuffGyiHF0
VKrlhVT/7tvzSNX2EPw8Eh0Va4EhxVsEHZWrtJAcPwA/iY4KJv9+rQaGyiKE9F2p9bffRbyh
o5KJh3S8/kt/FFiK9Yqdtqr6rg/BpwjRUdHEQ9qpvdoJLMV2xU5tQdd1uNTnrZrcJon+3emo
bOIhXXfsqo8XDRjSrjl3tL/tXl7U2scihtBR4aRD+rm+j/fqx30pblOE1LbzC+lFfGKaavGk
Q9qo3/r349gkeEg/t326QFOEyAgDbyaXq6de2rdupd5mFATdtds9Fn7ZhZkiREeQ3iL9tG/d
j327kB/sq56Jq+kNktTfnY4gHtJaNdNyTu8H+UHPI+0f+VST2yOpvzsdoZYO6fzc7zu7LiWX
KUJ0hIbs+/XwDOngupRMQqIjtGTfr+v7luj8tm+32JDoCDei79fT/fRNMwp+6v6PpYZER7gT
fb/un7Psjv2B54WGREd4EH2/VtXQQ7ulZBASHeGptM8jCS6CjvBCSLboCB2ENGA1/1ymqaKH
kD6t5ksiI/QR0odVPbtNoiO8IaR3t4ZWUynREd4R0pvVx4MPdIQPhNS3GnzYQ0f4REg9q9Ff
PNERBhBS3+wWiY4whJDezBwj0REGCb9f77dufb96fUYhPQKiI5jwEpLqf4gix5DoCEbEQ2p+
3L9fjyunkCZOyNIRxngJ6ePCjFmFNDZFiOl1GOcppLfrYOUV0khH/lYE+fO0a/d28frMQhpC
R5gy8Gb60zT4cjfvF5TLPyQ6wiQ/o3abjEftBtERpnnZtTtWqn8mKfeQ6Agz/Aw2nN7GvzMP
iY4wx09I7+PfeYdER5jlJ6TL2/h31iHREeZ5CemyeRu3yzkkOoIGT3Ptqv6dxjIOiY6gw0tI
1T7eHfuEF0FH0MLnkSbREfQQ0gSmqUIXIY0jI2gjpFF0BH2ENIaOYICQRtARTBDSMDqCEUIa
REcwQ0hD6AiGCGkAHcGU+Pv1tKvU7vj2m3mFREcwJv1+3d9m263PrkuJFxIdwZzw+/WgquvW
6HL9qVdSTiFZd6Rx51ksluz79fwIaKd2jkuJFJL99DqNO89iuWTfr3t1uD24bHtXtssmJPvd
Oo07z2LBZN+vm/er59svJUpI9pujqUvvowBD/yprGnq1kbd/JiG5Hx5RUqlk3695hyQxzEBJ
hSKkJ5nhOkoqk+z7dfs8Rjr2rtqQQ0gOp4/YIkH2/Xp4jNr9qrXjUkKH5HQalmOk4nk6j7RR
mQ1/O05nmLzxLAog/H7dtTMbztvcrrTqPC2I4e/CSb9fN1nOtROYXscJ2bKJv19/tkptftyX
EjIkkWmqTBEqGp9HEpvuTUclIySuAgkBxYdERpBQekh0BBGFh0RHkFF2SHQEIUWHREeQUnJI
dAQxJYcU5u+OIhASIICQAAGEBAggJEAAIQECCAkQQEiAgKJDAjJj8S6XD8dSEmvCSjwlsRZJ
rISWdNY0iTVhJZ6SWIskVkJLOmuaxJqwEk9JrEUSK6ElnTVNYk1Yiack1iKJldCSzpomsSas
xFMSa5HESmhJZ02TWBNW4imJtUhiJbSks6ZJrAkr8ZTEWiSxElrSWdMk1oSVeEpiLZJYCS3p
rGkSa8JKPCWxFkmshJZ01jSJNWElnpJYiyRWQks6a5rEmrAST0msRRIroSWdNU1iTViJpyTW
IomV0JLPmgIJIyRAACEBAggJEEBIgABCAgQQEiCAkAABhAQIICRAACEBAggJEEBIgABCAgQQ
EiCAkAAB8UP6Xqtqf2kf7qvnw7AuO6V2pzruSjR+VeyV6F5FPt5anJpvyDnyShiJHtK+/b5V
zVdq0z5cR1iJql1yW1K8lbi6VLfvR7yVOHVCircWxxTeFGZih3RSu+uX61vtmn+Nq1N9qtRv
8JXYN4vfq20dcyUa29s7OOJKnNqvQh15Larrki9btY/9/TAQO6TtbQWaN9BeHa+PftQh+EpU
6nJfh4gr0S72FlLElfh+LTTeWvw0CdUXVUX+fpiIHdJd8wbaqmanuPNPYuh1uH7foq7EWW1u
IUVciW/1/XgYby126hR/JQylEdJFbe5bhOdPwe3bt1DMldio8225EVdiq46768F93LVYq/pQ
tfv8sd8U+tJYwe9mAx71a3bdq4r87qkP6qdOIKTWJupaKNWuRhV1JQwlsYLnqtlyR/2afW+r
dj883kq0uy/RQ1LXmutLu3WOGVIz2LBrviGEZOBSNf8ARv+a7eK+e9bNaG/0kG4uzXhzzJCa
Y6Rz3JUwlMIKbm5nCarIX7N2lCjaSuza4anbcmN/JW6LjrcWnXrifyk0xV/B83pzO4V9G6A5
xxugeQ0dRliJ7q3po38l4n4puudE4n8pNEUP6dge2DYO7b/Jx9tBf1C380jtrkS0leiGFO8r
8fxSbGOuxW3J5+adEfFLYSZ2SOdnR7FnNly2zTFS5DPp0Wc27Ju37KU9DRpvLa7/pF2awYaf
6N8PfbFD2r3+Ha7Xz5HX0KrXkuOtRON+LBBvJS63L8U+7locUvl+6IsdUmeH5voPYXU/Fxjc
dcnr2yn9iCtRP0OKuBKXJL4Ux81jyXG/H/pihwQsAiEBAggJEEBIgABCAgQQEiCAkAABhAQI
ICRAACEBAggJEEBIgABCAgQQEiCAkAABhAQIICRAACEBAggJEEBIgABCAgQQEiCAkAABhAQI
ICRAACEBAggJEEBIgABCAgQQEiCAkAABhAQIIKTs8S1MAd+F9B2Hf7u9u99519zQ7hJ0fTCA
kJK3HvkeNSGdbvcNrcKuET4RUvLUREgbtb+oy0ZlcJPVhSOk5E2F1P5XX9gkRUdISTlu1f0e
3kqdt6o63O/7/vbH9tV1G9T8bqUuz2/h67mdP1DX32tVfYda/3IRUkoOt0OepoZrFM3Dw1BI
m+a3ts3v7tX6qD6ee/sDu/Zp2/Z3N2H/HgUipJQo9VPXP20A1zf/pf5W64Fdux9VnepT1f7+
rinm9+25x9cfODYvcz2IGhn5gxRCSs89pN/6dRzUs23/1/H2+6d9s3XqP3fbdtP+ga1qhsYv
nT8BLwgpLefjYXMPqa5HQrr/xuP31XGtvgeee3/yXZC1Lxhf4KRsnu96g5CuG5z1wHMJKSS+
wCnZqfX38WwcUvvw47nDT4YffJ1Tcpv1MxfS7RDo9zX83Z5H6jy3d4zEMEMQhJSSZoTh9HmM
dO7/qc6g3E5tHzMbOs/t/IF2hK/+ZrDBN0JKyf5+QPPbDWn9MZdu+zxNdKmec+06z30cLqnn
w+r8sSyIIqSkXOvY/B6b7ccrpN/1xwygw3Piwnn/nP39em47s2Hz+5zZoHZ05BshZW/0W8h8
hoAIKXuf38J2ksNly5zwgAgpD0oZnBE68Cml4AgpD0Yh1d8bpdZsj0IiJEAAIQECCAkQQEiA
AEICBBASIICQAAGEBAggJEAAIQECCAkQQEiAAEICBBASIICQAAGEBAggJEAAIQECCAkQQEiA
AEICBBASIICQAAGEBAggJEAAIQECCAkQ8B+JRnpVjJZqCQAAAABJRU5ErkJggg=="
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here we plot models for three different groups. And one plot for the average model.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1">####################Aufgabe 2 ########################</span>
Wage_c <span class="o">&lt;-</span> Wage<span class="p">[</span><span class="kp">colnames</span><span class="p">(</span>Wage<span class="p">)[</span><span class="o">!</span><span class="p">(</span><span class="kp">colnames</span><span class="p">(</span>Wage<span class="p">)</span> <span class="o">%in%</span> <span class="kt">c</span><span class="p">(</span><span class="s">&quot;logwage&quot;</span><span class="p">,</span> <span class="s">&quot;region&quot;</span><span class="p">))]]</span>
<span class="kp">set.seed</span><span class="p">(</span><span class="m">100</span><span class="p">)</span>
train_ind <span class="o">&lt;-</span> <span class="kp">sample</span><span class="p">(</span><span class="m">1</span><span class="o">:</span><span class="kp">nrow</span><span class="p">(</span>Wage_c<span class="p">),</span> <span class="kp">round</span><span class="p">(</span><span class="m">0.7</span><span class="o">*</span><span class="kp">nrow</span><span class="p">(</span>Wage_c<span class="p">)))</span> 
Wage_train <span class="o">&lt;-</span> Wage_c<span class="p">[</span>train_ind<span class="p">,]</span> 
Wage_test <span class="o">&lt;-</span> Wage_c<span class="p">[</span><span class="o">-</span>train_ind<span class="p">,]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[55]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>pr1<span class="o">=</span>lm<span class="p">(</span>wage <span class="o">~</span> year<span class="o">+</span>age<span class="o">+</span>maritl<span class="o">+</span>race<span class="o">+</span>education<span class="o">+</span>jobclass<span class="o">+</span>health<span class="o">+</span>health_ins<span class="p">,</span> data<span class="o">=</span>Wage_train<span class="p">)</span> <span class="c1"># This is our OLS model.</span>
<span class="kp">summary</span><span class="p">(</span>pr1<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = wage ~ year + age + maritl + race + education + 
    jobclass + health + health_ins, data = Wage_train)

Residuals:
   Min     1Q Median     3Q    Max 
-96.12 -18.53  -3.30  12.98 212.21 

Coefficients:
              Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) -2.397e+03  7.327e+02  -3.271  0.00109 ** 
year         1.236e+00  3.653e-01   3.383  0.00073 ***
age          3.683e-01  7.285e-02   5.056 4.66e-07 ***
maritl1     -6.581e+00  2.644e+00  -2.489  0.01290 *  
maritl2      1.082e+01  2.322e+00   4.657 3.41e-06 ***
maritl3     -6.211e+00  7.307e+00  -0.850  0.39538    
maritl4     -1.457e+00  3.105e+00  -0.469  0.63893    
race1        4.920e+00  2.027e+00   2.427  0.01529 *  
race2       -2.536e+00  2.598e+00  -0.976  0.32916    
race3        2.359e+00  2.898e+00   0.814  0.41580    
education1  -2.256e+01  2.109e+00 -10.699  &lt; 2e-16 ***
education2  -1.498e+01  1.324e+00 -11.314  &lt; 2e-16 ***
education3  -4.006e+00  1.489e+00  -2.691  0.00717 ** 
education4   1.037e+01  1.446e+00   7.175 9.99e-13 ***
jobclass1   -1.592e+00  7.814e-01  -2.037  0.04178 *  
health1     -4.452e+00  8.444e-01  -5.272 1.49e-07 ***
health_ins1  7.896e+00  8.195e-01   9.636  &lt; 2e-16 ***
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 33.52 on 2083 degrees of freedom
Multiple R-squared:  0.359,	Adjusted R-squared:  0.3541 
F-statistic: 72.91 on 16 and 2083 DF,  p-value: &lt; 2.2e-16
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>At first we train our model. In this case we get OLS. Then we will compare different models with different transformation
in OLS and another methods.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[39]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>plot<span class="p">(</span>Wage_train<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
Ql8c6gAAAABJRU5ErkJggg=="
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We have to give attention to the predictors with some correlation. Because we can include them in the model as interaction terms</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[53]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>pr2<span class="o">=</span>lm<span class="p">(</span>wage <span class="o">~</span> year<span class="o">*</span>age<span class="o">+</span>maritl<span class="o">+</span>race<span class="o">*</span>age<span class="o">+</span>education<span class="o">*</span>age<span class="o">+</span>jobclass<span class="o">+</span>health<span class="o">+</span>health_ins<span class="p">,</span> data<span class="o">=</span>Wage_train<span class="p">)</span> 
<span class="kp">summary</span><span class="p">(</span>pr2<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = wage ~ year * age + maritl + race * age + education * 
    age + jobclass + health + health_ins, data = Wage_train)

Residuals:
     Min       1Q   Median       3Q      Max 
-100.106  -18.378   -3.285   12.994  210.709 

Coefficients:
                 Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)    -4.863e+03  2.734e+03  -1.779   0.0754 .  
year            2.464e+00  1.363e+00   1.808   0.0707 .  
age             5.600e+01  6.150e+01   0.911   0.3626    
maritl1        -6.666e+00  2.648e+00  -2.518   0.0119 *  
maritl2         1.097e+01  2.333e+00   4.700 2.77e-06 ***
maritl3        -6.461e+00  7.344e+00  -0.880   0.3790    
maritl4        -1.889e+00  3.110e+00  -0.607   0.5436    
race1           5.266e+00  6.977e+00   0.755   0.4505    
race2           4.006e+00  8.961e+00   0.447   0.6549    
race3           1.166e+01  1.048e+01   1.112   0.2661    
education1     -6.523e+00  7.144e+00  -0.913   0.3613    
education2     -5.265e+00  4.831e+00  -1.090   0.2759    
education3     -1.364e+01  5.476e+00  -2.490   0.0128 *  
education4      1.317e+01  5.621e+00   2.343   0.0192 *  
jobclass1      -1.632e+00  7.813e-01  -2.089   0.0369 *  
health1        -4.356e+00  8.437e-01  -5.163 2.66e-07 ***
health_ins1     8.111e+00  8.238e-01   9.846  &lt; 2e-16 ***
year:age       -2.770e-02  3.066e-02  -0.903   0.3664    
age:race1      -2.674e-02  1.732e-01  -0.154   0.8773    
age:race2      -1.570e-01  2.095e-01  -0.750   0.4535    
age:race3      -2.312e-01  2.509e-01  -0.922   0.3569    
age:education1 -3.770e-01  1.645e-01  -2.292   0.0220 *  
age:education2 -2.220e-01  1.089e-01  -2.038   0.0417 *  
age:education3  2.424e-01  1.272e-01   1.906   0.0568 .  
age:education4 -6.085e-02  1.268e-01  -0.480   0.6312    
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 33.44 on 2075 degrees of freedom
Multiple R-squared:  0.3644,	Adjusted R-squared:  0.3571 
F-statistic: 49.57 on 24 and 2075 DF,  p-value: &lt; 2.2e-16
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here i tried to trnasform variables with including of interaction terms. I choosed variables with the biggest correlation.
But it didn't improve our model so well. We could also do some Polynomial or log distribution but as we see below it doesn't make so much sense because our data doesn't show any non-linearities.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[56]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>layout<span class="p">(</span><span class="kt">matrix</span><span class="p">(</span><span class="kt">c</span><span class="p">(</span><span class="m">1</span><span class="p">,</span><span class="m">2</span><span class="p">,</span><span class="m">3</span><span class="p">,</span><span class="m">4</span><span class="p">),</span><span class="m">2</span><span class="p">,</span><span class="m">2</span><span class="p">))</span> 
plot<span class="p">(</span>pr1<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
gg=="
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As we can conclude from this plots there are no non-linearities.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[60]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>pd_pr1 <span class="o">=</span> predict<span class="p">(</span>pr1<span class="p">,</span> newdata<span class="o">=</span>Wage_test<span class="p">)</span> <span class="c1"># Here we get fitted values.</span>
rss_ols <span class="o">=</span> <span class="kp">mean</span><span class="p">((</span>Wage_test<span class="p">[,</span><span class="s">&quot;wage&quot;</span><span class="p">]</span><span class="o">-</span>pd_pr1<span class="p">)</span><span class="o">^</span><span class="p">(</span><span class="m">2</span><span class="p">))</span> <span class="c1"># Here we get our Av. RSS for OLS.</span>
rss_ols
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
1244.23861249978
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here we compute average RSS for different methods and compare them. As we showed above it doesn't make so much sense to transform something or add some interactions we will use just our classic models with predictors.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[67]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1"># For the regression Tree.</span>

<span class="kp">set.seed</span><span class="p">(</span><span class="m">100</span><span class="p">)</span>
rg_tree <span class="o">=</span> rpart<span class="p">(</span>wage <span class="o">~</span> <span class="m">.</span><span class="p">,</span>Wage_train<span class="p">,</span> cp <span class="o">=</span> <span class="m">0.0001</span><span class="p">)</span>
printcp<span class="p">(</span>rg_tree<span class="p">)</span>
regression_trees_pred <span class="o">&lt;-</span> predict<span class="p">(</span>rg_tree<span class="p">,</span> Wage_test<span class="p">)</span>
rss_reg_tree <span class="o">&lt;-</span> <span class="kp">mean</span><span class="p">((</span>Wage_test<span class="o">$</span>wage <span class="o">-</span> regression_trees_pred<span class="p">)</span><span class="o">^</span><span class="p">(</span><span class="m">2</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>
Regression tree:
rpart(formula = wage ~ ., data = Wage_train, cp = 1e-04)

Variables actually used in tree construction:
[1] age        education  health     health_ins jobclass   maritl     race      
[8] year      

Root node error: 3651382/2100 = 1738.8

n= 2100 

            CP nsplit rel error  xerror     xstd
1   0.19381157      0   1.00000 1.00036 0.056314
2   0.03370416      1   0.80619 0.80702 0.047707
3   0.03067754      2   0.77248 0.79504 0.047004
4   0.02520473      3   0.74181 0.75773 0.046298
5   0.01196640      4   0.71660 0.73614 0.045176
6   0.01138937      5   0.70464 0.72493 0.044394
7   0.01054834      6   0.69325 0.71668 0.043994
8   0.00988937      7   0.68270 0.70844 0.043530
9   0.00672986      8   0.67281 0.69165 0.042369
10  0.00641096      9   0.66608 0.70835 0.043516
11  0.00616113     10   0.65967 0.70803 0.043567
12  0.00613904     11   0.65351 0.70706 0.043240
13  0.00542195     12   0.64737 0.70479 0.043237
14  0.00444838     13   0.64195 0.70821 0.043181
15  0.00398366     15   0.63305 0.70483 0.042708
16  0.00318517     18   0.62110 0.70918 0.042615
17  0.00301145     19   0.61791 0.71409 0.042981
18  0.00294012     20   0.61490 0.71549 0.043004
19  0.00282265     21   0.61196 0.71466 0.042964
20  0.00280584     22   0.60914 0.71492 0.042927
21  0.00280182     23   0.60633 0.71533 0.043011
22  0.00257733     24   0.60353 0.71566 0.043587
23  0.00252145     26   0.59838 0.71335 0.043264
24  0.00208332     27   0.59585 0.71169 0.043089
25  0.00208298     28   0.59377 0.71172 0.042803
26  0.00201661     31   0.58752 0.71254 0.042840
27  0.00200318     32   0.58551 0.71167 0.042754
28  0.00196545     33   0.58350 0.71302 0.042808
29  0.00194012     34   0.58154 0.71464 0.042830
30  0.00193088     35   0.57960 0.71420 0.042831
31  0.00177856     36   0.57767 0.71325 0.042700
32  0.00175343     39   0.57233 0.71283 0.042472
33  0.00174754     40   0.57058 0.71321 0.042457
34  0.00174337     42   0.56708 0.71321 0.042457
35  0.00155719     43   0.56534 0.71457 0.042542
36  0.00150007     44   0.56378 0.71186 0.042321
37  0.00142720     45   0.56228 0.71552 0.042511
38  0.00127835     46   0.56085 0.71719 0.042788
39  0.00124639     47   0.55958 0.71827 0.042776
40  0.00109863     51   0.55451 0.72146 0.042853
41  0.00107530     52   0.55341 0.72224 0.043138
42  0.00106223     55   0.55019 0.72295 0.043258
43  0.00105951     57   0.54806 0.72341 0.043320
44  0.00101140     61   0.54383 0.72163 0.043242
45  0.00099642     62   0.54281 0.72024 0.042928
46  0.00092972     63   0.54182 0.72219 0.042978
47  0.00087672     64   0.54089 0.72461 0.042791
48  0.00085559     65   0.54001 0.72519 0.042846
49  0.00083731     66   0.53916 0.72503 0.043003
50  0.00083558     67   0.53832 0.72610 0.043006
51  0.00082468     69   0.53665 0.72819 0.043572
52  0.00080748     71   0.53500 0.72961 0.043610
53  0.00078445     75   0.53177 0.73051 0.043613
54  0.00076312     76   0.53098 0.73107 0.043500
55  0.00074276     77   0.53022 0.73130 0.043489
56  0.00074179     78   0.52948 0.73149 0.043457
57  0.00074147     80   0.52799 0.73149 0.043457
58  0.00073994     82   0.52651 0.73149 0.043457
59  0.00073859     83   0.52577 0.73149 0.043457
60  0.00072296     85   0.52429 0.73147 0.043410
61  0.00072131     86   0.52357 0.73088 0.043401
62  0.00068136     87   0.52285 0.73083 0.043331
63  0.00064977     89   0.52149 0.73130 0.043367
64  0.00063918     90   0.52084 0.73236 0.043370
65  0.00063039     91   0.52020 0.73327 0.043398
66  0.00058456     95   0.51768 0.73456 0.043469
67  0.00058054     96   0.51709 0.73671 0.043548
68  0.00054523     97   0.51651 0.73596 0.043547
69  0.00054403     98   0.51597 0.73606 0.043524
70  0.00053333     99   0.51542 0.73579 0.043526
71  0.00048176    100   0.51489 0.73600 0.043511
72  0.00047026    102   0.51393 0.73667 0.043508
73  0.00045510    104   0.51299 0.73814 0.043489
74  0.00043915    105   0.51253 0.73933 0.043492
75  0.00043408    106   0.51209 0.74041 0.043598
76  0.00042326    107   0.51166 0.74102 0.043606
77  0.00042008    108   0.51123 0.74083 0.043605
78  0.00041963    110   0.51039 0.74068 0.043603
79  0.00040423    112   0.50955 0.74113 0.043607
80  0.00037557    113   0.50915 0.74136 0.043609
81  0.00037384    114   0.50877 0.74156 0.043566
82  0.00035636    115   0.50840 0.74196 0.043562
83  0.00035153    118   0.50733 0.74298 0.043634
84  0.00034988    119   0.50698 0.74263 0.043556
85  0.00034281    120   0.50663 0.74263 0.043505
86  0.00032487    121   0.50629 0.74223 0.043457
87  0.00032477    122   0.50596 0.74185 0.043462
88  0.00032055    123   0.50564 0.74195 0.043461
89  0.00032030    124   0.50532 0.74164 0.043457
90  0.00031707    127   0.50436 0.74171 0.043457
91  0.00030662    128   0.50404 0.74284 0.043497
92  0.00029932    130   0.50343 0.74295 0.043497
93  0.00028520    131   0.50313 0.74291 0.043495
94  0.00027933    133   0.50256 0.74313 0.043498
95  0.00027687    135   0.50200 0.74325 0.043498
96  0.00027125    136   0.50172 0.74342 0.043498
97  0.00026763    137   0.50145 0.74353 0.043499
98  0.00026715    138   0.50118 0.74334 0.043497
99  0.00025321    140   0.50065 0.74374 0.043691
100 0.00023762    141   0.50039 0.74329 0.043653
101 0.00021147    142   0.50016 0.74375 0.043696
102 0.00020956    143   0.49995 0.74362 0.043626
103 0.00020311    145   0.49953 0.74388 0.043629
104 0.00019686    146   0.49932 0.74360 0.043604
105 0.00018839    147   0.49913 0.74328 0.043502
106 0.00018108    149   0.49875 0.74397 0.043502
107 0.00017827    151   0.49839 0.74431 0.043503
108 0.00017124    153   0.49803 0.74427 0.043504
109 0.00016543    154   0.49786 0.74395 0.043487
110 0.00015716    155   0.49769 0.74416 0.043485
111 0.00015493    156   0.49754 0.74475 0.043491
112 0.00015433    158   0.49723 0.74475 0.043492
113 0.00014058    159   0.49707 0.74461 0.043492
114 0.00013793    160   0.49693 0.74507 0.043497
115 0.00013493    161   0.49679 0.74468 0.043487
116 0.00012945    162   0.49666 0.74426 0.043456
117 0.00012652    163   0.49653 0.74432 0.043457
118 0.00012552    164   0.49640 0.74424 0.043457
119 0.00011952    165   0.49628 0.74411 0.043463
120 0.00011244    166   0.49616 0.74412 0.043463
121 0.00010196    167   0.49605 0.74422 0.043462
122 0.00010000    168   0.49594 0.74430 0.043462
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[68]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>plotcp<span class="p">(</span>rg_tree<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>How we see from the table and the graph that it makes sense to take  0.00208298 cp. Because as our cp decreases after this cp our xerror increases.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[71]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">set.seed</span><span class="p">(</span><span class="m">100</span><span class="p">)</span>
rg_tree <span class="o">=</span> rpart<span class="p">(</span>wage <span class="o">~</span> <span class="m">.</span><span class="p">,</span>Wage_train<span class="p">,</span> cp <span class="o">=</span> <span class="m">0.00208298</span><span class="p">)</span>
regression_trees_pred <span class="o">&lt;-</span> predict<span class="p">(</span>rg_tree<span class="p">,</span> Wage_test<span class="p">)</span>
rss_reg_tree <span class="o">&lt;-</span> <span class="kp">mean</span><span class="p">((</span>Wage_test<span class="o">$</span>wage <span class="o">-</span> regression_trees_pred<span class="p">)</span><span class="o">^</span><span class="p">(</span><span class="m">2</span><span class="p">))</span>
rss_reg_tree
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
1328.16261410069
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This is our average RSS for the Regression Tree.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[72]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1">### Random Forest.</span>
rnd_forest_md <span class="o">=</span> randomForest<span class="p">(</span>wage<span class="o">~</span> <span class="m">.</span><span class="p">,</span> Wage_train<span class="p">,</span> ntree<span class="o">=</span><span class="m">50</span><span class="p">,</span> norm.votes<span class="o">=</span><span class="kc">FALSE</span><span class="p">)</span>
prd_ranfor <span class="o">=</span> predict<span class="p">(</span>rnd_forest_md<span class="p">,</span> Wage_test<span class="p">)</span>
<span class="kp">mean</span><span class="p">((</span>Wage_test<span class="o">$</span>wage<span class="o">-</span>prd_ranfor<span class="p">)</span><span class="o">^</span><span class="p">(</span><span class="m">2</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
1253.4966565669
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As we know that in Random Forest the more trees we do the better model we get. Now we will try different numbers of trees to check whether it makes a big difference to make number of tree real big.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[74]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>rnd_forest_md <span class="o">=</span> randomForest<span class="p">(</span>wage<span class="o">~</span> <span class="m">.</span><span class="p">,</span> Wage_train<span class="p">,</span> ntree<span class="o">=</span><span class="m">100</span><span class="p">,</span> norm.votes<span class="o">=</span><span class="kc">FALSE</span><span class="p">)</span>
prd_ranfor <span class="o">=</span> predict<span class="p">(</span>rnd_forest_md<span class="p">,</span> Wage_test<span class="p">)</span>
<span class="kp">mean</span><span class="p">((</span>Wage_test<span class="o">$</span>wage<span class="o">-</span>prd_ranfor<span class="p">)</span><span class="o">^</span><span class="p">(</span><span class="m">2</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
1246.05387203512
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[75]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>rnd_forest_md <span class="o">=</span> randomForest<span class="p">(</span>wage<span class="o">~</span> <span class="m">.</span><span class="p">,</span> Wage_train<span class="p">,</span> ntree<span class="o">=</span><span class="m">3000</span><span class="p">,</span> norm.votes<span class="o">=</span><span class="kc">FALSE</span><span class="p">)</span>
prd_ranfor <span class="o">=</span> predict<span class="p">(</span>rnd_forest_md<span class="p">,</span> Wage_test<span class="p">)</span>
<span class="kp">mean</span><span class="p">((</span>Wage_test<span class="o">$</span>wage<span class="o">-</span>prd_ranfor<span class="p">)</span><span class="o">^</span><span class="p">(</span><span class="m">2</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
1239.65822298803
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As we see that influence of the number of the trees for our average RSS is not so big. We needed 3000 Trees to get our average less than 
OLS. Therefore i think that some average number of trees  for our model would be enough.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">

<pre><code>                      ############################Aufgabe 3 ##################################</code></pre>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[175]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>r_est <span class="o">=</span> read.table<span class="p">(</span><span class="s">&quot;realestate.txt&quot;</span><span class="p">,</span> header<span class="o">=</span><span class="kc">TRUE</span><span class="p">)</span> <span class="c1"># Real Estate</span>
r_est
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th scope=col>SalesPrice</th><th scope=col>SqFeet</th><th scope=col>Beds</th><th scope=col>Baths</th><th scope=col>AirCond</th><th scope=col>Garage</th><th scope=col>Pool</th><th scope=col>Year</th><th scope=col>Quality</th><th scope=col>Style</th><th scope=col>Lot</th><th scope=col>Highway</th></tr></thead>
<tbody>
	<tr><td>360.00</td><td>3.032 </td><td>4     </td><td>4     </td><td>1     </td><td>2     </td><td>0     </td><td>1972  </td><td>2     </td><td>1     </td><td>22.221</td><td>0     </td></tr>
	<tr><td>340.00</td><td>2.058 </td><td>4     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1976  </td><td>2     </td><td>1     </td><td>22.912</td><td>0     </td></tr>
	<tr><td>250.00</td><td>1.780 </td><td>4     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1980  </td><td>2     </td><td>1     </td><td>21.345</td><td>0     </td></tr>
	<tr><td>205.50</td><td>1.638 </td><td>4     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1963  </td><td>2     </td><td>1     </td><td>17.342</td><td>0     </td></tr>
	<tr><td>275.50</td><td>2.196 </td><td>4     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1968  </td><td>2     </td><td>7     </td><td>21.786</td><td>0     </td></tr>
	<tr><td>248.00</td><td>1.966 </td><td>4     </td><td>3     </td><td>1     </td><td>5     </td><td>1     </td><td>1972  </td><td>2     </td><td>1     </td><td>18.902</td><td>0     </td></tr>
	<tr><td>229.90</td><td>2.216 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1972  </td><td>2     </td><td>7     </td><td>18.639</td><td>0     </td></tr>
	<tr><td>150.00</td><td>1.597 </td><td>2     </td><td>1     </td><td>1     </td><td>1     </td><td>0     </td><td>1955  </td><td>2     </td><td>1     </td><td>22.112</td><td>0     </td></tr>
	<tr><td>195.00</td><td>1.622 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1975  </td><td>3     </td><td>1     </td><td>14.321</td><td>0     </td></tr>
	<tr><td>160.00</td><td>1.976 </td><td>3     </td><td>3     </td><td>0     </td><td>1     </td><td>0     </td><td>1918  </td><td>3     </td><td>1     </td><td>32.358</td><td>0     </td></tr>
	<tr><td>190.00</td><td>2.812 </td><td>7     </td><td>5     </td><td>0     </td><td>2     </td><td>1     </td><td>1966  </td><td>3     </td><td>7     </td><td>56.639</td><td>0     </td></tr>
	<tr><td>559.00</td><td>2.791 </td><td>3     </td><td>4     </td><td>1     </td><td>3     </td><td>0     </td><td>1992  </td><td>1     </td><td>1     </td><td>30.595</td><td>0     </td></tr>
	<tr><td>535.00</td><td>3.381 </td><td>5     </td><td>4     </td><td>1     </td><td>3     </td><td>0     </td><td>1988  </td><td>1     </td><td>7     </td><td>23.172</td><td>0     </td></tr>
	<tr><td>525.00</td><td>3.459 </td><td>5     </td><td>4     </td><td>1     </td><td>2     </td><td>0     </td><td>1978  </td><td>1     </td><td>5     </td><td>35.351</td><td>0     </td></tr>
	<tr><td>299.90</td><td>2.090 </td><td>3     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1987  </td><td>2     </td><td>1     </td><td>24.025</td><td>0     </td></tr>
	<tr><td>527.00</td><td>3.232 </td><td>5     </td><td>5     </td><td>1     </td><td>2     </td><td>0     </td><td>1984  </td><td>2     </td><td>6     </td><td>21.445</td><td>0     </td></tr>
	<tr><td>169.90</td><td>1.502 </td><td>2     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1956  </td><td>2     </td><td>1     </td><td>28.958</td><td>0     </td></tr>
	<tr><td>335.25</td><td>2.747 </td><td>3     </td><td>4     </td><td>1     </td><td>2     </td><td>0     </td><td>1993  </td><td>2     </td><td>7     </td><td>22.241</td><td>0     </td></tr>
	<tr><td>323.90</td><td>2.890 </td><td>4     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1954  </td><td>2     </td><td>7     </td><td>41.992</td><td>0     </td></tr>
	<tr><td>200.00</td><td>1.825 </td><td>3     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1957  </td><td>2     </td><td>1     </td><td>30.266</td><td>0     </td></tr>
	<tr><td>211.00</td><td>1.578 </td><td>4     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1986  </td><td>2     </td><td>2     </td><td>18.829</td><td>0     </td></tr>
	<tr><td>212.00</td><td>1.763 </td><td>3     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1959  </td><td>2     </td><td>1     </td><td>24.726</td><td>0     </td></tr>
	<tr><td>245.00</td><td>2.517 </td><td>4     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1965  </td><td>2     </td><td>1     </td><td>23.261</td><td>0     </td></tr>
	<tr><td>140.40</td><td>1.872 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1985  </td><td>2     </td><td>3     </td><td>24.017</td><td>0     </td></tr>
	<tr><td>295.00</td><td>3.266 </td><td>3     </td><td>3     </td><td>1     </td><td>2     </td><td>0     </td><td>1908  </td><td>2     </td><td>6     </td><td>24.881</td><td>0     </td></tr>
	<tr><td>170.90</td><td>2.020 </td><td>1     </td><td>2     </td><td>1     </td><td>1     </td><td>0     </td><td>1956  </td><td>2     </td><td>1     </td><td>21.385</td><td>0     </td></tr>
	<tr><td>229.00</td><td>2.164 </td><td>4     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1965  </td><td>2     </td><td>1     </td><td>28.291</td><td>0     </td></tr>
	<tr><td>218.50</td><td>2.080 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>1     </td><td>1959  </td><td>2     </td><td>1     </td><td>14.752</td><td>0     </td></tr>
	<tr><td>160.00</td><td>2.208 </td><td>2     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1985  </td><td>2     </td><td>7     </td><td> 8.058</td><td>0     </td></tr>
	<tr><td>259.00</td><td>3.048 </td><td>6     </td><td>4     </td><td>1     </td><td>3     </td><td>0     </td><td>1960  </td><td>2     </td><td>7     </td><td>29.307</td><td>0     </td></tr>
	<tr><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td></tr>
	<tr><td>175.00</td><td>2.035 </td><td>4     </td><td>2     </td><td>1     </td><td>3     </td><td>0     </td><td>1962  </td><td>3     </td><td>7     </td><td>20.131</td><td>0     </td></tr>
	<tr><td>147.00</td><td>1.534 </td><td>3     </td><td>2     </td><td>0     </td><td>1     </td><td>0     </td><td>1955  </td><td>3     </td><td>3     </td><td>15.361</td><td>0     </td></tr>
	<tr><td>155.00</td><td>1.624 </td><td>2     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1955  </td><td>3     </td><td>1     </td><td>16.721</td><td>0     </td></tr>
	<tr><td>150.00</td><td>1.700 </td><td>4     </td><td>2     </td><td>1     </td><td>1     </td><td>0     </td><td>1954  </td><td>3     </td><td>1     </td><td>15.391</td><td>0     </td></tr>
	<tr><td>165.00</td><td>1.630 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1978  </td><td>3     </td><td>2     </td><td>24.963</td><td>0     </td></tr>
	<tr><td>147.00</td><td>1.526 </td><td>3     </td><td>2     </td><td>1     </td><td>1     </td><td>0     </td><td>1957  </td><td>3     </td><td>1     </td><td>15.007</td><td>0     </td></tr>
	<tr><td>146.25</td><td>1.672 </td><td>3     </td><td>1     </td><td>1     </td><td>2     </td><td>0     </td><td>1949  </td><td>3     </td><td>1     </td><td>22.617</td><td>0     </td></tr>
	<tr><td>177.50</td><td>1.588 </td><td>4     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1980  </td><td>3     </td><td>2     </td><td>21.925</td><td>0     </td></tr>
	<tr><td>153.65</td><td>1.752 </td><td>4     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1950  </td><td>3     </td><td>6     </td><td> 9.126</td><td>0     </td></tr>
	<tr><td>199.50</td><td>1.674 </td><td>4     </td><td>2     </td><td>0     </td><td>2     </td><td>0     </td><td>1947  </td><td>3     </td><td>1     </td><td>33.237</td><td>0     </td></tr>
	<tr><td>186.00</td><td>1.980 </td><td>3     </td><td>1     </td><td>0     </td><td>1     </td><td>0     </td><td>1927  </td><td>3     </td><td>6     </td><td>47.679</td><td>0     </td></tr>
	<tr><td>139.90</td><td>1.396 </td><td>1     </td><td>1     </td><td>0     </td><td>2     </td><td>0     </td><td>1950  </td><td>3     </td><td>1     </td><td>25.879</td><td>0     </td></tr>
	<tr><td>160.00</td><td>1.178 </td><td>1     </td><td>1     </td><td>0     </td><td>2     </td><td>0     </td><td>1959  </td><td>3     </td><td>1     </td><td> 9.941</td><td>0     </td></tr>
	<tr><td>125.00</td><td>1.263 </td><td>2     </td><td>2     </td><td>0     </td><td>0     </td><td>0     </td><td>1955  </td><td>3     </td><td>1     </td><td>12.357</td><td>0     </td></tr>
	<tr><td>359.90</td><td>2.377 </td><td>5     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1937  </td><td>3     </td><td>6     </td><td>51.005</td><td>0     </td></tr>
	<tr><td>184.50</td><td>1.304 </td><td>3     </td><td>1     </td><td>1     </td><td>2     </td><td>0     </td><td>1951  </td><td>3     </td><td>1     </td><td>21.305</td><td>0     </td></tr>
	<tr><td>155.00</td><td>1.340 </td><td>3     </td><td>1     </td><td>0     </td><td>0     </td><td>0     </td><td>1952  </td><td>3     </td><td>1     </td><td> 5.666</td><td>0     </td></tr>
	<tr><td>150.00</td><td>1.559 </td><td>2     </td><td>1     </td><td>0     </td><td>2     </td><td>0     </td><td>1952  </td><td>3     </td><td>1     </td><td>23.999</td><td>0     </td></tr>
	<tr><td>146.00</td><td>1.412 </td><td>1     </td><td>2     </td><td>1     </td><td>0     </td><td>0     </td><td>1920  </td><td>3     </td><td>1     </td><td> 4.560</td><td>0     </td></tr>
	<tr><td>129.00</td><td>1.198 </td><td>2     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1925  </td><td>3     </td><td>1     </td><td>20.918</td><td>0     </td></tr>
	<tr><td>145.00</td><td>1.424 </td><td>2     </td><td>1     </td><td>1     </td><td>2     </td><td>0     </td><td>1947  </td><td>3     </td><td>1     </td><td>16.414</td><td>0     </td></tr>
	<tr><td>200.00</td><td>1.370 </td><td>4     </td><td>1     </td><td>0     </td><td>1     </td><td>0     </td><td>1925  </td><td>3     </td><td>4     </td><td> 8.000</td><td>0     </td></tr>
	<tr><td>149.90</td><td>1.584 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1957  </td><td>3     </td><td>1     </td><td>13.514</td><td>0     </td></tr>
	<tr><td>132.00</td><td>1.567 </td><td>2     </td><td>1     </td><td>1     </td><td>1     </td><td>0     </td><td>1934  </td><td>3     </td><td>4     </td><td>12.249</td><td>0     </td></tr>
	<tr><td>136.90</td><td>1.409 </td><td>2     </td><td>1     </td><td>0     </td><td>1     </td><td>0     </td><td>1951  </td><td>3     </td><td>1     </td><td>28.421</td><td>0     </td></tr>
	<tr><td>137.00</td><td>1.655 </td><td>2     </td><td>1     </td><td>0     </td><td>1     </td><td>0     </td><td>1935  </td><td>3     </td><td>1     </td><td>54.651</td><td>0     </td></tr>
	<tr><td>185.00</td><td>1.944 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1939  </td><td>3     </td><td>6     </td><td>17.999</td><td>0     </td></tr>
	<tr><td>133.50</td><td>1.922 </td><td>3     </td><td>1     </td><td>0     </td><td>2     </td><td>0     </td><td>1950  </td><td>3     </td><td>1     </td><td>14.805</td><td>0     </td></tr>
	<tr><td>124.00</td><td>1.480 </td><td>3     </td><td>2     </td><td>1     </td><td>2     </td><td>0     </td><td>1953  </td><td>3     </td><td>1     </td><td>28.351</td><td>0     </td></tr>
	<tr><td> 95.50</td><td>1.184 </td><td>2     </td><td>1     </td><td>0     </td><td>1     </td><td>0     </td><td>1951  </td><td>3     </td><td>1     </td><td>14.786</td><td>0     </td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[88]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>d_V <span class="o">&lt;-</span> lm<span class="p">(</span>SalesPrice<span class="o">~</span>SqFeet<span class="o">+</span>Beds<span class="o">+</span>Baths<span class="o">+</span>AirCond<span class="o">+</span>Garage<span class="o">+</span>Pool<span class="o">+</span>Year<span class="o">+</span>Quality<span class="o">+</span>Style<span class="o">+</span>Lot<span class="o">+</span>Highway<span class="p">,</span>data <span class="o">=</span> r_est<span class="p">)</span>
ols_step_all_possible<span class="p">(</span>d_V<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>mindex</th><th scope=col>n</th><th scope=col>predictors</th><th scope=col>rsquare</th><th scope=col>adjr</th><th scope=col>predrsq</th><th scope=col>cp</th><th scope=col>aic</th><th scope=col>sbic</th><th scope=col>sbc</th><th scope=col>msep</th><th scope=col>fpe</th><th scope=col>apc</th><th scope=col>hsp</th></tr></thead>
<tbody>
	<tr><th scope=row>1</th><td> 1             </td><td>1              </td><td>SqFeet         </td><td>0.676943525    </td><td>0.6763210657   </td><td> 0.673082541   </td><td> 274.2860      </td><td>6026.136       </td><td>4546.003       </td><td>6038.903       </td><td> 6153.518      </td><td> 6153.427      </td><td>0.3255463      </td><td>11.833775      </td></tr>
	<tr><th scope=row>8</th><td> 2             </td><td>1              </td><td>Quality        </td><td>0.572302678    </td><td>0.5714785987   </td><td> 0.568433754   </td><td> 530.5905      </td><td>6172.323       </td><td>4691.273       </td><td>6185.090       </td><td> 8146.696      </td><td> 8146.576      </td><td>0.4309936      </td><td>15.666839      </td></tr>
	<tr><th scope=row>3</th><td> 3             </td><td>1              </td><td>Baths          </td><td>0.488229039    </td><td>0.4872429679   </td><td> 0.482659152   </td><td> 736.5182      </td><td>6265.822       </td><td>4784.268       </td><td>6278.589       </td><td> 9748.115      </td><td> 9747.971      </td><td>0.5157152      </td><td>18.746513      </td></tr>
	<tr><th scope=row>5</th><td> 4             </td><td>1              </td><td>Garage         </td><td>0.331606045    </td><td>0.3303181951   </td><td> 0.323859725   </td><td>1120.1464      </td><td>6404.930       </td><td>4922.739       </td><td>6417.697       </td><td>12731.439      </td><td>12731.251      </td><td>0.6735454      </td><td>24.483718      </td></tr>
	<tr><th scope=row>7</th><td> 5             </td><td>1              </td><td>Year           </td><td>0.306226804    </td><td>0.3048900539   </td><td> 0.298226217   </td><td>1182.3096      </td><td>6424.346       </td><td>4942.077       </td><td>6437.113       </td><td>13214.858      </td><td>13214.663      </td><td>0.6991202      </td><td>25.413377      </td></tr>
	<tr><th scope=row>2</th><td> 6             </td><td>1              </td><td>Beds           </td><td>0.186226514    </td><td>0.1846585499   </td><td> 0.180237534   </td><td>1476.2352      </td><td>6507.465       </td><td>5024.885       </td><td>6520.232       </td><td>15500.601      </td><td>15500.372      </td><td>0.8200453      </td><td>29.809068      </td></tr>
	<tr><th scope=row>9</th><td> 7             </td><td>1              </td><td>Style          </td><td>0.131143852    </td><td>0.1294697559   </td><td> 0.123622583   </td><td>1611.1532      </td><td>6541.588       </td><td>5058.892       </td><td>6554.355       </td><td>16549.805      </td><td>16549.560      </td><td>0.8755525      </td><td>31.826782      </td></tr>
	<tr><th scope=row>4</th><td> 8             </td><td>1              </td><td>AirCond        </td><td>0.082941782    </td><td>0.0811748104   </td><td> 0.077823703   </td><td>1729.2181      </td><td>6569.718       </td><td>5086.932       </td><td>6582.486       </td><td>17467.948      </td><td>17467.691      </td><td>0.9241261      </td><td>33.592456      </td></tr>
	<tr><th scope=row>10</th><td> 9             </td><td>1              </td><td>Lot            </td><td>0.048944000    </td><td>0.0471115218   </td><td> 0.041269842   </td><td>1812.4913      </td><td>6588.684       </td><td>5105.839       </td><td>6601.451       </td><td>18115.532      </td><td>18115.264      </td><td>0.9583859      </td><td>34.837818      </td></tr>
	<tr><th scope=row>6</th><td>10             </td><td>1              </td><td>Pool           </td><td>0.021917262    </td><td>0.0200327099   </td><td> 0.014411550   </td><td>1878.6899      </td><td>6603.283       </td><td>5120.394       </td><td>6616.050       </td><td>18630.332      </td><td>18630.057      </td><td>0.9856209      </td><td>35.827825      </td></tr>
	<tr><th scope=row>11</th><td>11             </td><td>1              </td><td>Highway        </td><td>0.002562165    </td><td>0.0006403195   </td><td>-0.002873205   </td><td>1926.0977      </td><td>6613.492       </td><td>5130.573       </td><td>6626.259       </td><td>18999.004      </td><td>18998.723      </td><td>1.0051252      </td><td>36.536816      </td></tr>
	<tr><th scope=row>18</th><td>12             </td><td>2              </td><td>SqFeet Quality </td><td>0.741477771    </td><td>0.7404796160   </td><td> 0.736808161   </td><td> 118.2175      </td><td>5912.034       </td><td>4432.374       </td><td>5929.057       </td><td> 4943.331      </td><td> 4943.149      </td><td>0.2615167      </td><td> 9.506476      </td></tr>
	<tr><th scope=row>17</th><td>13             </td><td>2              </td><td>SqFeet Year    </td><td>0.721477711    </td><td>0.7204023358   </td><td> 0.716589534   </td><td> 167.2051      </td><td>5950.857       </td><td>4470.793       </td><td>5967.880       </td><td> 5325.762      </td><td> 5325.566      </td><td>0.2817484      </td><td>10.241926      </td></tr>
	<tr><th scope=row>19</th><td>14             </td><td>2              </td><td>SqFeet Style   </td><td>0.711146359    </td><td>0.7100310943   </td><td> 0.705508843   </td><td> 192.5104      </td><td>5969.833       </td><td>4489.578       </td><td>5986.856       </td><td> 5523.313      </td><td> 5523.109      </td><td>0.2921994      </td><td>10.621834      </td></tr>
	<tr><th scope=row>15</th><td>15             </td><td>2              </td><td>SqFeet Garage  </td><td>0.702663222    </td><td>0.7015152033   </td><td> 0.697519748   </td><td> 213.2888      </td><td>5984.913       </td><td>4504.509       </td><td>6001.936       </td><td> 5685.523      </td><td> 5685.313      </td><td>0.3007808      </td><td>10.933779      </td></tr>
	<tr><th scope=row>13</th><td>16             </td><td>2              </td><td>SqFeet Baths   </td><td>0.689968383    </td><td>0.6887713492   </td><td> 0.684549827   </td><td> 244.3832      </td><td>6006.696       </td><td>4526.081       </td><td>6023.719       </td><td> 5928.268      </td><td> 5928.049      </td><td>0.3136227      </td><td>11.400599      </td></tr>
	<tr><th scope=row>20</th><td>17             </td><td>2              </td><td>SqFeet Lot     </td><td>0.685462963    </td><td>0.6842485340   </td><td> 0.679176135   </td><td> 255.4187      </td><td>6014.212       </td><td>4533.526       </td><td>6031.235       </td><td> 6014.418      </td><td> 6014.196      </td><td>0.3181803      </td><td>11.566274      </td></tr>
	<tr><th scope=row>14</th><td>18             </td><td>2              </td><td>SqFeet AirCond </td><td>0.681831681    </td><td>0.6806032321   </td><td> 0.677289374   </td><td> 264.3130      </td><td>6020.193       </td><td>4539.450       </td><td>6037.216       </td><td> 6083.853      </td><td> 6083.629      </td><td>0.3218537      </td><td>11.699804      </td></tr>
	<tr><th scope=row>12</th><td>19             </td><td>2              </td><td>SqFeet Beds    </td><td>0.678413743    </td><td>0.6771720969   </td><td> 0.672737196   </td><td> 272.6848      </td><td>6025.760       </td><td>4544.965       </td><td>6042.783       </td><td> 6149.210      </td><td> 6148.983      </td><td>0.3253112      </td><td>11.825490      </td></tr>
	<tr><th scope=row>16</th><td>20             </td><td>2              </td><td>SqFeet Pool    </td><td>0.677159360    </td><td>0.6759128706   </td><td> 0.671532363   </td><td> 275.7573      </td><td>6027.788       </td><td>4546.974       </td><td>6044.811       </td><td> 6173.195      </td><td> 6172.967      </td><td>0.3265801      </td><td>11.871617      </td></tr>
	<tr><th scope=row>21</th><td>21             </td><td>2              </td><td>SqFeet Highway </td><td>0.676944006    </td><td>0.6756966853   </td><td> 0.672112555   </td><td> 276.2848      </td><td>6028.135       </td><td>4547.319       </td><td>6045.158       </td><td> 6177.313      </td><td> 6177.085      </td><td>0.3267980      </td><td>11.879536      </td></tr>
	<tr><th scope=row>35</th><td>22             </td><td>2              </td><td>Baths Quality  </td><td>0.629313368    </td><td>0.6278821455   </td><td> 0.623597048   </td><td> 392.9500      </td><td>6099.789       </td><td>4618.335       </td><td>6116.812       </td><td> 7088.082      </td><td> 7087.820      </td><td>0.3749803      </td><td>13.631028      </td></tr>
	<tr><th scope=row>48</th><td>23             </td><td>2              </td><td>Garage Quality </td><td>0.610359396    </td><td>0.6088549922   </td><td> 0.604651754   </td><td> 439.3753      </td><td>6125.770       </td><td>4644.099       </td><td>6142.793       </td><td> 7450.510      </td><td> 7450.235      </td><td>0.3941538      </td><td>14.328010      </td></tr>
	<tr><th scope=row>27</th><td>24             </td><td>2              </td><td>Beds Quality   </td><td>0.592903126    </td><td>0.5913313237   </td><td> 0.587483023   </td><td> 482.1323      </td><td>6148.604       </td><td>4666.749       </td><td>6165.627       </td><td> 7784.300      </td><td> 7784.013      </td><td>0.4118123      </td><td>14.969919      </td></tr>
	<tr><th scope=row>62</th><td>25             </td><td>2              </td><td>Quality Lot    </td><td>0.591050414    </td><td>0.5894714580   </td><td> 0.585582665   </td><td> 486.6703      </td><td>6150.970       </td><td>4669.096       </td><td>6167.993       </td><td> 7819.727      </td><td> 7819.438      </td><td>0.4136865      </td><td>15.038047      </td></tr>
	<tr><th scope=row>57</th><td>26             </td><td>2              </td><td>Year Quality   </td><td>0.584662074    </td><td>0.5830584529   </td><td> 0.579172275   </td><td> 502.3177      </td><td>6159.045       </td><td>4677.108       </td><td>6176.068       </td><td> 7941.881      </td><td> 7941.588      </td><td>0.4201488      </td><td>15.272962      </td></tr>
	<tr><th scope=row>61</th><td>27             </td><td>2              </td><td>Quality Style  </td><td>0.582668816    </td><td>0.5810574985   </td><td> 0.576379107   </td><td> 507.1999      </td><td>6161.540       </td><td>4679.583       </td><td>6178.563       </td><td> 7979.995      </td><td> 7979.701      </td><td>0.4221651      </td><td>15.346258      </td></tr>
	<tr><th scope=row>53</th><td>28             </td><td>2              </td><td>Pool Quality   </td><td>0.575072039    </td><td>0.5734313905   </td><td> 0.569794892   </td><td> 525.8073      </td><td>6170.938       </td><td>4688.909       </td><td>6187.961       </td><td> 8125.257      </td><td> 8124.957      </td><td>0.4298499      </td><td>15.625610      </td></tr>
	<tr><th scope=row>63</th><td>29             </td><td>2              </td><td>Quality Highway</td><td>0.573568918    </td><td>0.5719224663   </td><td> 0.568553276   </td><td> 529.4890      </td><td>6172.778       </td><td>4690.735       </td><td>6189.801       </td><td> 8153.999      </td><td> 8153.698      </td><td>0.4313704      </td><td>15.680883      </td></tr>
	<tr><th scope=row>42</th><td>30             </td><td>2              </td><td>AirCond Quality</td><td>0.573050753    </td><td>0.5714022999   </td><td> 0.568250514   </td><td> 530.7582      </td><td>6173.411       </td><td>4691.362       </td><td>6190.434       </td><td> 8163.907      </td><td> 8163.606      </td><td>0.4318946      </td><td>15.699937      </td></tr>
	<tr><th scope=row>...</th><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td></tr>
	<tr><th scope=row>1999</th><td>2018                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Pool Year Style Lot Highway               </td><td>0.7719683                                                           </td><td>0.7679521                                                           </td><td>0.7585629                                                           </td><td> 57.53471                                                           </td><td>5860.650                                                            </td><td>4380.763                                                            </td><td>5907.463                                                            </td><td>4480.703                                                            </td><td>4478.917                                                            </td><td>0.2369566                                                           </td><td> 8.616801                                                           </td></tr>
	<tr><th scope=row>2019</th><td>2019                                                                </td><td> 9                                                                  </td><td>SqFeet Baths AirCond Garage Pool Year Quality Lot Highway           </td><td>0.7716052                                                           </td><td>0.7675826                                                           </td><td>0.7596010                                                           </td><td> 58.42407                                                           </td><td>5861.479                                                            </td><td>4381.562                                                            </td><td>5908.292                                                            </td><td>4487.838                                                            </td><td>4486.049                                                            </td><td>0.2373339                                                           </td><td> 8.630522                                                           </td></tr>
	<tr><th scope=row>1998</th><td>2020                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Pool Year Quality Lot Highway             </td><td>0.7702827                                                           </td><td>0.7662368                                                           </td><td>0.7579376                                                           </td><td> 61.66336                                                           </td><td>5864.487                                                            </td><td>4384.461                                                            </td><td>5911.300                                                            </td><td>4513.824                                                            </td><td>4512.025                                                            </td><td>0.2387082                                                           </td><td> 8.680496                                                           </td></tr>
	<tr><th scope=row>1985</th><td>2021                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Style Highway            </td><td>0.7661179                                                           </td><td>0.7619987                                                           </td><td>0.7539754                                                           </td><td> 71.86459                                                           </td><td>5873.848                                                            </td><td>4393.487                                                            </td><td>5920.661                                                            </td><td>4595.661                                                            </td><td>4593.829                                                            </td><td>0.2430360                                                           </td><td> 8.837875                                                           </td></tr>
	<tr><th scope=row>1983</th><td>2022                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Quality Highway          </td><td>0.7622001                                                           </td><td>0.7580119                                                           </td><td>0.7505396                                                           </td><td> 81.46069                                                           </td><td>5882.503                                                            </td><td>4401.836                                                            </td><td>5929.316                                                            </td><td>4672.644                                                            </td><td>4670.781                                                            </td><td>0.2471071                                                           </td><td> 8.985919                                                           </td></tr>
	<tr><th scope=row>1989</th><td>2023                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Quality Lot Highway           </td><td>0.7608196                                                           </td><td>0.7566071                                                           </td><td>0.7486254                                                           </td><td> 84.84207                                                           </td><td>5885.519                                                            </td><td>4404.747                                                            </td><td>5932.332                                                            </td><td>4699.770                                                            </td><td>4697.896                                                            </td><td>0.2485416                                                           </td><td> 9.038085                                                           </td></tr>
	<tr><th scope=row>1986</th><td>2024                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Lot Highway              </td><td>0.7536934                                                           </td><td>0.7493553                                                           </td><td>0.7403185                                                           </td><td>102.29680                                                           </td><td>5900.815                                                            </td><td>4419.515                                                            </td><td>5947.628                                                            </td><td>4839.796                                                            </td><td>4837.867                                                            </td><td>0.2559468                                                           </td><td> 9.307369                                                           </td></tr>
	<tr><th scope=row>1990</th><td>2025                                                                </td><td> 9                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Style Lot Highway             </td><td>0.7490245                                                           </td><td>0.7446042                                                           </td><td>0.7349501                                                           </td><td>113.73264                                                           </td><td>5910.598                                                            </td><td>4428.968                                                            </td><td>5957.412                                                            </td><td>4931.537                                                            </td><td>4929.571                                                            </td><td>0.2607984                                                           </td><td> 9.483795                                                           </td></tr>
	<tr><th scope=row>2028</th><td>2026                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Garage Pool Year Quality Lot Highway             </td><td>0.6747779                                                           </td><td>0.6690499                                                           </td><td>0.6607720                                                           </td><td>295.59039                                                           </td><td>6045.617                                                            </td><td>4559.925                                                            </td><td>6092.430                                                            </td><td>6390.445                                                            </td><td>6387.897                                                            </td><td>0.3379510                                                           </td><td>12.289408                                                           </td></tr>
	<tr><th scope=row>2035</th><td>2027                                                                </td><td> 9                                                                  </td><td>Baths AirCond Garage Pool Year Quality Style Lot Highway            </td><td>0.6746325                                                           </td><td>0.6689020                                                           </td><td>0.6600620                                                           </td><td>295.94652                                                           </td><td>6045.850                                                            </td><td>4560.151                                                            </td><td>6092.663                                                            </td><td>6393.302                                                            </td><td>6390.753                                                            </td><td>0.3381020                                                           </td><td>12.294902                                                           </td></tr>
	<tr><th scope=row>2031</th><td>2028                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Garage Year Quality Style Lot Highway            </td><td>0.6743164                                                           </td><td>0.6685803                                                           </td><td>0.6599135                                                           </td><td>296.72083                                                           </td><td>6046.356                                                            </td><td>4560.644                                                            </td><td>6093.169                                                            </td><td>6399.514                                                            </td><td>6396.962                                                            </td><td>0.3384305                                                           </td><td>12.306848                                                           </td></tr>
	<tr><th scope=row>2026</th><td>2029                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Garage Pool Year Quality Style Lot               </td><td>0.6736613                                                           </td><td>0.6679137                                                           </td><td>0.6582024                                                           </td><td>298.32533                                                           </td><td>6047.403                                                            </td><td>4561.662                                                            </td><td>6094.216                                                            </td><td>6412.385                                                            </td><td>6409.829                                                            </td><td>0.3391112                                                           </td><td>12.331601                                                           </td></tr>
	<tr><th scope=row>2033</th><td>2030                                                                </td><td> 9                                                                  </td><td>Beds Baths Garage Pool Year Quality Style Lot Highway               </td><td>0.6717538                                                           </td><td>0.6659726                                                           </td><td>0.6568161                                                           </td><td>302.99744                                                           </td><td>6050.439                                                            </td><td>4564.618                                                            </td><td>6097.252                                                            </td><td>6449.866                                                            </td><td>6447.295                                                            </td><td>0.3410934                                                           </td><td>12.403680                                                           </td></tr>
	<tr><th scope=row>2030</th><td>2031                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Garage Pool Quality Style Lot Highway            </td><td>0.6664841                                                           </td><td>0.6606100                                                           </td><td>0.6517813                                                           </td><td>315.90498                                                           </td><td>6058.737                                                            </td><td>4572.696                                                            </td><td>6105.550                                                            </td><td>6553.413                                                            </td><td>6550.801                                                            </td><td>0.3465694                                                           </td><td>12.602811                                                           </td></tr>
	<tr><th scope=row>2027</th><td>2032                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Garage Pool Year Quality Style Highway           </td><td>0.6624239                                                           </td><td>0.6564783                                                           </td><td>0.6472290                                                           </td><td>325.85003                                                           </td><td>6065.041                                                            </td><td>4578.836                                                            </td><td>6111.855                                                            </td><td>6633.195                                                            </td><td>6630.551                                                            </td><td>0.3507885                                                           </td><td>12.756239                                                           </td></tr>
	<tr><th scope=row>2032</th><td>2033                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Pool Year Quality Style Lot Highway              </td><td>0.6594563                                                           </td><td>0.6534585                                                           </td><td>0.6447211                                                           </td><td>333.11861                                                           </td><td>6069.601                                                            </td><td>4583.278                                                            </td><td>6116.415                                                            </td><td>6691.505                                                            </td><td>6688.838                                                            </td><td>0.3538722                                                           </td><td>12.868375                                                           </td></tr>
	<tr><th scope=row>2034</th><td>2034                                                                </td><td> 9                                                                  </td><td>Beds AirCond Garage Pool Year Quality Style Lot Highway             </td><td>0.6585403                                                           </td><td>0.6525263                                                           </td><td>0.6436287                                                           </td><td>335.36231                                                           </td><td>6071.001                                                            </td><td>4584.641                                                            </td><td>6117.814                                                            </td><td>6709.505                                                            </td><td>6706.830                                                            </td><td>0.3548241                                                           </td><td>12.902990                                                           </td></tr>
	<tr><th scope=row>2029</th><td>2035                                                                </td><td> 9                                                                  </td><td>Beds Baths AirCond Garage Pool Year Style Lot Highway               </td><td>0.6047513                                                           </td><td>0.5977900                                                           </td><td>0.5856230                                                           </td><td>467.11165                                                           </td><td>6147.216                                                            </td><td>4659.018                                                            </td><td>6194.029                                                            </td><td>7766.431                                                            </td><td>7763.335                                                            </td><td>0.4107183                                                           </td><td>14.935554                                                           </td></tr>
	<tr><th scope=row>2041</th><td>2036                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Garage Year Quality Style Lot Highway     </td><td>0.7919362                                                           </td><td>0.7878565                                                           </td><td>0.7795007                                                           </td><td> 10.62605                                                           </td><td>5814.905                                                            </td><td>4336.862                                                            </td><td>5865.974                                                            </td><td>4104.410                                                            </td><td>4102.441                                                            </td><td>0.2170391                                                           </td><td> 7.893155                                                           </td></tr>
	<tr><th scope=row>2044</th><td>2037                                                                </td><td>10                                                                  </td><td>SqFeet Beds AirCond Garage Pool Year Quality Style Lot Highway      </td><td>0.7917750                                                           </td><td>0.7876921                                                           </td><td>0.7795245                                                           </td><td> 11.02090                                                           </td><td>5815.309                                                            </td><td>4337.248                                                            </td><td>5866.378                                                            </td><td>4107.590                                                            </td><td>4105.619                                                            </td><td>0.2172073                                                           </td><td> 7.899270                                                           </td></tr>
	<tr><th scope=row>2043</th><td>2038                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths Garage Pool Year Quality Style Lot Highway        </td><td>0.7911738                                                           </td><td>0.7870792                                                           </td><td>0.7784236                                                           </td><td> 12.49331                                                           </td><td>5816.811                                                            </td><td>4338.685                                                            </td><td>5867.880                                                            </td><td>4119.449                                                            </td><td>4117.472                                                            </td><td>0.2178344                                                           </td><td> 7.922075                                                           </td></tr>
	<tr><th scope=row>2036</th><td>2039                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Quality Style Lot        </td><td>0.7907014                                                           </td><td>0.7865975                                                           </td><td>0.7775640                                                           </td><td> 13.65048                                                           </td><td>5817.988                                                            </td><td>4339.812                                                            </td><td>5869.057                                                            </td><td>4128.768                                                            </td><td>4126.787                                                            </td><td>0.2183272                                                           </td><td> 7.939998                                                           </td></tr>
	<tr><th scope=row>2045</th><td>2040                                                                </td><td>10                                                                  </td><td>SqFeet Baths AirCond Garage Pool Year Quality Style Lot Highway     </td><td>0.7899758                                                           </td><td>0.7858577                                                           </td><td>0.7773569                                                           </td><td> 15.42771                                                           </td><td>5819.791                                                            </td><td>4341.538                                                            </td><td>5870.860                                                            </td><td>4143.082                                                            </td><td>4141.094                                                            </td><td>0.2190841                                                           </td><td> 7.967524                                                           </td></tr>
	<tr><th scope=row>2042</th><td>2041                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Pool Year Quality Style Lot Highway       </td><td>0.7896805                                                           </td><td>0.7855566                                                           </td><td>0.7767028                                                           </td><td> 16.15089                                                           </td><td>5820.523                                                            </td><td>4342.239                                                            </td><td>5871.592                                                            </td><td>4148.906                                                            </td><td>4146.915                                                            </td><td>0.2193921                                                           </td><td> 7.978724                                                           </td></tr>
	<tr><th scope=row>2037</th><td>2042                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Quality Style Highway    </td><td>0.7840221                                                           </td><td>0.7797872                                                           </td><td>0.7718460                                                           </td><td> 30.01058                                                           </td><td>5834.355                                                            </td><td>4355.487                                                            </td><td>5885.424                                                            </td><td>4260.529                                                            </td><td>4258.484                                                            </td><td>0.2252946                                                           </td><td> 8.193385                                                           </td></tr>
	<tr><th scope=row>2040</th><td>2043                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Quality Style Lot Highway     </td><td>0.7790602                                                           </td><td>0.7747281                                                           </td><td>0.7662039                                                           </td><td> 42.16403                                                           </td><td>5846.189                                                            </td><td>4366.833                                                            </td><td>5897.258                                                            </td><td>4358.410                                                            </td><td>4356.318                                                            </td><td>0.2304705                                                           </td><td> 8.381619                                                           </td></tr>
	<tr><th scope=row>2039</th><td>2044                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Style Lot Highway        </td><td>0.7761220                                                           </td><td>0.7717322                                                           </td><td>0.7621184                                                           </td><td> 49.36085                                                           </td><td>5853.072                                                            </td><td>4373.435                                                            </td><td>5904.141                                                            </td><td>4416.371                                                            </td><td>4414.252                                                            </td><td>0.2335355                                                           </td><td> 8.493085                                                           </td></tr>
	<tr><th scope=row>2038</th><td>2045                                                                </td><td>10                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Quality Lot Highway      </td><td>0.7742538                                                           </td><td>0.7698274                                                           </td><td>0.7612240                                                           </td><td> 53.93669                                                           </td><td>5857.401                                                            </td><td>4377.590                                                            </td><td>5908.470                                                            </td><td>4453.224                                                            </td><td>4451.087                                                            </td><td>0.2354842                                                           </td><td> 8.563956                                                           </td></tr>
	<tr><th scope=row>2046</th><td>2046                                                                </td><td>10                                                                  </td><td>Beds Baths AirCond Garage Pool Year Quality Style Lot Highway       </td><td>0.6752917                                                           </td><td>0.6689248                                                           </td><td>0.6593261                                                           </td><td>296.33195                                                           </td><td>6046.793                                                            </td><td>4560.433                                                            </td><td>6097.862                                                            </td><td>6405.419                                                            </td><td>6402.346                                                            </td><td>0.3387153                                                           </td><td>12.318205                                                           </td></tr>
	<tr><th scope=row>2047</th><td>2047                                                                </td><td>11                                                                  </td><td>SqFeet Beds Baths AirCond Garage Pool Year Quality Style Lot Highway</td><td>0.7921918                                                           </td><td>0.7877008                                                           </td><td>0.7786135                                                           </td><td> 12.00000                                                           </td><td>5816.265                                                            </td><td>4338.296                                                            </td><td>5871.590                                                            </td><td>4115.507                                                            </td><td>4113.168                                                            </td><td>0.2176067                                                           </td><td> 7.914496                                                           </td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[97]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>m<span class="o">=</span> ols_step_all_possible<span class="p">(</span>d_V<span class="p">)</span>
<span class="kp">summary</span><span class="p">(</span>d_V<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = SalesPrice ~ SqFeet + Beds + Baths + AirCond + Garage + 
    Pool + Year + Quality + Style + Lot + Highway, data = r_est)

Residuals:
    Min      1Q  Median      3Q     Max 
-186.25  -37.55   -2.36   31.70  293.79 

Coefficients:
              Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) -2351.8910   433.9996  -5.419 9.26e-08 ***
SqFeet        129.7452     7.6675  16.921  &lt; 2e-16 ***
Beds           -8.2357     3.5350  -2.330   0.0202 *  
Baths           4.7172     4.6687   1.010   0.3128    
AirCond       -13.5533     8.5834  -1.579   0.1150    
Garage         13.5320     5.4562   2.480   0.0135 *  
Pool            8.8900    11.2356   0.791   0.4292    
Year            1.2410     0.2188   5.671 2.38e-08 ***
Quality       -46.6914     7.4423  -6.274 7.54e-10 ***
Style          -9.4818     1.4305  -6.628 8.66e-11 ***
Lot             1.1536     0.2579   4.473 9.51e-06 ***
Highway       -37.4620    19.6072  -1.911   0.0566 .  
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 63.41 on 509 degrees of freedom
Multiple R-squared:  0.7922,	Adjusted R-squared:  0.7877 
F-statistic: 176.4 on 11 and 509 DF,  p-value: &lt; 2.2e-16
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[92]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>m<span class="p">[</span><span class="kp">which</span><span class="p">(</span>m<span class="p">[</span><span class="s">&quot;cp&quot;</span><span class="p">]</span><span class="o">==</span><span class="kp">min</span><span class="p">(</span>m<span class="p">[</span><span class="s">&quot;cp&quot;</span><span class="p">])),]</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>mindex</th><th scope=col>n</th><th scope=col>predictors</th><th scope=col>rsquare</th><th scope=col>adjr</th><th scope=col>predrsq</th><th scope=col>cp</th><th scope=col>aic</th><th scope=col>sbic</th><th scope=col>sbc</th><th scope=col>msep</th><th scope=col>fpe</th><th scope=col>apc</th><th scope=col>hsp</th></tr></thead>
<tbody>
	<tr><th scope=row>2014</th><td>1981                                                     </td><td>9                                                        </td><td>SqFeet Beds AirCond Garage Year Quality Style Lot Highway</td><td>0.7914493                                                </td><td>0.7877762                                                </td><td>0.7803609                                                </td><td>9.818642                                                 </td><td>5814.123                                                 </td><td>4335.987                                                 </td><td>5860.936                                                 </td><td>4097.913                                                 </td><td>4096.28                                                  </td><td>0.2167132                                                </td><td>7.880661                                                 </td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We fitted a full ols model . And then we just try all possible models with different number of subsets. And as we see from the table that the smallest cp we get was 9.818642 when we have 9 variables. Now we want to fit a model with these variables. It would be our best subset model with the smalles Mallows CP.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[95]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>new_model <span class="o">=</span> lm<span class="p">(</span>SalesPrice<span class="o">~</span>SqFeet<span class="o">+</span>Beds<span class="o">+</span>AirCond<span class="o">+</span>Garage<span class="o">+</span>Year<span class="o">+</span>Quality<span class="o">+</span>Style<span class="o">+</span>Lot<span class="o">+</span>Highway<span class="p">,</span>data <span class="o">=</span> r_est<span class="p">)</span>
<span class="kp">summary</span><span class="p">(</span>new_model<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = SalesPrice ~ SqFeet + Beds + AirCond + Garage + 
    Year + Quality + Style + Lot + Highway, data = r_est)

Residuals:
     Min       1Q   Median       3Q      Max 
-200.882  -38.112   -2.321   31.847  295.698 

Coefficients:
              Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept) -2404.8069   427.1919  -5.629 2.99e-08 ***
SqFeet        132.5857     7.2880  18.192  &lt; 2e-16 ***
Beds           -7.0923     3.3941  -2.090   0.0371 *  
AirCond       -12.9699     8.5694  -1.514   0.1308    
Garage         13.8375     5.4506   2.539   0.0114 *  
Year            1.2706     0.2148   5.916 6.04e-09 ***
Quality       -48.6607     7.2108  -6.748 4.07e-11 ***
Style          -9.3659     1.4208  -6.592 1.08e-10 ***
Lot             1.1647     0.2557   4.555 6.55e-06 ***
Highway       -38.4819    19.5891  -1.964   0.0500 .  
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 63.4 on 511 degrees of freedom
Multiple R-squared:  0.7914,	Adjusted R-squared:  0.7878 
F-statistic: 215.5 on 9 and 511 DF,  p-value: &lt; 2.2e-16
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As we see that  our R^2 adjusted a bit better now. And we have excluded two unsignificant variables.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[101]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>anova<span class="p">(</span>new_model<span class="p">,</span>d_V<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th scope=col>Res.Df</th><th scope=col>RSS</th><th scope=col>Df</th><th scope=col>Sum of Sq</th><th scope=col>F</th><th scope=col>Pr(&gt;F)</th></tr></thead>
<tbody>
	<tr><td>511      </td><td>2053779  </td><td>NA       </td><td>      NA </td><td>       NA</td><td>       NA</td></tr>
	<tr><td>509      </td><td>2046467  </td><td> 2       </td><td>7311.968 </td><td>0.9093212</td><td>0.4034509</td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We have not significant differences between a full model and a short model. Additional predictors doesn't have any additional explanation of the variation.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">

<pre><code>                                    Diagnostic plots of the model:</code></pre>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[103]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>layout<span class="p">(</span><span class="kt">matrix</span><span class="p">(</span><span class="kt">c</span><span class="p">(</span><span class="m">1</span><span class="p">,</span><span class="m">2</span><span class="p">,</span><span class="m">3</span><span class="p">,</span><span class="m">4</span><span class="p">),</span><span class="m">2</span><span class="p">,</span><span class="m">2</span><span class="p">))</span>
plot<span class="p">(</span>new_model<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>From the first plot we see that our residuals have non-linear patterns.And also we can see there some sign of the heteroscedasticity.Spread of our residuals are  getting bigger as our 
 fitted values are increasing. We can regulate this with GLS or FGLS.</p>
<p>In the second plot we see quite the same as in the first one: nonlinearity of residuals and some heteroscedasticity. And we have to apply the same techniques as in the first case to get rid of heteroscedasticity.</p>
<p>In the third plot we can say that our residuals are normaldistributed with some extrem values.</p>
<p>And in the fourth plot we see that we have no influential outliers in our model. All points are lying in the Cook's distance.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[117]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>VIF<span class="p">(</span>new_model<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
4.79499619940548
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This is our VIF for our new subset model. As it was said in lection if vif is  larger than 4 then it's a reason for concern.
And maybe we would  try to fit some reguralized models to get rid of Multicollinearity. For example: Ridge Regression.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[118]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>VIF<span class="p">(</span>d_V<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
4.8121285830025
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In our full model vif is big enough too. It means everything, what was said about subset model, apllies here as well.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[146]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>new_model2 <span class="o">=</span> lm<span class="p">(</span>SalesPrice<span class="o">~</span>SqFeet<span class="o">+</span>Beds<span class="o">+</span>AirCond<span class="o">+</span>Garage<span class="o">+</span>Year<span class="o">+</span>Quality<span class="o">+</span>Style<span class="o">+</span>Lot<span class="o">+</span>Highway<span class="p">,</span>data <span class="o">=</span> r_est<span class="p">)</span>
x<span class="o">=</span>boxcox<span class="p">(</span>new_model2<span class="p">,</span> lambda <span class="o">=</span> <span class="kp">seq</span><span class="p">(</span><span class="m">-2</span><span class="p">,</span> <span class="m">2</span><span class="p">,</span> <span class="m">1</span><span class="o">/</span><span class="m">10</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
3bm70F97BU9283lsu/O9C2urg+vD/vzX97AtPZAphufuQn/tlT9Zu/MderOD24TjcPnn6qb0
QKYYnrsbNYV0CuvSQ5hysFt5sP5qbnjufiivveInuxs3KVZZvRjMhzQYH9xIee2VPtljZ3Z3
cmH1YiAkAem1V/hkT53Zjd3I6sVASPG0116Bk739vdFrg++E3I7P6sXQEVI07bVXNKTjan3M
f/xnPIT0edfuaPeu3WB37j6pr72SJ7u3e8Pum9WLYTt+m7wPfemBPGB17kbya6/gyR7td2T2
YrD/ZIPdubvQX3sFT/YthNtdlElmB7caZ870P4nMzt2Q4toreLKBkJY7jU9/lx7FQ2bnbkhx
7Rk+WcAPQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRA
gJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQ
AAFCAgQIyafTqtuXHgNuEJJPb+/D6lR6EPhBSD6d1233XnoQ+EFIbh02pUeAH4Tk1r4rPQL8
ICS3VqydISyGV/sQDqXHgCtC8moV3rjbYAchObUPm/e+9CBwRUhOrcOB23aGEJJPh7Bh8Sxh
LXzaXO40rE+snxUshEvjC9Kwe/9YlR4JPhGSS5vPW9/r7qP0SPCJkAABQgIECAkQICRAgJAA
AUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFC
AgQICRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJEPgHJYziLjYJ37YAAAAASUVORK5CYII="
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[152]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>x<span class="o">$</span>x<span class="p">[</span><span class="kp">which</span><span class="p">(</span>x<span class="o">$</span>y<span class="o">==</span><span class="kp">max</span><span class="p">(</span>x<span class="o">$</span>y<span class="p">))]</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
-0.262626262626263
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We are using here Box-Cox Transformation. Our purpose is to find lambds for the smallest log-likelihood. Now with the help of this graph we see at which lambda we have the smallest log-likelihood.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[176]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>lambda <span class="o">=</span> <span class="m">-0.262626262626263</span> 
 r_est<span class="o">$</span>SalesPrice <span class="o">=</span> <span class="p">((</span>r_est<span class="o">$</span>SalesPrice<span class="p">)</span><span class="o">^</span><span class="p">(</span>lambda<span class="p">)</span><span class="m">-1</span><span class="p">)</span><span class="o">/</span>lambda
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>And now we transform with the help of this lambda our response value. And fit our model again to see, whether there are
some improvements.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[178]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>new_model2 <span class="o">=</span> lm<span class="p">(</span>SalesPrice<span class="o">~</span>SqFeet<span class="o">+</span>Beds<span class="o">+</span>AirCond<span class="o">+</span>Garage<span class="o">+</span>Year<span class="o">+</span>Quality<span class="o">+</span>Style<span class="o">+</span>Lot<span class="o">+</span>Highway<span class="p">,</span>data <span class="o">=</span> r_est<span class="p">)</span>
<span class="kp">summary</span><span class="p">(</span>new_model2<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = SalesPrice ~ SqFeet + Beds + AirCond + Garage + 
    Year + Quality + Style + Lot + Highway, data = r_est)

Residuals:
      Min        1Q    Median        3Q       Max 
-0.145899 -0.025223  0.000449  0.028033  0.124799 

Coefficients:
              Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)  0.9638719  0.2800452   3.442 0.000625 ***
SqFeet       0.0762047  0.0047777  15.950  &lt; 2e-16 ***
Beds         0.0042202  0.0022250   1.897 0.058429 .  
AirCond      0.0115551  0.0056177   2.057 0.040202 *  
Garage       0.0095251  0.0035731   2.666 0.007924 ** 
Year         0.0009116  0.0001408   6.475 2.23e-10 ***
Quality     -0.0369583  0.0047270  -7.819 3.08e-14 ***
Style       -0.0029414  0.0009314  -3.158 0.001682 ** 
Lot          0.0011359  0.0001676   6.776 3.40e-11 ***
Highway     -0.0193674  0.0128416  -1.508 0.132126    
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 0.04156 on 511 degrees of freedom
Multiple R-squared:  0.8242,	Adjusted R-squared:  0.8212 
F-statistic: 266.3 on 9 and 511 DF,  p-value: &lt; 2.2e-16
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>And as we see our R^(2) adjusted was improved because of this Box-Cox Transformation.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[184]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="c1">###### Aufgabe 4 ##############</span>
w_r <span class="o">=</span> read.xlsx<span class="p">(</span><span class="s">&quot;WordRecall.xlsx&quot;</span><span class="p">,</span><span class="m">1</span><span class="p">)</span>
w_r <span class="o">=</span> w_r<span class="p">[,</span><span class="m">1</span><span class="o">:</span><span class="m">2</span><span class="p">]</span>
w_r
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th scope=col>time</th><th scope=col>prop</th></tr></thead>
<tbody>
	<tr><td>    1</td><td>0.84 </td></tr>
	<tr><td>    5</td><td>0.71 </td></tr>
	<tr><td>   15</td><td>0.61 </td></tr>
	<tr><td>   30</td><td>0.56 </td></tr>
	<tr><td>   60</td><td>0.54 </td></tr>
	<tr><td>  120</td><td>0.47 </td></tr>
	<tr><td>  240</td><td>0.45 </td></tr>
	<tr><td>  480</td><td>0.38 </td></tr>
	<tr><td>  720</td><td>0.36 </td></tr>
	<tr><td> 1440</td><td>0.26 </td></tr>
	<tr><td> 2880</td><td>0.20 </td></tr>
	<tr><td> 5760</td><td>0.16 </td></tr>
	<tr><td>10080</td><td>0.08 </td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[185]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> time <span class="p">,</span> data <span class="o">=</span> w_r<span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = prop ~ time, data = w_r)

Residuals:
     Min       1Q   Median       3Q      Max 
-0.18564 -0.11913 -0.04495  0.08496  0.31418 

Coefficients:
              Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)  5.259e-01  4.881e-02  10.774 3.49e-07 ***
time        -5.571e-05  1.457e-05  -3.825  0.00282 ** 
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 0.1523 on 11 degrees of freedom
Multiple R-squared:  0.5709,	Adjusted R-squared:  0.5318 
F-statistic: 14.63 on 1 and 11 DF,  p-value: 0.002817
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here we fit just our untransformed value. Then we will trnasform some variables and fit it again to compare adjusted R^(2).</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[186]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> time<span class="m">+1</span><span class="o">/</span>time<span class="p">,</span> data <span class="o">=</span> w_r<span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = prop ~ time + 1/time, data = w_r)

Residuals:
     Min       1Q   Median       3Q      Max 
-0.18564 -0.11913 -0.04495  0.08496  0.31418 

Coefficients:
              Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)  5.259e-01  4.881e-02  10.774 3.49e-07 ***
time        -5.571e-05  1.457e-05  -3.825  0.00282 ** 
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 0.1523 on 11 degrees of freedom
Multiple R-squared:  0.5709,	Adjusted R-squared:  0.5318 
F-statistic: 14.63 on 1 and 11 DF,  p-value: 0.002817
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here we add 1/time term. As we see it doesn't help at all. Therefore we will try something else.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[187]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> <span class="kp">log</span><span class="p">(</span>time<span class="p">)</span> <span class="p">,</span> data <span class="o">=</span> w_r<span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = prop ~ log(time), data = w_r)

Residuals:
      Min        1Q    Median        3Q       Max 
-0.036077 -0.015330 -0.006415  0.017967  0.037799 

Coefficients:
             Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)  0.846415   0.014195   59.63 3.65e-15 ***
log(time)   -0.079227   0.002416  -32.80 2.53e-12 ***
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 0.02339 on 11 degrees of freedom
Multiple R-squared:  0.9899,	Adjusted R-squared:  0.989 
F-statistic:  1076 on 1 and 11 DF,  p-value: 2.525e-12
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[191]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>plot<span class="p">(</span>w_r<span class="p">[,</span><span class="s">&quot;prop&quot;</span><span class="p">]</span><span class="o">~</span>w_r<span class="p">[,</span><span class="s">&quot;time&quot;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
RK5CYII="
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here we transform our predictor with logarithm. And we see that after this transformation our Adjusted R-squared is  0.989.
We can say that this transformation does make sense. There are some non-linear patterns on the graph in our data. Therefore 
it's clear why logarithm transformation improves our model so well.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[192]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span><span class="kp">summary</span><span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> <span class="kp">log</span><span class="p">(</span>time<span class="p">)</span> <span class="o">+</span> <span class="m">1</span><span class="o">/</span>time <span class="p">,</span> data <span class="o">=</span> w_r<span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>
Call:
lm(formula = prop ~ log(time) + 1/time, data = w_r)

Residuals:
      Min        1Q    Median        3Q       Max 
-0.036077 -0.015330 -0.006415  0.017967  0.037799 

Coefficients:
             Estimate Std. Error t value Pr(&gt;|t|)    
(Intercept)  0.846415   0.014195   59.63 3.65e-15 ***
log(time)   -0.079227   0.002416  -32.80 2.53e-12 ***
---
Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1

Residual standard error: 0.02339 on 11 degrees of freedom
Multiple R-squared:  0.9899,	Adjusted R-squared:  0.989 
F-statistic:  1076 on 1 and 11 DF,  p-value: 2.525e-12
</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This kind of transformation doesn't  help us a lot. R^(2) adjusted stays the same.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[200]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>predict<span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> time <span class="p">,</span> data <span class="o">=</span> w_r<span class="p">),</span> <span class="kt">data.frame</span><span class="p">(</span>time<span class="o">=</span><span class="m">8</span><span class="p">)</span> <span class="p">,</span>interval <span class="o">=</span><span class="s">&quot;confidence&quot;</span><span class="p">,</span> level<span class="o">=</span><span class="m">0.95</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>fit</th><th scope=col>lwr</th><th scope=col>upr</th></tr></thead>
<tbody>
	<tr><th scope=row>1</th><td>0.5254245</td><td>0.4181291</td><td>0.6327199</td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here we have done  confidence intervall of the proportion of items correctly recalled after 8 days
for our untransformed model. Now we want to do it for every our model and compare their confidence intervals.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[202]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>predict<span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> time <span class="o">+</span> <span class="m">1</span><span class="o">/</span>time<span class="p">,</span> data <span class="o">=</span> w_r<span class="p">),</span> <span class="kt">data.frame</span><span class="p">(</span>time<span class="o">=</span><span class="m">8</span><span class="p">)</span> <span class="p">,</span>interval <span class="o">=</span><span class="s">&quot;confidence&quot;</span><span class="p">,</span> level<span class="o">=</span><span class="m">0.95</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>fit</th><th scope=col>lwr</th><th scope=col>upr</th></tr></thead>
<tbody>
	<tr><th scope=row>1</th><td>0.5254245</td><td>0.4181291</td><td>0.6327199</td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[203]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>predict<span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> <span class="kp">log</span><span class="p">(</span>time<span class="p">)</span> <span class="p">,</span> data <span class="o">=</span> w_r<span class="p">),</span> <span class="kt">data.frame</span><span class="p">(</span>time<span class="o">=</span><span class="m">8</span><span class="p">)</span> <span class="p">,</span>interval <span class="o">=</span><span class="s">&quot;confidence&quot;</span><span class="p">,</span> level<span class="o">=</span><span class="m">0.95</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>fit</th><th scope=col>lwr</th><th scope=col>upr</th></tr></thead>
<tbody>
	<tr><th scope=row>1</th><td>0.6816677</td><td>0.6596709</td><td>0.7036645</td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>And as we see here our Confidence Interval is much smaller in compare to untrasformed models.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[205]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-r"><pre><span></span>predict<span class="p">(</span>lm<span class="p">(</span>prop <span class="o">~</span> <span class="kp">log</span><span class="p">(</span>time<span class="p">)</span> <span class="o">+</span> <span class="m">1</span><span class="o">/</span>time <span class="p">,</span> data <span class="o">=</span> w_r<span class="p">),</span> <span class="kt">data.frame</span><span class="p">(</span>time<span class="o">=</span><span class="m">8</span><span class="p">)</span> <span class="p">,</span>interval <span class="o">=</span><span class="s">&quot;confidence&quot;</span><span class="p">,</span> level<span class="o">=</span><span class="m">0.95</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<table>
<thead><tr><th></th><th scope=col>fit</th><th scope=col>lwr</th><th scope=col>upr</th></tr></thead>
<tbody>
	<tr><th scope=row>1</th><td>0.6816677</td><td>0.6596709</td><td>0.7036645</td></tr>
</tbody>
</table>

</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The same Confidence Interval.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>

   
