# Interactive Corruption Model

The corruption game is played by two players $i$, a $payer$ and a $receivver$.

## Constants

Let:

$b$ =  bribe;

$a$ =  Advantage from corruption or favour;

$c_b$ = Corruption cost;

$f$ = Fine;

$\alpha$ = Probability of detection;

$\beta$ = probability of conviction;

$\gamma$ = Time discount; and

$\eta$ = risk aversion constant.

It is possible to simplify the costs of corruption as $\phi_i$ and the benefits as $\pi_i$, so:

$\pi_{payer} = a$;

$\pi_{receiver} = b$;

$\phi_{payer} = b$;and

$\phi_{receiver} = c_b$.

## Payoffs

The payoffs $y$ given each possivle state $S_t$ in the game can be summarized as:



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

Therefore, the expected returns for both players is:

$$ E [y_i] = -\phi_i + \gamma^2 \left[ (1-\alpha \beta) \pi_i - \alpha \beta f \right] $$
## Calculating the Endogenous Bribe

Here, agents will enter in corruption if the proposed bribe is bigger then the expected return from corruption $E[y_i]$, or

$$
	b <  \gamma^2 \left[ (1-\alpha\beta) a - \alpha\beta f \right] 
$$
And for the $receiver$,

$$
	b > \frac{ (\gamma^2 \alpha \beta f + c_b)}{\gamma^2 (1-\alpha\beta) } 
$$

Once again, if agents have equal bargaining power, the players surplus is equally divided and the chosen bribe $b^*$ is the median of the interval from the inequations above, or 

$$
	b^*(a,c_b,\beta,\alpha,\gamma) = \left[ \frac{\gamma^2 \left[ (1-\alpha\beta) a - \alpha\beta f \right] +  \frac{ (\gamma^2 \alpha \beta f + c_b)}{\gamma^2 (1-\alpha\beta) }  } {2}   \right]
$$

## Risk Aversion

In the next examples, it is assumed that the utility function $u(.)$ is an isoelastic utility function. Also called constant relative risk aversion (CRRA) function, such that:

$$ u(x) = \begin{cases}
\frac{\displaystyle x ^{(1-\eta)} - 1 } {1-\eta} +1 \textrm{   if  } \eta \neq 1 \\
ln(x)+1\textrm{   if  } \eta = 1 \end{cases} $$

Where $\eta$ is the risk aversion parameter and $\eta > 0$ represents some degree of risk aversion.

## Insentive Compatibility Constraints

The Incentive Constraints for both player can be given as all the point in they both are indifferent between enter in bribery or not, or

$$E[y_{payer}] = E[y_{receiver}] = 0$$ , or

$$ u \left(-b^* + \gamma^2 \left[ (1-\alpha \beta) a - \alpha \beta f \right] \right) =u \left( -c_b + \gamma^2 \left[ (1-\alpha \beta) b^* - \alpha \beta f \right]\right) = 0 .$$

Notably, any pont bellow this curve, corruption is profitable for both players.

## Policy Incentive Constraints



### Self-Reporting Area

|            | Report          | Not Report       |
|------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Report     | $$ u(- rf) ; u(- rf) $$ | $$  u(- Rf) ; u(- f) $$                                                                                                                   |
| Not Report | $$ u(- f); u(- Rf) $$   | $$  \gamma^2 \left[ (1-\alpha \beta) u(a) - \alpha \beta u(f) \right]  ;  \gamma^2 \left[ (1-\alpha \beta) u(b) - \alpha \beta u(f) \right]  $$ |

Agents report befor being detectd if:

$$ -u(R_if) \geq \gamma^2 \left[ (1-\alpha \beta) ~ u(\pi_j )- \alpha \beta ~ u(f) \right],$$ 

where the subscrpit $j$ represents the other player.


### Pleaing Guilty Area

|              | Admit Guilty    | Not Admit                                                                                          |
|--------------|-----------------|----------------------------------------------------------------------------------------------------|
| Admit Guilty | $$ - u(pf) ; - u(pf) $$ | $$  - u(Pf) ; - u(f )$$                                                                                    |
| Not Admit    | $$ - u(f ); - u(Pf) $$   | $$  \gamma \left[ (1-\beta) u(a )- \beta u(f) \right]  ;  \gamma \left[ (1-\beta) u(b )-  \beta u(f) \right]  $$ |$

$$
 -u(P_if) \geq \gamma \left[ (1-\beta) ~u(\pi_j) - \beta ~u(f) \right].
$$


The interpretation from the self-reporting area and the plea bargaining area is straightforward. In the first case, for a given leniency policy $R$, if the combined probability of detection and conviction is higher than $\alpha(R^*_i)$ and $\beta(R^*_i)$, it means that it is more profitable (in expected terms) to self-report and get the bonus than it is to stay in the game. Likewise, if the agents are detected, then they will always plea guilty if the observed probability of conviction $\beta$ is higher then the threshold $\beta(P^*_i)$. Lastly, the thresholds $\alpha\beta(R^*_i)$ and $\beta(P^*_i)$ move towards the origin as $R$ and $P$ are smaller (more lenient). Therefore, more lenient sanction reduction rules from NTR decrease the non-observable corruption.
