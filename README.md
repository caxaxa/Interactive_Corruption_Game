<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>MathJax example</title>
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
      <body>
<h1> Interactive Corruption Model     
<h4>  The corruption game is played by two players \(i\), a \(payer\) and a \(receiver\). 
<h2> 	Constants 

<h4> 
	Let:
<p>
	\(b\) =  bribe;
<p>
	\(a\)  =  Advantage from corruption or favour;
<p>
	\(c_b\)  = Corruption cost;
<p>
	\(f\)  = Fine;
<p>
	\( \alpha \)  = Probability of detection;
<p>
	\( \beta \) = probability of conviction;
<p>
	\( \gamma \)= Time discount; an
<p>
	\( \eta \) = risk aversion constant.
<p>
	It is possible to simplify the costs of corruption as \( \phi_i\) and the benefits as \( \pi_i\), so:
<p>
	\(\pi_{payer} = a\);
<p>
	\(\pi_{receiver} = b\);
<p>
	\(\phi_{payer} = b\);and
<p>
	\(\phi_{receiver} = c_b\).
<h2>
	Payoffs
<h4>
	The payoffs \(y\) given each possivle state \(S_t\) in the game can be summarized as:

<p>

	$$ y_{i,t}(S_t) = \begin{cases}
		0\textrm{   if not colluding}\\
		\pi_i \textrm{   if colluding}\\
		0\textrm{   if desisted} \\
		f\textrm{   if convicted } \\
		0 \textrm{ if acquitted } \\
		Rf \textrm{ if reported alone before detection } \\
		rf \textrm{ if reported simultaneously before detection}\\
		Pf \textrm{ if the other party admits guilty} \\
		pf \textrm{ if both parties admit guilty}
	 \end{cases}.$$
<p>
	Therefore, the expected returns for both players is:
<p>
	$$ E [y_i] = -\phi_i + \gamma^2 \left[ (1-\alpha \beta) \pi_i - \alpha \beta f \right] $$
<p>

<h2> Calculating the Endogenous Bribe
<h4>
<p>	
Here, agents will enter in corruption if the proposed bribe is bigger then the expected return from corruption \(E[y_i]\), or
<p>
$$
	b <  \gamma^2 \left[ (1-\alpha\beta) a - \alpha\beta f \right] 
$$
<p>
And for the \(receiver\),
<p>
$$
	b > \frac{ (\gamma^2 \alpha \beta f + c_b)}{\gamma^2 (1-\alpha\beta) } 
$$
<p>
Once again, if agents have equal bargaining power, the players surplus is equally divided and the chosen bribe \(b^*\) is the median of the interval from the inequations above, or 
<p>
$$
	b^*(a,c_b,\beta,\alpha,\gamma) = \left[ \frac{\gamma^2 \left[ (1-\alpha\beta) a - \alpha\beta f \right] +  \frac{ (\gamma^2 \alpha \beta f + c_b)}{\gamma^2 (1-\alpha\beta) }  } {2}   \right]
$$	
<p>		
	
<h2> Risk Aversion
<h4>
<p>
	In the next examples, it is assumed that the utility function \(u(.)\) is an isoelastic utility function. Also called constant relative risk aversion (CRRA) function, such that:
<p>
	$$ u(x) = \begin{cases}
	\frac{\displaystyle x ^{(1-\eta)} - 1 } {1-\eta} \textrm{   if  } \eta \neq 1 \\
	ln(y)\textrm{   if  } \eta = 1 \end{cases} $$
<p>
	Where $\eta$ is the risk aversion parameter and \(\eta > 0\) represents some degree of risk aversion.
<h2>
	Insentive Compatibility Constraints
<h4>
<p>
	The Incentive Constraints for both player can be given as all the point in they both are indifferent between enter in bribery or not, or
<p>
$$E[y_{payer}] = E[y_{receiver}] = 0$$ , or
<p>
$$ E[u(y_i)] = \gamma^2 \left[ (1-\alpha \beta) u\left(\pi_i + f - \frac{\phi}{\gamma^2}\right) - \alpha \beta u(0) \right] > u\left(\frac{f}{\gamma^2} + \phi\right) .$$
<p>
Notably, any pont bellow this curve, corruption is profitable for both players.
<p>	
<h2>
	Policy Incentive Constraints
