# Correlation & Causality: Confounders, Colliders and the Limits of Controls

## Objective
I tested when adding control variables to a regression recovers a causal effect and when it introduces bias.

## Methodology
- I simulated three worlds (true causation, pure confounding and pure selection) in which the correlation between the two main variables is near 0.65, while the true effects are 2.0, 0.0 and 0.0.
- I drew a confounder, a collider and a mediator as directed graphs with networkx.
- I estimated the treatment effect with and without each type of control to compare the results with the known true effect.
- I built an M-bias structure in which a control measured before treatment still opens a biasing path.
- I wrote a function, `coef_on_d()`, that returns the coefficient on the treatment for any list of controls, and used it to show that also controlling for one of the hidden causes (u1) closes the path again.
- I reproduced the LaLonde (1986) contrast, comparing the randomised experiment with a comparison group drawn from the CPS, and measured how much of the gap covariate adjustment closes.

## Key Findings
- The correlations in the three worlds were [YOUR VALUE], [YOUR VALUE] and [YOUR VALUE], although only the first world has a causal effect. Correlation alone did not tell the worlds apart.
- Controlling for the confounder recovered the true effect.
- Controlling for the collider gave [YOUR VALUE] where the truth is 0, a large and highly significant association between two independent variables.
- In the M-bias structure, the pre-treatment control gave [YOUR VALUE]. Adding u1 as a control gave [YOUR VALUE]. A control measured before treatment can still bias the estimate.
- LaLonde: the experimental estimate was $[YOUR VALUE], the naive CPS estimate was $[YOUR VALUE], and the estimate with controls was $[YOUR VALUE]. Covariate adjustment closed [YOUR VALUE]% of the gap.
