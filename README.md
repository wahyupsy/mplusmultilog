# mplusmultilog

<h1>Mplus vs Multilog in 2PL IRT</h1>

<p>&nbsp;</p>

<p><span style="color:#000000">This is an example result of IRT analysis&nbsp;using MPLUS&nbsp;and Multilog. &nbsp;</span></p>

<h2><span style="color:#0000a0">DATASET</span></h2>

<p>1. MPLUS Syntax&nbsp;&amp; Output</p>

<p><a href="http://elisa1.ugm.ac.id/files/wahyu_psy/lb9iBryP/lsat-mplus.dat">lsat-mplus.dat</a>&nbsp;| <a href="http://elisa1.ugm.ac.id/files/wahyu_psy/lb9iBryP/lsat-multilog.MLG">lsat-multilog.MLG</a></p>

<p>2. MULTILOG&nbsp; Syntax&nbsp;&amp; Output<br />
<a href="http://elisa1.ugm.ac.id/files/wahyu_psy/lb9iBryP/lsat-multilog.dat">lsat-multilog.dat</a>&nbsp;| <a href="http://elisa1.ugm.ac.id/files/wahyu_psy/lb9iBryP/lsatmplus.inp">lsatmplus.inp</a></p>

<h2>&nbsp;</h2>

<h2><span style="color:#0000a0">MPLUS</span></h2>

<h4>MPLUS SYNTAX</h4>

<pre>
TITLE:&nbsp; Analisis Teori Respons Butir MPLUS (GRM)&nbsp; 
DATA:&nbsp;&nbsp; FILE IS lsat-mplus.dat; 
VARIABLE:&nbsp;&nbsp; NAMES ARE a01-a05 freq;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; FREQWEIGHT IS freq; 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MISSING ARE ALL (-9);
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; USEVARIABLE ARE a01-a05;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; CATEGORICAL ARE a01-a05;
ANALYSIS:&nbsp;&nbsp; ESTIMATOR IS ML; 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; LINK IS LOGIT;&nbsp; 
MODEL:&nbsp;&nbsp; 
F1 BY a01-a05*;
!F1 BY <a href="mailto:a01@1">a01@1</a> a02-a05;
&nbsp;&nbsp;&nbsp; [a01$1-a05$1*]
[F1@0]; <a href="mailto:F1@1">F1@1</a>;
OUTPUT:&nbsp;&nbsp;&nbsp;&nbsp; STAND; 
PLOT:&nbsp;&nbsp; TYPE IS PLOT1; ! Perintah Plot untuk deskriptif
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TYPE IS PLOT2; ! Perintah Plot untuk kurva IRT
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TYPE IS PLOT3; ! Perintah Plot untuk nilai theta</pre>

<pre>
&nbsp;</pre>

<h4>MPLUS OUTPUT.</h4>

<pre>
MODEL RESULTS</pre>

<pre>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Two-Tailed
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Estimate&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S.E.&nbsp; Est./S.E.&nbsp;&nbsp;&nbsp; P-Value</pre>

<pre>
&nbsp;F1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; BY
&nbsp;&nbsp;&nbsp; A01&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.825&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.258&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.198&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.001
&nbsp;&nbsp;&nbsp; A02&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.722&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.186&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.872&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A03&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.891&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.233&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.826&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A04&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.688&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.185&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.718&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A05&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.659&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.210&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.133&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.002</pre>

<pre>
&nbsp;Means
&nbsp;&nbsp;&nbsp; F1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp; 999.000&nbsp;&nbsp;&nbsp; 999.000</pre>

<pre>
&nbsp;Thresholds
&nbsp;&nbsp;&nbsp; A01$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -2.773&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.206&nbsp;&nbsp;&nbsp; -13.482&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A02$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -0.990&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.090&nbsp;&nbsp;&nbsp; -11.005&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A03$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -0.249&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.076&nbsp;&nbsp;&nbsp;&nbsp; -3.266&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.001
&nbsp;&nbsp;&nbsp; A04$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -1.285&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.099&nbsp;&nbsp;&nbsp; -12.977&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A05$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -2.054&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.136&nbsp;&nbsp;&nbsp; -15.148&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000</pre>

<pre>
&nbsp;Variances
&nbsp;&nbsp;&nbsp; F1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp; 999.000&nbsp;&nbsp;&nbsp; 999.000</pre>