<h3>
	Self-Reporting Area
<h4>


<table>
    <tr>
        <td></td>
        <td>Report</td>
        <td>Not Report</td>
    </tr>
    <tr>
        <td>Report</td>
        <td>\(  u(-rf) ;  u(-rf) \)</td>
        <td>\(  u(-Rf) ;  u(-f )\)</td>
    </tr>
    <tr>
        <td>Not Report</td>
        <td>\( u(-f); u(-Rf) \)</td>
        <td>\(  \gamma^2 \left[ (1-\alpha \beta) u\left(a + f \right) - \alpha \beta u(0) \right] ;   \gamma^2 \left[ (1-\alpha \beta) u\left(b + f \right) - \alpha \beta u(0) \right] \)</td>
    </tr>
</table>

<p>	
	
	Agents report befor being detectd if:
<p>
	$$ u\left(-R_i^*f + \frac{f}{\gamma^2}\right) \geq \gamma^2 \left[ (1-\alpha \beta) u(\pi_j + f) - \alpha \beta u(0) \right],$$ 
<p>
	where the subscrpit \(j\) represents the other player. 

<p>
<h3> Pleaing Guilty Area
<h4>	
<table>
    <tr>
        <td></td>
        <td>Admit Guilty</td>
        <td>Not Admit</td>
    </tr>
    <tr>
        <td>Admit Guilty</td>
        <td>\(  u(-pf) ;  u(-pf) \)</td>
        <td>\(  u(-Pf) ;  u(-f )\)</td>
    </tr>
    <tr>
        <td>Not Admit</td>
        <td>\( - u(f); - u(Pf) \)</td>
        <td>\(  \gamma \left[ (1-\beta) u(a + f ) - \beta u(0) \right] ; \gamma \left[ (1-\beta) u(b+ f ) - \beta u(0) \right] \)</td>
    </tr>
</table>
	
<p>
	Notably, the agents admit guilty if,
<p>
	$$
		u\left(-P_i^*f + \frac{f}{\gamma}\right) \geq \gamma \left[ (1-\beta) u(\pi_j + f ) - \beta u(0) \right].
	$$

<p>
	The interpretation from the self-reporting area and the plea bargaining area is straightforward. In the first case, for a given leniency policy \(R\), if the combined probability of detection and conviction is higher than \(\alpha(R^*_i)\) and \(\beta(R^*_i)\), it means that it is more profitable (in expected terms) to self-report and get the bonus than it is to stay in the game. Likewise, if the agents are detected, then they will always plea guilty if the observed probability of conviction \(\beta\) is higher then the threshold \(\beta(P^*_i)\). Lastly, the thresholds \(\alpha\beta(R^*_i)\) and \(\beta(P^*_i)\) move towards the origin as \(R\) and \(P\) are smaller (more lenient). Therefore, more lenient sanction reduction rules from NTR decrease the non-observable corruption.

<h1> Play With The Game!!
<h4>


