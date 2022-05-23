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
$$ u (-b^* ) + \gamma^2 \left[ (1-\alpha \beta) u(a) - \alpha \beta u(f) \right]  =u ( -c_b) + \gamma^2 \left[ (1-\alpha \beta) u(b^*) - \alpha \beta u(f) \right] = 0 .$$
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
        <td>\( - u(rf) ; - u(rf) \)</td>
        <td>\(  - u(Rf) ; - u(f )\)</td>
    </tr>
    <tr>
        <td>Not Report</td>
        <td>\( - u(f); - u(Rf) \)</td>
        <td>\(  \gamma^2 \left[ (1-\alpha \beta) u(a )- \alpha \beta u(f )\right]  ;  \gamma^2 \left[ (1-\alpha \beta) u(b )- \alpha \beta u(f )\right]  \)</td>
    </tr>
</table>

<p>	
	
	Agents report befor being detectd if:
<p>
	$$ -u(R_if)  \geq \gamma^2 \left[ (1-\alpha \beta) ~ u(\pi_j )- \alpha \beta ~ u(f) \right],$$ 
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
        <td>\( - u(pf) ; - u(pf) \)</td>
        <td>\(  - u(Pf) ; - u(f )\)</td>
    </tr>
    <tr>
        <td>Not Admit</td>
        <td>\( - u(f); - u(Pf) \)</td>
        <td>\(  \gamma \left[ (1-\beta) u(a) - \beta u(f) \right]  ;  \gamma \left[ (1-\beta) u(b) -  \beta u(f) \right]  \)</td>
    </tr>
</table>
	
<p>
	Notably, the agents admit guilty if,