<pre>
IRT PARAMETERIZATION IN TWO-PARAMETER LOGISTIC METRIC
WHERE THE LOGIT IS 1.7*DISCRIMINATION*(THETA - DIFFICULTY)</pre>

<pre>
&nbsp;Item Discriminations</pre>

<pre>
&nbsp;F1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; BY
&nbsp;&nbsp;&nbsp; A01&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.486&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.152&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.198&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.001
&nbsp;&nbsp;&nbsp; A02&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.425&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.110&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.872&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A03&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.524&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.137&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.826&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A04&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.405&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.109&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.718&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A05&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.387&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.124&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3.133&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.002</pre>

<pre>
&nbsp;Means
&nbsp;&nbsp;&nbsp; F1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1.000</pre>

<pre>
&nbsp;Item Difficulties
&nbsp;&nbsp;&nbsp; A01$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -3.360&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.867&nbsp;&nbsp;&nbsp;&nbsp; -3.875&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A02$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -1.371&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.308&nbsp;&nbsp;&nbsp;&nbsp; -4.455&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A03$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -0.280&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.100&nbsp;&nbsp;&nbsp;&nbsp; -2.807&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.005
&nbsp;&nbsp;&nbsp; A04$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -1.868&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.435&nbsp;&nbsp;&nbsp;&nbsp; -4.296&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000
&nbsp;&nbsp;&nbsp; A05$1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -3.119&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.868&nbsp;&nbsp;&nbsp;&nbsp; -3.595&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000</pre>

<pre>
&nbsp;Variances
&nbsp;&nbsp;&nbsp; F1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1.000</pre>

<pre>
&nbsp;</pre>

<h2><span style="color:#0000a0">MULTILOG</span></h2>

<h4>Syntax Analysis</h4>

<pre>
         

       MML PARAMETER ESTIMATION FOR THE 2PL MODEL, LSAT DATA
&gt;PROBLEM RANDOM, PATTERN, NITEMS=5, NGROUPS=1, NPATTERNS=32, 
DATA=&#39;lsat-multilog.DAT&#39;;
&gt;TEST ALL, L2;
&gt;SAVE;
&gt;END;
2
01
11111
N
(4X,5A1,F4.0)</pre>

<p>&lt; h4 align = &quot;left&quot; &gt;</p>

<pre>
&nbsp;</pre>

<h4><span style="font-family:Arial">Syntax Analysis</span></h4>

<pre>
         

       OUTPUT ANALYSIS
&nbsp;
ITEM 1: 2 GRADED CATEGORIES
P(#) ESTIMATE (S.E.)
A 1 0.82 (0.18)
B( 1) 2 -3.36 (0.62)
@THETA: INFORMATION: (Theta values increase in steps of 0.2)
-3.0 - -1.6 0.166 0.161 0.154 0.146 0.136 0.126 0.115 0.104
-1.4 - 0.0 0.094 0.084 0.074 0.065 0.057 0.050 0.043 0.038
0.2 - 1.6 0.032 0.028 0.024 0.021 0.018 0.015 0.013 0.011
1.8 - 3.0 0.009 0.008 0.007 0.006 0.005 0.004 0.004
OBSERVED AND EXPECTED COUNTS/PROPORTIONS IN
CATEGORY(K): 1 2
OBS. FREQ. 76 924
OBS. PROP. 0.0760 0.9240
EXP. PROP. 0.0760 0.9240</pre>

<pre>
         

       ITEM 2: 2 GRADED CATEGORIES
P(#) ESTIMATE (S.E.)
A 3 0.72 (0.11)
B( 1) 4 -1.37 (0.21)
@THETA: INFORMATION: (Theta values increase in steps of 0.2)
-3.0 - -1.6 0.094 0.101 0.108 0.115 0.120 0.125 0.128 0.130
-1.4 - 0.0 0.131 0.131 0.129 0.126 0.122 0.116 0.110 0.104
0.2 - 1.6 0.097 0.089 0.082 0.075 0.068 0.061 0.055 0.049
1.8 - 3.0 0.044 0.039 0.034 0.030 0.027 0.023 0.020
OBSERVED AND EXPECTED COUNTS/PROPORTIONS IN
CATEGORY(K): 1 2
OBS. FREQ. 291 709
OBS. PROP. 0.2910 0.7090
EXP. PROP. 0.2910 0.7090</pre>

<pre>
         

        &nbsp;
</pre>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p>Wahyu Widhiarso | Fakultas Psikologi UGM</p>

<p>&nbsp;</p>