<html lang="en">
  
  <head>
    
      <meta charset="utf-8">
      <title>slider.py example</title>
      
      
        
          
        
        
          
        <script type="text/javascript" src="https://cdn.bokeh.org/bokeh/release/bokeh-2.3.3.min.js" integrity="sha384-dM3QQsP+wXdHg42wTqW85BjZQdLNNIXqlPw/BgKoExPmTG7ZLML4EGqLMfqHT6ON" crossorigin="anonymous"></script>
        <script type="text/javascript" src="https://cdn.bokeh.org/bokeh/release/bokeh-widgets-2.3.3.min.js" integrity="sha384-3QTqdz9LyAm2i0sG5XTePsHec3UHWwVsrOL68SYRoAXsafvfAyqtQ+h440+qIBhS" crossorigin="anonymous"></script>
        <script type="text/javascript">
            Bokeh.set_log_level("info");
        </script>
        
      
      
    
  </head>
  
  
  <body>
    
      
        
          
          
            
              <div class="bk-root" id="de10b467-3004-44a0-8a28-e6433ba366de" data-root-id="2525"></div>
            
          
        
      
      
        <script type="application/json" id="2625">
          {"b08e3d26-82c4-4637-a2ec-381880345c4b":{"defs":[],"roots":{"references":[{"attributes":{"label":{"value":"Incentive Constraint"},"renderers":[{"id":"2431"}]},"id":"2445","type":"LegendItem"},{"attributes":{"end":20,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":0,"title":"Recipient's Cost (c_b)","value":2},"id":"2517","type":"Slider"},{"attributes":{"label":{"value":"Payer's self reporting Constraint"},"renderers":[{"id":"2449"}]},"id":"2462","type":"LegendItem"},{"attributes":{"line_color":"steelblue","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"l"}},"id":"2447","type":"Line"},{"attributes":{"source":{"id":"2394"}},"id":"2450","type":"CDSView"},{"attributes":{"data_source":{"id":"2394"},"glyph":{"id":"2447"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"2448"},"view":{"id":"2450"}},"id":"2449","type":"GlyphRenderer"},{"attributes":{"line_alpha":0.6,"line_color":"darkgreen","line_width":3,"x":{"field":"x"},"y":{"field":"y"}},"id":"2429","type":"Line"},{"attributes":{},"id":"2396","type":"Range1d"},{"attributes":{"line_alpha":0.1,"line_color":"steelblue","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"l"}},"id":"2448","type":"Line"},{"attributes":{"end":50,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":1,"title":"Payer's Advantage (a)","value":25},"id":"2516","type":"Slider"},{"attributes":{},"id":"2398","type":"Range1d"},{"attributes":{},"id":"2400","type":"LinearScale"},{"attributes":{"data":{"l":{"__ndarray__":"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","dtype":"float64","order":"little","shape":[300]},"m":{"__ndarray__":"GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/m9MGOm2gwz/rUbgeheuxP08b6LSBTms/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/","dtype":"float64","order":"little","shape":[300]},"n":{"__ndarray__":"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","dtype":"float64","order":"little","shape":[300]},"o":{"__ndarray__":"GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D9PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/","dtype":"float64","order":"little","shape":[300]},"x":{"__ndarray__":"SK+8mvLXej7IUM1kt05rPwy22oycTns/2WGns+56hD+taOEgj06LP8C3DccXEZE/Kruq/ed6lD+Uvkc0uOSXP/7B5GqITps/aMWBoVi4nj9pZA9sFBGhPx7mXYf8xaI/02esouR6pD+I6fq9zC+mPz1rSdm05Kc/8uyX9JyZqT+nbuYPhU6rP1zwNCttA60/EXKDRlW4rj/j+eiwnjawP706kL4SEbE/mHs3zIbrsT9yvN7Z+sWyP039heduoLM/Jz4t9eJ6tD8Cf9QCV1W1P9y/exDLL7Y/twAjHj8Ktz+RQcors+S3P2yCcTknv7g/RsMYR5uZuT8hBMBUD3S6P/tEZ2KDTrs/1YUOcPcovD+wxrV9awO9P4oHXYvf3b0/ZUgEmVO4vj8/iaumx5K/Pw1lKdqdNsA/egX94NejwD/npdDnERHBP1VGpO5LfsE/wuZ39YXrwT8vh0v8v1jCP5wnHwP6xcI/CsjyCTQzwz93aMYQbqDDP+QImheoDcQ/UaltHuJ6xD++SUElHOjEPyzqFCxWVcU/mYroMpDCxT8GK7w5yi/GP3PLj0AEncY/4WtjRz4Kxz9ODDdOeHfHP7usClWy5Mc/KE3eW+xRyD+W7bFiJr/IPwOOhWlgLMk/cC5ZcJqZyT/dzix31AbKP0tvAH4OdMo/uA/UhEjhyj8lsKeLgk7LP5JQe5K8u8s///BOmfYozD9tkSKgMJbMP9ox9qZqA80/R9LJraRwzT+0cp203t3NPyITcbsYS84/j7NEwlK4zj/8UxjJjCXPP2n068/Gks8/a8pfawAA0D+imslunTbQP9lqM3I6bdA/Dzudddej0D9GCwd5dNrQP3zbcHwREdE/s6vaf65H0T/qe0SDS37RPyBMrobotNE/VxwYioXr0T+N7IGNIiLSP8S865C/WNI/+4xVlFyP0j8xXb+X+cXSP2gtKZuW/NI/n/2SnjMz0z/Vzfyh0GnTPwyeZqVtoNM/Qm7QqArX0z95Pjqspw3UP7AOpK9ERNQ/5t4Ns+F61D8dr3e2frHUP1N/4bkb6NQ/ik9Lvbge1T/BH7XAVVXVP/fvHsTyi9U/LsCIx4/C1T9lkPLKLPnVP5tgXM7JL9Y/0jDG0WZm1j8IATDVA53WPz/Rmdig09Y/dqED3D0K1z+scW3f2kDXP+NB1+J3d9c/GhJB5hSu1z9Q4qrpseTXP4eyFO1OG9g/vYJ+8OtR2D/0UujziIjYPysjUvclv9g/YfO7+sL12D+YwyX+XyzZP86TjwH9Ytk/BWT5BJqZ2T88NGMIN9DZP3IEzQvUBto/qdQ2D3E92j/gpKASDnTaPxZ1Charqto/TUV0GUjh2j+DFd4c5RfbP7rlRyCCTts/8bWxIx+F2z8nhhsnvLvbP15WhSpZ8ts/lCbvLfYo3D/L9lgxk1/cPwLHwjQwltw/OJcsOM3M3D9vZ5Y7agPdP6Y3AD8HOt0/3AdqQqRw3T8T2NNFQafdP0moPUne3d0/gHinTHsU3j+3SBFQGEveP+0Ye1O1gd4/JOnkVlK43j9auU5a7+7eP5GJuF2MJd8/yFkiYSlc3z/+KYxkxpLfPzX69Wdjyd8/NeWvNQAA4D9RzWS3ThvgP2y1GTmdNuA/h53OuutR4D+jhYM8Om3gP75tOL6IiOA/2VXtP9ej4D/0PaLBJb/gPxAmV0N02uA/Kw4MxcL14D9G9sBGERHhP2LedchfLOE/fcYqSq5H4T+Yrt/L/GLhP7SWlE1LfuE/z35Jz5mZ4T/qZv5Q6LThPwZPs9I20OE/ITdoVIXr4T88Hx3W0wbiP1cH0lciIuI/c++G2XA94j+O1ztbv1jiP6m/8NwNdOI/xaelXlyP4j/gj1rgqqriP/t3D2L5xeI/F2DE40fh4j8ySHlllvziP00wLufkF+M/aRjjaDMz4z+EAJjqgU7jP5/oTGzQaeM/utAB7h6F4z/WuLZvbaDjP/Gga/G7u+M/DIkgcwrX4z8ocdX0WPLjP0NZinanDeQ/XkE/+PUo5D96KfR5RETkP5URqfuSX+Q/sPldfeF65D/M4RL/L5bkP+fJx4B+seQ/ArJ8As3M5D8dmjGEG+jkPzmC5gVqA+U/VGqbh7ge5T9vUlAJBzrlP4s6BYtVVeU/piK6DKRw5T/BCm+O8ovlP93yIxBBp+U/+NrYkY/C5T8Tw40T3t3lPy+rQpUs+eU/SpP3FnsU5j9le6yYyS/mP4BjYRoYS+Y/nEsWnGZm5j+3M8sdtYHmP9IbgJ8DneY/7gM1IVK45j8J7OmioNPmPyTUniTv7uY/QLxTpj0K5z9bpAgojCXnP3aMvanaQOc/knRyKylc5z+tXCetd3fnP8hE3C7Gkuc/5CyRsBSu5z//FEYyY8nnPxr9+rOx5Oc/NeWvNQAA6D9RzWS3ThvoP2y1GTmdNug/h53OuutR6D+jhYM8Om3oP75tOL6IiOg/2VXtP9ej6D/1PaLBJb/oPxAmV0N02ug/Kw4MxcL16D9H9sBGERHpP2LedchfLOk/fcYqSq5H6T+Yrt/L/GLpP7SWlE1Lfuk/z35Jz5mZ6T/qZv5Q6LTpPwZPs9I20Ok/ITdoVIXr6T88Hx3W0wbqP1gH0lciIuo/c++G2XA96j+O1ztbv1jqP6q/8NwNdOo/xaelXlyP6j/gj1rgqqrqP/t3D2L5xeo/F2DE40fh6j8ySHlllvzqP00wLufkF+s/aRjjaDMz6z+EAJjqgU7rP5/oTGzQaes/u9AB7h6F6z/WuLZvbaDrP/Gga/G7u+s/DYkgcwrX6z8ocdX0WPLrP0NZinanDew/XkE/+PUo7D96KfR5RETsP5URqfuSX+w/sPldfeF67D/M4RL/L5bsP+fJx4B+sew/ArJ8As3M7D8emjGEG+jsPzmC5gVqA+0/VGqbh7ge7T9wUlAJBzrtP4s6BYtVVe0/piK6DKRw7T/BCm+O8ovtP93yIxBBp+0/+NrYkY/C7T8Tw40T3t3tPy+rQpUs+e0/SpP3FnsU7j9le6yYyS/uP4FjYRoYS+4/nEsWnGZm7j+3M8sdtYHuP9MbgJ8Dne4/7gM1IVK47j8J7OmioNPuPyTUniTv7u4/QLxTpj0K7z9bpAgojCXvP3aMvanaQO8/knRyKylc7z+tXCetd3fvP8hE3C7Gku8/5CyRsBSu7z//FEYyY8nvPxr9+rOx5O8/","dtype":"float64","order":"little","shape":[300]},"y":{"__ndarray__":"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61G4HoXrsT8RERERERGxPxEREREREbE/ERERERERsT8RERERERGxPxEREREREbE/ERERERERsT8RERERERGxPxEREREREbE/ERERERERsT8RERERERGxPxEREREREbE/ERERERERsT830GkDnTawPzfQaQOdNrA/N9BpA502sD830GkDnTawPzfQaQOdNrA/N9BpA502sD830GkDnTawPzfQaQOdNrA/N9BpA502sD830GkDnTawPzfQaQOdNrA/N9BpA502sD+5HoXrUbiuP7kehetRuK4/uR6F61G4rj+5HoXrUbiuP7kehetRuK4/uR6F61G4rj+5HoXrUbiuP7kehetRuK4/uR6F61G4rj+5HoXrUbiuP7kehetRuK4/uR6F61G4rj+5HoXrUbiuP7kehetRuK4/BJ020GkDrT8EnTbQaQOtPwSdNtBpA60/BJ020GkDrT8EnTbQaQOtPwSdNtBpA60/BJ020GkDrT8EnTbQaQOtPwSdNtBpA60/BJ020GkDrT8EnTbQaQOtPwSdNtBpA60/BJ020GkDrT8EnTbQaQOtPwSdNtBpA60/BJ020GkDrT9PG+i0gU6rP08b6LSBTqs/TxvotIFOqz9PG+i0gU6rP08b6LSBTqs/TxvotIFOqz9PG+i0gU6rP08b6LSBTqs/TxvotIFOqz9PG+i0gU6rP08b6LSBTqs/TxvotIFOqz9PG+i0gU6rP08b6LSBTqs/TxvotIFOqz9PG+i0gU6rP08b6LSBTqs/mpmZmZmZqT+amZmZmZmpP5qZmZmZmak/","dtype":"float64","order":"little","shape":[300]}},"selected":{"id":"2442"},"selection_policy":{"id":"2441"}},"id":"2394","type":"ColumnDataSource"},{"attributes":{"label":{"value":"Payer's Plea Agreement Constraint"},"renderers":[{"id":"2466"}]},"id":"2479","type":"LegendItem"},{"attributes":{},"id":"2402","type":"LinearScale"},{"attributes":{"line_color":"blue","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"m"}},"id":"2464","type":"Line"},{"attributes":{},"id":"2435","type":"BasicTickFormatter"},{"attributes":{"axis_label":"Probability of Conviction \ud835\udefd","formatter":{"id":"2435"},"major_label_policy":{"id":"2436"},"ticker":{"id":"2405"}},"id":"2404","type":"LinearAxis"},{"attributes":{"source":{"id":"2394"}},"id":"2467","type":"CDSView"},{"attributes":{"data_source":{"id":"2394"},"glyph":{"id":"2464"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"2465"},"view":{"id":"2467"}},"id":"2466","type":"GlyphRenderer"},{"attributes":{},"id":"2405","type":"BasicTicker"},{"attributes":{"axis":{"id":"2404"},"ticker":null},"id":"2407","type":"Grid"},{"attributes":{"line_alpha":0.1,"line_color":"blue","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"m"}},"id":"2465","type":"Line"},{"attributes":{"axis_label":"Probability of Detection \ud835\udefc","formatter":{"id":"2438"},"major_label_policy":{"id":"2439"},"ticker":{"id":"2409"}},"id":"2408","type":"LinearAxis"},{"attributes":{},"id":"2409","type":"BasicTicker"},{"attributes":{"label":{"value":"Receiver's self reporting Constraint"},"renderers":[{"id":"2483"}]},"id":"2496","type":"LegendItem"},{"attributes":{"axis":{"id":"2408"},"dimension":1,"ticker":null},"id":"2411","type":"Grid"},{"attributes":{"items":[{"id":"2445"},{"id":"2462"},{"id":"2479"},{"id":"2496"},{"id":"2513"}]},"id":"2444","type":"Legend"},{"attributes":{"line_color":"gold","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"n"}},"id":"2481","type":"Line"},{"attributes":{"below":[{"id":"2404"}],"center":[{"id":"2407"},{"id":"2411"},{"id":"2444"}],"height":500,"left":[{"id":"2408"}],"renderers":[{"id":"2431"},{"id":"2449"},{"id":"2466"},{"id":"2483"},{"id":"2500"}],"title":{"id":"2434"},"toolbar":{"id":"2420"},"toolbar_location":"below","width":500,"x_range":{"id":"2396"},"x_scale":{"id":"2400"},"y_range":{"id":"2398"},"y_scale":{"id":"2402"}},"id":"2395","subtype":"Figure","type":"Plot"},{"attributes":{"source":{"id":"2394"}},"id":"2484","type":"CDSView"},{"attributes":{},"id":"2434","type":"Title"},{"attributes":{},"id":"2436","type":"AllLabels"},{"attributes":{"data_source":{"id":"2394"},"glyph":{"id":"2481"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"2482"},"view":{"id":"2484"}},"id":"2483","type":"GlyphRenderer"},{"attributes":{"label":{"value":"Receiver's Plea Agreement Constraint"},"renderers":[{"id":"2500"}]},"id":"2513","type":"LegendItem"},{"attributes":{"line_alpha":0.1,"line_color":"gold","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"n"}},"id":"2482","type":"Line"},{"attributes":{},"id":"2438","type":"BasicTickFormatter"},{"attributes":{},"id":"2412","type":"PanTool"},{"attributes":{"active":3,"js_property_callbacks":{"change:active":[{"id":"2522"}]},"labels":["Show the Corruption Constraint","Show Payer's Policy Constraints","Show Receivers's Policy Constraints","Show all curves"],"width":500},"id":"2514","type":"RadioGroup"},{"attributes":{"end":50,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":1,"title":"Fine (f)","value":25},"id":"2515","type":"Slider"},{"attributes":{},"id":"2413","type":"WheelZoomTool"},{"attributes":{"end":1,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":-1,"step":0.01,"title":"Fine Reduction for Self-Reporting Before Detection (R)","value":-0.1},"id":"2518","type":"Slider"},{"attributes":{"overlay":{"id":"2418"}},"id":"2414","type":"BoxZoomTool"},{"attributes":{"line_color":"darkorange","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"o"}},"id":"2498","type":"Line"},{"attributes":{},"id":"2415","type":"SaveTool"},{"attributes":{"source":{"id":"2394"}},"id":"2501","type":"CDSView"},{"attributes":{},"id":"2416","type":"ResetTool"},{"attributes":{"data_source":{"id":"2394"},"glyph":{"id":"2498"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"2499"},"view":{"id":"2501"}},"id":"2500","type":"GlyphRenderer"},{"attributes":{},"id":"2417","type":"HelpTool"},{"attributes":{"line_alpha":0.1,"line_color":"darkorange","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"o"}},"id":"2499","type":"Line"},{"attributes":{"end":1,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":-1,"step":0.01,"title":"Fine Reduction for Self-Reporting After Detection (P)","value":0.6},"id":"2519","type":"Slider"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"right_units":"screen","syncable":false,"top_units":"screen"},"id":"2418","type":"BoxAnnotation"},{"attributes":{"end":1,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":0,"step":0.01,"title":"Time discount (gamma)","value":0.95},"id":"2520","type":"Slider"},{"attributes":{"callback":null,"tooltips":[["(\ud835\udefd,\ud835\udefc)","($x, $y)"]]},"id":"2419","type":"HoverTool"},{"attributes":{"end":2,"js_property_callbacks":{"change:value":[{"id":"2522"}]},"start":0.001,"step":0.01,"title":"Risk Aversion (eta)","value":0.001},"id":"2521","type":"Slider"},{"attributes":{"active_multi":null,"tools":[{"id":"2412"},{"id":"2413"},{"id":"2414"},{"id":"2415"},{"id":"2416"},{"id":"2417"},{"id":"2419"}]},"id":"2420","type":"Toolbar"},{"attributes":{"args":{"P":{"id":"2519"},"R":{"id":"2518"},"a":{"id":"2516"},"c_b":{"id":"2517"},"checkbox":{"id":"2514"},"eta":{"id":"2521"},"f":{"id":"2515"},"gamma":{"id":"2520"},"source":{"id":"2394"}},"code":"\n\n\nfunction u(z,eta)\n{\n    return ((z**(1-eta))-1)/(1-eta);\n};\n\nfunction get_b_star(gamma,alpha,beta,c,a,f,eta)\n{\n    return (((gamma**2)*((1-alpha*beta)*a-alpha*beta*f)) + ((gamma*gamma*alpha*beta*f+c)/((gamma*gamma)*(1-alpha*beta))))/2 ;\n};\n\nfunction get_u_y_receiver(gamma,alpha,beta,f,c,a)\n{\n    return   (gamma**2)*((1-alpha*beta)*u((-c/(gamma**2)) + get_b_star(gamma,alpha,beta,c,a,f,eta) + f,eta) + alpha*beta*u(0,eta));\n};\n\nfunction alpha_solver(beta,j,gamma,a,c,f,eta)\n{ \n    var alpha = 0 ;\n    while ( get_u_y_receiver(gamma,alpha,beta,f,c,a) &gt; u((f/(gamma**2)) + c ,eta) )\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction R_payer_solver(beta, j ,gamma,a,c,f,R,eta)\n{ \n    var alpha = 0 ;\n    while ((gamma**2)*((1-alpha*beta)*u((get_b_star(gamma,alpha,beta,c,a,f,eta)/gamma**2) + f, eta ) + alpha*beta*u(0,eta))  &gt;  u((-R*f)+(f/(gamma**2)),eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction P_payer_solver(beta, j ,gamma,a,c,f,P,eta)\n{ \n    var alpha = 0 ;\n    while  (gamma*((1-beta)*u((get_b_star(gamma,alpha,beta,c,a,f,eta)/gamma) +f, eta ) + beta*u(0,eta)) &gt; u((-P*f)+(f/gamma),eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction R_receiver_solver(beta, j ,gamma,a,c,f,R,eta)\n{ \n    var alpha = 0 ;\n    while ((gamma**2)*((1-alpha*beta)*u(a+f,eta) + alpha*beta*u(0,eta))  &gt;  u((-R*f)+(f/(gamma**2)),eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction P_receiver_solver(beta, j ,gamma,a,c,f,P,eta)\n{ \n    var alpha = 0 ;\n    while (gamma*((1-beta)*u(a+f,eta) + beta*u(0,eta)) &gt; u((-P*f)+(f/(gamma)),eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\n    console.log('log =' + cb_obj.active, cb_obj.toString(), cb_obj.value)\n    var data = source.data;\n    var checkbox = checkbox.active;\n    var j = 400\n    var f = f.value;\n    var c_b = c_b.value;\n    var a = a.value;\n    var R = R.value;\n    var P = P.value;\n    var eta = eta.value;\n    var gamma = gamma.value;\n    const x = data['x']\n    const y = data['y']\n    const z = data['z']\n    const l = data['l']\n    const m = data['m']\n    const n = data['n']\n    const o = data['o']\n    const alpha = data['alpha']\n    const b = data['b']\n\n    if (checkbox==0){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = alpha_solver(x[i],j,gamma,a,c_b,f,eta);\n        l[i] = 0;\n        m[i] = 0;\n        n[i] = 0;\n        o[i] = 0;\n         } }\n    if (checkbox==1){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = alpha_solver(x[i],j,gamma,a,c_b,f,eta);\n        l[i] = R_payer_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        m[i] = P_payer_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n        n[i] = 0;\n        o[i] = 0;\n         } }\n    if (checkbox==2){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = 0;\n        l[i] = 0;\n        m[i] = 0;\n        n[i] = R_receiver_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        o[i] = P_receiver_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n         } }\n    if (checkbox==3){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = alpha_solver(x[i],j,gamma,a,c_b,f,eta);\n        l[i] = R_payer_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        m[i] = P_payer_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n        n[i] = R_receiver_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        o[i] = P_receiver_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n         } }\n   source.change.emit();\n\n"},"id":"2522","type":"CustomJS"},{"attributes":{"source":{"id":"2394"}},"id":"2432","type":"CDSView"},{"attributes":{"children":[{"id":"2395"}]},"id":"2523","type":"Column"},{"attributes":{"data_source":{"id":"2394"},"glyph":{"id":"2429"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"2430"},"view":{"id":"2432"}},"id":"2431","type":"GlyphRenderer"},{"attributes":{"line_alpha":0.1,"line_color":"darkgreen","line_width":3,"x":{"field":"x"},"y":{"field":"y"}},"id":"2430","type":"Line"},{"attributes":{"children":[{"id":"2514"},{"id":"2515"},{"id":"2517"},{"id":"2516"},{"id":"2518"},{"id":"2519"},{"id":"2520"},{"id":"2521"}]},"id":"2524","type":"Column"},{"attributes":{},"id":"2439","type":"AllLabels"},{"attributes":{"children":[{"id":"2523"},{"id":"2524"}]},"id":"2525","type":"Row"},{"attributes":{},"id":"2441","type":"UnionRenderers"},{"attributes":{},"id":"2442","type":"Selection"}],"root_ids":["2525"]},"title":"Bokeh Application","version":"2.3.3"}}
        </script>
        <script type="text/javascript">
          (function() {
            var fn = function() {
              Bokeh.safely(function() {
                (function(root) {
                  function embed_document(root) {
                    
                  var docs_json = document.getElementById('2625').textContent;
                  var render_items = [{"docid":"b08e3d26-82c4-4637-a2ec-381880345c4b","root_ids":["2525"],"roots":{"2525":"de10b467-3004-44a0-8a28-e6433ba366de"}}];
                  root.Bokeh.embed.embed_items(docs_json, render_items);
                
                  }
                  if (root.Bokeh !== undefined) {
                    embed_document(root);
                  } else {
                    var attempts = 0;
                    var timer = setInterval(function(root) {
                      if (root.Bokeh !== undefined) {
                        clearInterval(timer);
                        embed_document(root);
                      } else {
                        attempts++;
                        if (attempts > 100) {
                          clearInterval(timer);
                          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
                        }
                      }
                    }, 10, root)
                  }
                })(window);
              });
            };
            if (document.readyState != "loading") fn();
            else document.addEventListener("DOMContentLoaded", fn);
          })();
        </script>
    
  </body>
  
</html>
