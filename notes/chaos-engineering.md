CHAOS IN PRACTICE



To specifically address the uncertainty of distributed systems at scale, Chaos Engineering can be thought of as the facilitation of experiments to uncover systemic weaknesses.  These experiments follow four steps:

Start by defining ‘steady state’ as some measurable output of a system that indicates normal behavior.

Hypothesize that this steady state will continue in both the control group and the experimental group.

Introduce variables that reflect real world events like servers that crash, hard drives that malfunction, network connections that are severed, etc.

Try to disprove the hypothesis by looking for a difference in steady state between the control group and the experimental group.

The harder it is to disrupt the steady state, the more confidence we have in the behavior of the system.  If a weakness is uncovered, we now have a target for improvement before that behavior manifests in the system at large.

 --- [Principles of Chaos Engineering](http://www.principlesofchaos.org/)