<p>
	$$
	 -u(P_if) \geq \gamma \left[ (1-\beta) ~u(\pi_j) - \beta ~u(f) \right].
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
    
      
        
          
          
            
              <div class="bk-root" id="30b399d4-2c31-4f82-bf04-b6e6ce9542f3" data-root-id="1366"></div>
            
          
        
      
      
        <script type="application/json" id="1521">
          {"9148ae12-d2cc-4355-b5cc-7ecfdac6b78f":{"defs":[],"roots":{"references":[{"attributes":{},"id":"1277","type":"AllLabels"},{"attributes":{"end":2,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":0.001,"step":0.01,"title":"Risk Aversion (eta)","value":0.001},"id":"1362","type":"Slider"},{"attributes":{},"id":"1278","type":"BasicTickFormatter"},{"attributes":{"args":{"P":{"id":"1360"},"R":{"id":"1359"},"a":{"id":"1357"},"c_b":{"id":"1358"},"checkbox":{"id":"1355"},"eta":{"id":"1362"},"f":{"id":"1356"},"gamma":{"id":"1361"},"source":{"id":"1235"}},"code":"\n\n\nfunction u(z,eta)\n{\n    return (1-(2.718281828459045**(-eta*z)))/eta;\n};\n\nfunction get_b_star(gamma,alpha,beta,c,a,f,eta)\n{\n    return (((gamma**2)*((1-alpha*beta)*a-alpha*beta*f)) + ((gamma*gamma*alpha*beta*f+c)/((gamma*gamma)*(1-alpha*beta))))/2 ;\n};\n\nfunction get_y_payer(gamma,alpha,beta,f,c,a)\n{\n    return   (gamma**2)*((1-alpha*beta)*u((-get_b_star(gamma,alpha,beta,c,a,f,eta)/(gamma**2)) + a + (f/(gamma**2)),eta) + alpha*beta*u(0,eta));\n};\n\nfunction alpha_solver(beta,j,gamma,a,c,f,eta)\n{ \n    var alpha = 0 ;\n    while ( get_y_payer(gamma,alpha,beta,f,c,a) &gt; u(f,eta) )\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction R_payer_solver(beta, j ,gamma,a,c,f,R,eta)\n{ \n    var alpha = 0 ;\n    while ((gamma**2)*((1-alpha*beta)*u((get_b_star(gamma,alpha,beta,c,a,f,eta)/gamma**2) + (f/(gamma**2)), eta ) + alpha*beta*u(0,eta))  &gt;  u((-R*f)+f,eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction P_payer_solver(beta, j ,gamma,a,c,f,P,eta)\n{ \n    var alpha = 0 ;\n    while  (gamma*((1-beta)*u((get_b_star(gamma,alpha,beta,c,a,f,eta)/gamma) + (f/(gamma)), eta ) + beta*u(0,eta)) &gt; u((-P*f)+f,eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction R_receiver_solver(beta, j ,gamma,a,c,f,R,eta)\n{ \n    var alpha = 0 ;\n    while ((gamma**2)*((1-alpha*beta)*u(a+(f/(gamma**2)),eta) + alpha*beta*u(0,eta))  &gt;  u((-R*f)+f,eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\nfunction P_receiver_solver(beta, j ,gamma,a,c,f,P,eta)\n{ \n    var alpha = 0 ;\n    while (gamma*((1-beta)*u(a+(f/(gamma)),eta) + beta*u(0,eta)) &gt; u((-P*f)+f,eta))\n        {\n        alpha += 1/j;\n        if (alpha &gt; 1.01) \n            {\n            break ;\n            }\n        }\n    return alpha; \n};\n\n    console.log('log =' + cb_obj.active, cb_obj.toString(), cb_obj.value)\n    var data = source.data;\n    var checkbox = checkbox.active;\n    var j = 400\n    var f = f.value;\n    var c_b = c_b.value;\n    var a = a.value;\n    var R = R.value;\n    var P = P.value;\n    var eta = eta.value;\n    var gamma = gamma.value;\n    const x = data['x']\n    const y = data['y']\n    const z = data['z']\n    const l = data['l']\n    const m = data['m']\n    const n = data['n']\n    const o = data['o']\n    const alpha = data['alpha']\n    const b = data['b']\n\n    if (checkbox==0){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = alpha_solver(x[i],j,gamma,a,c_b,f,eta);\n        l[i] = 0;\n        m[i] = 0;\n        n[i] = 0;\n        o[i] = 0;\n         } }\n    if (checkbox==1){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = alpha_solver(x[i],j,gamma,a,c_b,f,eta);\n        l[i] = R_payer_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        m[i] = P_payer_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n        n[i] = 0;\n        o[i] = 0;\n         } }\n    if (checkbox==2){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = 0;\n        l[i] = 0;\n        m[i] = 0;\n        n[i] = R_receiver_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        o[i] = P_receiver_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n         } }\n    if (checkbox==3){\n      for (var i = 0; i &lt; x.length; i++) {\n        y[i] = alpha_solver(x[i],j,gamma,a,c_b,f,eta);\n        l[i] = R_payer_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        m[i] = P_payer_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n        n[i] = R_receiver_solver(x[i], j ,gamma,a,c_b,f,R,eta);\n        o[i] = P_receiver_solver(x[i], j ,gamma,a,c_b,f,P,eta);\n         } }\n   source.change.emit();\n\n"},"id":"1363","type":"CustomJS"},{"attributes":{},"id":"1282","type":"Selection"},{"attributes":{},"id":"1283","type":"UnionRenderers"},{"attributes":{"items":[{"id":"1286"},{"id":"1303"},{"id":"1320"},{"id":"1337"},{"id":"1354"}]},"id":"1285","type":"Legend"},{"attributes":{"label":{"value":"Incentive Constraint"},"renderers":[{"id":"1272"}]},"id":"1286","type":"LegendItem"},{"attributes":{"label":{"value":"Payer's self reporting Constraint"},"renderers":[{"id":"1290"}]},"id":"1303","type":"LegendItem"},{"attributes":{"data_source":{"id":"1235"},"glyph":{"id":"1288"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"1289"},"view":{"id":"1291"}},"id":"1290","type":"GlyphRenderer"},{"attributes":{"line_alpha":0.1,"line_color":"steelblue","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"l"}},"id":"1289","type":"Line"},{"attributes":{"line_color":"steelblue","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"l"}},"id":"1288","type":"Line"},{"attributes":{},"id":"1237","type":"Range1d"},{"attributes":{"source":{"id":"1235"}},"id":"1291","type":"CDSView"},{"attributes":{},"id":"1239","type":"Range1d"},{"attributes":{"children":[{"id":"1364"},{"id":"1365"}]},"id":"1366","type":"Row"},{"attributes":{},"id":"1241","type":"LinearScale"},{"attributes":{"data":{"l":{"__ndarray__":"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","dtype":"float64","order":"little","shape":[300]},"m":{"__ndarray__":"GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/","dtype":"float64","order":"little","shape":[300]},"n":{"__ndarray__":"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","dtype":"float64","order":"little","shape":[300]},"o":{"__ndarray__":"GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/GFyPwvUo8D8YXI/C9SjwPxhcj8L1KPA/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/TxvotIFOa79PG+i0gU5rv08b6LSBTmu/","dtype":"float64","order":"little","shape":[300]},"x":{"__ndarray__":"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","dtype":"float64","order":"little","shape":[300]},"y":{"__ndarray__":"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","dtype":"float64","order":"little","shape":[300]}},"selected":{"id":"1282"},"selection_policy":{"id":"1283"}},"id":"1235","type":"ColumnDataSource"},{"attributes":{"label":{"value":"Payer's Plea Agreement Constraint"},"renderers":[{"id":"1307"}]},"id":"1320","type":"LegendItem"},{"attributes":{"data_source":{"id":"1235"},"glyph":{"id":"1305"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"1306"},"view":{"id":"1308"}},"id":"1307","type":"GlyphRenderer"},{"attributes":{},"id":"1243","type":"LinearScale"},{"attributes":{"axis_label":"Probability of Conviction \ud835\udefd","formatter":{"id":"1278"},"major_label_policy":{"id":"1277"},"ticker":{"id":"1246"}},"id":"1245","type":"LinearAxis"},{"attributes":{"line_alpha":0.1,"line_color":"blue","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"m"}},"id":"1306","type":"Line"},{"attributes":{"line_color":"blue","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"m"}},"id":"1305","type":"Line"},{"attributes":{},"id":"1246","type":"BasicTicker"},{"attributes":{"source":{"id":"1235"}},"id":"1308","type":"CDSView"},{"attributes":{"axis":{"id":"1245"},"ticker":null},"id":"1248","type":"Grid"},{"attributes":{"children":[{"id":"1236"}]},"id":"1364","type":"Column"},{"attributes":{"axis_label":"Probability of Detection \ud835\udefc","formatter":{"id":"1281"},"major_label_policy":{"id":"1280"},"ticker":{"id":"1250"}},"id":"1249","type":"LinearAxis"},{"attributes":{"label":{"value":"Receiver's self reporting Constraint"},"renderers":[{"id":"1324"}]},"id":"1337","type":"LegendItem"},{"attributes":{},"id":"1250","type":"BasicTicker"},{"attributes":{"data_source":{"id":"1235"},"glyph":{"id":"1322"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"1323"},"view":{"id":"1325"}},"id":"1324","type":"GlyphRenderer"},{"attributes":{"axis":{"id":"1249"},"dimension":1,"ticker":null},"id":"1252","type":"Grid"},{"attributes":{"data_source":{"id":"1235"},"glyph":{"id":"1270"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"1271"},"view":{"id":"1273"}},"id":"1272","type":"GlyphRenderer"},{"attributes":{"line_alpha":0.1,"line_color":"gold","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"n"}},"id":"1323","type":"Line"},{"attributes":{"below":[{"id":"1245"}],"center":[{"id":"1248"},{"id":"1252"},{"id":"1285"}],"height":500,"left":[{"id":"1249"}],"renderers":[{"id":"1272"},{"id":"1290"},{"id":"1307"},{"id":"1324"},{"id":"1341"}],"title":{"id":"1275"},"toolbar":{"id":"1261"},"toolbar_location":"below","width":500,"x_range":{"id":"1237"},"x_scale":{"id":"1241"},"y_range":{"id":"1239"},"y_scale":{"id":"1243"}},"id":"1236","subtype":"Figure","type":"Plot"},{"attributes":{},"id":"1275","type":"Title"},{"attributes":{"line_color":"gold","line_dash":[6],"line_width":3,"x":{"field":"x"},"y":{"field":"n"}},"id":"1322","type":"Line"},{"attributes":{"source":{"id":"1235"}},"id":"1325","type":"CDSView"},{"attributes":{},"id":"1253","type":"PanTool"},{"attributes":{"active":3,"js_property_callbacks":{"change:active":[{"id":"1363"}]},"labels":["Show the Corruption Constraint","Show Payer's Policy Constraints","Show Receivers's Policy Constraints","Show all curves"],"width":500},"id":"1355","type":"RadioGroup"},{"attributes":{"children":[{"id":"1355"},{"id":"1356"},{"id":"1358"},{"id":"1357"},{"id":"1359"},{"id":"1360"},{"id":"1361"},{"id":"1362"}]},"id":"1365","type":"Column"},{"attributes":{},"id":"1254","type":"WheelZoomTool"},{"attributes":{"data_source":{"id":"1235"},"glyph":{"id":"1339"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"1340"},"view":{"id":"1342"}},"id":"1341","type":"GlyphRenderer"},{"attributes":{"overlay":{"id":"1259"}},"id":"1255","type":"BoxZoomTool"},{"attributes":{},"id":"1256","type":"SaveTool"},{"attributes":{"line_alpha":0.1,"line_color":"darkorange","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"o"}},"id":"1340","type":"Line"},{"attributes":{"line_color":"darkorange","line_dash":[2,4],"line_width":3,"x":{"field":"x"},"y":{"field":"o"}},"id":"1339","type":"Line"},{"attributes":{},"id":"1257","type":"ResetTool"},{"attributes":{},"id":"1258","type":"HelpTool"},{"attributes":{"source":{"id":"1235"}},"id":"1342","type":"CDSView"},{"attributes":{"label":{"value":"Receiver's Plea Agreement Constraint"},"renderers":[{"id":"1341"}]},"id":"1354","type":"LegendItem"},{"attributes":{},"id":"1281","type":"BasicTickFormatter"},{"attributes":{},"id":"1280","type":"AllLabels"},{"attributes":{"end":50,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":1,"title":"Fine (f)","value":20},"id":"1356","type":"Slider"},{"attributes":{"end":50,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":1,"title":"Payer's Advantage (a)","value":10},"id":"1357","type":"Slider"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"right_units":"screen","syncable":false,"top_units":"screen"},"id":"1259","type":"BoxAnnotation"},{"attributes":{"end":1,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":0,"step":0.01,"title":"Time discount (gamma)","value":0.9},"id":"1361","type":"Slider"},{"attributes":{"callback":null,"tooltips":[["(\ud835\udefd,\ud835\udefc)","($x, $y)"]]},"id":"1260","type":"HoverTool"},{"attributes":{"active_multi":null,"tools":[{"id":"1253"},{"id":"1254"},{"id":"1255"},{"id":"1256"},{"id":"1257"},{"id":"1258"},{"id":"1260"}]},"id":"1261","type":"Toolbar"},{"attributes":{"end":20,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":0,"title":"Recipient's Cost (c_b)","value":1},"id":"1358","type":"Slider"},{"attributes":{"end":1,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":-1,"step":0.01,"title":"Fine Reduction for Self-Reporting Before Detection (R)","value":-0.1},"id":"1359","type":"Slider"},{"attributes":{"line_alpha":0.6,"line_color":"darkgreen","line_width":3,"x":{"field":"x"},"y":{"field":"y"}},"id":"1270","type":"Line"},{"attributes":{"line_alpha":0.1,"line_color":"darkgreen","line_width":3,"x":{"field":"x"},"y":{"field":"y"}},"id":"1271","type":"Line"},{"attributes":{"end":1,"js_property_callbacks":{"change:value":[{"id":"1363"}]},"start":-1,"step":0.01,"title":"Fine Reduction for Self-Reporting After Detection (P)","value":0.6},"id":"1360","type":"Slider"},{"attributes":{"source":{"id":"1235"}},"id":"1273","type":"CDSView"}],"root_ids":["1366"]},"title":"Bokeh Application","version":"2.3.3"}}
        </script>
        <script type="text/javascript">
          (function() {
            var fn = function() {
              Bokeh.safely(function() {
                (function(root) {
                  function embed_document(root) {
                    
                  var docs_json = document.getElementById('1521').textContent;
                  var render_items = [{"docid":"9148ae12-d2cc-4355-b5cc-7ecfdac6b78f","root_ids":["1366"],"roots":{"1366":"30b399d4-2c31-4f82-bf04-b6e6ce9542f3"}}];
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
