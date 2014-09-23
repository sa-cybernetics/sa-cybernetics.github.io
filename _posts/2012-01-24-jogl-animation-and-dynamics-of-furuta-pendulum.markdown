---
layout: post
title: "JOGL - Animation and Dynamics of Furuta pendulum"
date: 2012-01-24 20:44
comments: true
categories: [linux, java, jogl]
---



I wanted to animate a furuta pendulum, and include the real dynamics in the animation.
First off, what is a Furuta pendulum? It is a pendulum with two degrees of freedom (see wikipedia) where, from a control engineers' point of view, one is interested in stabilizing the second arm of the pendulum, by applying torque to the first arm. This poses quite an interesting control problem (much the same as in e.g. a segway). First lets look at the dynamimcs of the furuta pendulum:

<!-- more --> 


The dynamics of the furuta pendulum can be modeled with two second order differential equations. For simulations we will reduce the order and model the system with 4 first order ODE's. The following state space vector will be used:

$$
 \begin{aligned} x=\begin{bmatrix} \\ \frac{d\theta_{1}}{dt} & \frac{d\theta_1}{dt}& \theta_{1}&\theta_{2}\end{bmatrix}  \end{aligned}
$$

With the use of Lagrangian or Newton dynamics one can model the system which yields the following 2. order ODE's:


$$
\; \\ \; \\ \;
{ \scriptsize
\begin{aligned}
& \frac{d^2\theta_1}{dt^2}= \\
&  \frac{ (mx_1^2cos(x_4)
sin(x_4)^3L_2^3+(gmsin(x_4)^3-2mx_1x_2cos(x_4)^2sin(x_4)L_1)L_2^2+((mx_1^2-mx_2^2)cos(x_4)sin(x_4)L_1^2+x_1^2cos(x_4)sin(x_4)J_1)
L_2+gmsin(x_4)L_1^2+\tau cos(x_4)L_1+gsin(x_4)J_1)}{(msin(x_4)^2L_2^3+((m-mcos(x_4)^2)L_1^2+J_1)L_2)}
\\
&\frac{d^2\theta_2}{dt^2}=\\
& \frac{(mx_1^2cos(x_4) 
sin(x_4)^3L_2^3+(gmsin(x_4)^3-2mx_1x_2cos(x_4)^2sin(x_4)L_1)L_2^2+((mx_1^2-mx_2^2)cos(x_4)sin(x_4)L_1^2+x_1^2cos(x_4)sin(x_4)J_1)
L_2+gmsin(x_4)L_1^2+taucos(x_4)L_1+gsin(x_4)J_1)}{(msin(x_4)^2L_2^3+((m-mcos(x_4)^2)L_1^2+J_1)L_2)}
\end{aligned}
}
$$

The following state space equations used in the simulation is therefor

$$
\dot{x}= \begin{bmatrix}\ddot{\theta}_1 \\ \ddot{\theta}_2 \\ \theta_1 \\ \theta_2 \end{bmatrix} = f(x)
$$

And one can easily solve the dynamics by numerical integration. I have solved the system using Explicit Runge Kutta 4 which yields a discrete solution that can easily be used in a OpenGl 3d animation. The main idea for capturing the dynamics in the animation is to, in  each call to the display() function (each new frame of the animation), calculate the next iterate of the numerical integrator (RK4 in this case). This can be seen in the code below, where $$ f_1=\ddot{\theta}_1 $$ and f2, f3,f4 (not shown in the code) each calculates their derrivatives which is used in one multiple input, multiple output function f. Lastly this is used in solve_dyn() to calculate an iterate from the RK4 method.

<script src="https://gist.github.com/simena86/1cae25be89a82e4a650d.js"></script>

The animation:

{% youtube Lmvn_uDE4HE %}




The source can now be cloned from git [here](   https://github.com/simena86/furuta_pendulum "gitlink").
