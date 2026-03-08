---
title: "Design of a Technique for Analyzing Linear Time-Invariant Systems with Time-Varying Parameters Using Laplace Transform"
permalink: /coursework/MTH101_Project/
author_profile: true
---

# Design of a Technique for Analyzing Linear Time-Invariant Systems with Time-Varying Parameters Using Laplace Transform

**Team:** Junhan Chen, Shengda Gao, Yiwen Wang, Yulin Xia, Yang Tian, Siyuan Lin  
**Course:** MTH101 Engineering Mathematics  
**Institution:** Xi'an Jiaotong-Liverpool University  
**Date:** Oct 2024 – Dec 2024

---

# Background

Linear Time-Invariant (LTI) systems are widely used in engineering fields such as control systems, signal processing, and communications. Traditional analysis methods typically assume constant system parameters. In practice, however, many physical systems contain parameters that vary with time due to environmental disturbances or internal system dynamics.

Examples include variations in stiffness, damping coefficients, or system mass in mechanical systems. These variations make classical LTI analysis less suitable for modelling real dynamic behaviour. Extending analytical tools to handle time-varying parameters therefore becomes an important problem in engineering system analysis. :contentReference[oaicite:0]{index=0}

---

# Description of the Model

The Laplace Transform is a fundamental mathematical tool used to convert time-domain differential equations into algebraic equations in the frequency domain. This transformation greatly simplifies the analysis of many engineering systems.

To analyse systems with time-varying parameters, the classical transform framework can be extended through the introduction of a **Modified Laplace Transform (MLT)**. By incorporating a correction factor, the transform method becomes capable of handling differential equations whose coefficients vary with time. :contentReference[oaicite:1]{index=1}

---

# Classical Laplace Transform

For a time-domain function \( f(t) \), the Laplace Transform is defined as

\[
F(s) = \int_{0}^{\infty} f(t)e^{-st} dt
\]

where  

- \( t \) represents time  
- \( s = \sigma + j\omega \) is a complex variable  

This transformation converts differential equations into algebraic expressions in the frequency domain, making it easier to analyse system behaviour.

---

# Modified Laplace Transform (MLT)

To extend the Laplace transform framework to systems with time-varying parameters, a Modified Laplace Transform formulation is introduced.

Applying the Laplace transform to the governing equation leads to an expression that can be simplified to the form

\[
\frac{dY(s)}{ds} + \frac{4s-3}{s(s-1)}Y(s) = \frac{3y(0)}{s(s-1)}
\]

An integrating factor is introduced

\[
\mu(s) = s^3 (s-1)
\]

Multiplying the equation by this factor allows the system equation to be integrated and solved in the frequency domain. Finally, the inverse transform is applied to obtain the time-domain response of the system. :contentReference[oaicite:2]{index=2}

This approach enables differential equations with **time-varying coefficients** to be analysed using a transform-based method.

---

# Case Study: Spring–Mass–Damper System

To illustrate the modelling framework, the method is applied to a **spring–mass–damper system with time-varying parameters**.

<img src="/images/SpringMassDamperSystem.png" width="550">

The dynamic behaviour of the system can be described by the differential equation

\[
F(t) = m\frac{d^2X(t)}{dt^2} + b\frac{dX(t)}{dt} + kX(t)
\]

where  

- \( X(t) \) represents displacement  
- \( F(t) \) is the applied external force  

In this case study, the system parameters vary with time:

\[
m = \cos(t)
\]

\[
k = 3\cos(t)
\]

\[
b = -2\sin(t)
\]

Applying the Modified Laplace Transform allows the differential equation to be transformed and solved analytically. :contentReference[oaicite:3]{index=3}

---

# Numerical Verification

The analytical solution obtained through the Modified Laplace Transform can be verified through numerical simulation.

MATLAB is used to simulate the displacement response of the system over time.

<img src="/images/101_SystemPlot.png" width="650">

The first plot shows the **numerical displacement**, while the second plot shows the **analytical displacement** derived from the transform-based model.

The close agreement between the two curves indicates that the proposed method successfully captures the dynamic behaviour of the system with time-varying parameters. :contentReference[oaicite:4]{index=4}

---

# Conclusion

Extending classical transform-based analysis to systems with time-varying parameters allows a broader range of dynamic systems to be analysed. The Modified Laplace Transform provides a useful framework for handling differential equations with variable coefficients while maintaining the analytical advantages of transform methods.

The results demonstrate that the approach can effectively model the behaviour of dynamic systems with time-dependent parameters and may provide useful insights for further studies in dynamic system analysis. :contentReference[oaicite:5]{index=5}

---

# References

Rahman, S. M. R., “Development of a Method for the Evaluation of Linear Time-Invariant Systems with Time-Varying Parameters Using Laplace Transform Techniques,” *2024 4th International Conference on Intelligent Technologies (CONIT)*, 2024.

Elzaki, T. M., and Ishag, A. A., “Modified Laplace Transform and Ordinary Differential Equations with Variable Coefficients,” *World Engineering & Applied Sciences Journal*, vol. 10, no. 3, pp. 79–84, 2019.
