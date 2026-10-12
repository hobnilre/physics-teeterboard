---
title: "Physics of the teeterboard"
subtitle: "Why the falling-weight event exceeds COP 1.15"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-12"
abstract: |
  The falling-weight event in part 1 of Mad Scientist 1 delivers 6.994139 J
  to its receiver against a fixed starting-energy reference of 5.886 J:
  event COP 1.188267, above 1.15. The weights continue below the reference
  plane, releasing a further 2.244651 J. After remaining kinetic and elastic
  stores and bearing heat, 1.108139 J reaches the receiver above the starting
  reference. We follow the contact mechanism and derive the positive margin,
  supported by computed traces, five calculated cases and a measurement budget.
keywords:
  - teeterboard
  - unilateral contact
  - lever dynamics
  - work and energy
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-teeterboard}\par
\endgroup

# The question: event COP above 1.15

Two people land on one side of a teeterboard and lift a third. The pivot
redirects motion while legs and board deform. Part 1 of [Mad Scientist 1][companion]
uses this picture to motivate a falling-weight lever [OP-CT-HW-01]. Its human
speeds are illustrative; its numerical study concerns a separate mechanical model.

![Schematic of the illustrative launch. Incoming and outgoing kinetic energies describe different endpoints; compression, gravity and any muscular work act between them.](figures/launch.pdf){#fig:launch width=98%}

For three equal masses $M=70\,\mathrm{kg}$, two arrivals at downward speed
$u=5\,\mathrm{m/s}$ and one departure at upward speed $w=8\,\mathrm{m/s}$ give
\begin{equation}
K_{\rm in}=Mu^2=1750\,\mathrm J,\qquad
K_{\rm out}=\tfrac12Mw^2=2240\,\mathrm J,
\quad \frac{K_{\rm out}}{K_{\rm in}}=\frac{32}{25}.
\label{eq:launch}
\end{equation}
The difference is $490$ J. Two such masses descending another $0.50$ m
release $2Mg(0.50\,\mathrm m)=686.7$ J. The flyer's rise, remaining motion, deformation, losses and active work
also enter the launch account. Gravity keeps doing work after contact begins;
the arrival energy alone does not describe everything available to the receiver.

\newpage

# Geometry and forces of the computed event

The calculation replaces the performers with two identical, vertically guided
drivers and an external viscous receiver. The rigid board has a fixed pivot,
inertia $I$, a torsion spring $K_\phi$ and bearing damping $c_b$. Its centre of
mass lies at the pivot. Contacts exert vertical forces; ideal guides do no work.
Board bending, a departing flyer and active leg forces are absent from this model.

![Model schematic, shown in contact. The two drivers share the left arm but have separate vertical springs. Positive rotation lowers that arm and raises the receiver. The pivot spring and bearing act relative to ground.](figures/model.pdf){#fig:model width=98%}

Upward driver heights are $y_i$ and positive board angle is $\phi$. A signed
arm $a$ has height $a\sin\phi$; the receiver has displacement
$s_R=a_R\sin\phi$. Compression and receiver velocity follow from geometry:
\begin{equation}
\delta_i=[a\sin\phi-y_i]_+,\quad f_i=k\delta_i,\qquad
v_R=a_R\cos\phi\,\dot\phi,\quad F_R=bv_R.
\label{eq:contact}
\end{equation}
Here $[x]_+=\max(x,0)$ and $F_R$ is the force delivered to the receiver.
The opposite force acts on the board. Multiplying each vertical force by
its horizontal moment arm gives Newton's equations:
\begin{equation}
\begin{split}
m\ddot y_i=-mg+f_i,\qquad i=1,2,\\
I\ddot\phi=-a\cos\phi(f_1+f_2)-K_\phi\phi-c_b\dot\phi
-b a_R^2\cos^2\phi\,\dot\phi.
\end{split}
\label{eq:newton}
\end{equation}

| Quantity | Value | Quantity | Value |
| :--- | ---: | :--- | ---: |
| Each driver $m$ | $1$ kg | Board inertia $I$ | $0.15$ kg m$^2$ |
| Driver arm $a$ | $-0.50$ m | Receiver arm $a_R$ | $0.80$ m |
| Contact stiffness $k$ | $500$ N/m | Load $b$ | $32$ N s/m |
| Torsion $K_\phi$ | $50$ N m/rad | Bearing $c_b$ | $0.10$ N m s/rad |
| Release height $H$ | $0.30$ m | Gravity $g$ | $9.81$ m/s$^2$ |

: Reference parameters. Initially $y_1=y_2=H$, $\phi=0$ and all velocities are zero. The event ends at the fixed time $T=1.5$ s.

The springs push only while compressed. At separation $\delta_i=f_i=0$;
the law introduces neither an impact impulse nor a discrete energy loss.
Both contacts are purely elastic; the receiver and bearing dissipate energy.
The weights can keep falling while they turn the board. The springs time that
transfer, and the receiver takes work from the resulting motion.

\newpage

# The contact history

Before touchdown the board remains horizontal and each driver is in free fall:
$y=H-gt^2/2$. Contact begins at $t_c=\sqrt{2H/g}=0.247310$ s,
with $\dot y(t_c)=-\sqrt{2gH}=-2.426108$ m/s. The two contacts are
simultaneous by symmetry. Their forces decelerate the drivers and apply a
positive torque to the board; the right arm rises against the receiver.

![Computed reference trajectory. Left: driver, left board contact and receiver heights. Right: upward force on each driver and signed force delivered to the receiver. The contact-free interval lies between the dotted lines.](figures/history.pdf){#fig:history width=98%}

\FloatBarrier

| Event | Time (s) | Driver $y$ (m) | Board $\phi$ (rad) |
| :--- | ---: | ---: | ---: |
| First contact | 0.247310 | 0.000000 | 0.000000 |
| First driver reversal | 0.344255 | $-0.148164$ | 0.139293 |
| First board reversal | 0.408321 | $-0.110027$ | 0.195639 |
| Contact opens | 0.427352 | $-0.095356$ | 0.191887 |
| Contact closes again | 0.526451 | $-0.074597$ | 0.149754 |
| Declared event end | 1.500000 | $-0.114406$ | 0.190618 |

: Numerically located transitions and the prescribed endpoint. Driver and board reversals occur at different times.

The drivers reach their lowest position while the board is still rotating
upward on the receiver side. Elastic unloading then lifts the drivers.
They leave the board, follow a short ballistic arc, and contact it again.
Smaller oscillations follow. The peak force on each driver is $46.53$ N and
the largest compression is $93.05$ mm; these are spring-model predictions.

Receiver force changes sign when receiver velocity changes sign, but its power
remains $P_R=F_Rv_R=bv_R^2\geq0$. The descending return motion therefore also
delivers work. A one-way receiver or a free flyer would require a different law.

Moving board points have $v_a=a\cos\phi\dot\phi$ and $|v_R/v_a|=a_R/|a|=1.6$.
Here the drivers can compress and leave the contact, so their speed is not
the board-point speed. Compliance and timing determine the transfer; the arm
ratio alone cannot predict the outgoing motion or work.

A stationary ideal pivot supplies impulse $J_O=\int F_O\,dt$ but no work,
since $P_O=F_Ov_O=0$. The performers' vertical momentum alone is not conserved.
The receiver collects work on the upward stroke and the return stroke.
Their accumulated work is the output used in the event COP.

\newpage

# Following the extra descent into receiver work

The mechanical boundary contains the drivers, board, contact and torsion
springs, with gravity included as potential energy. The receiver and bearing
heat lie outside. Set gravitational zero at the initial horizontal board:
\begin{equation}
U=\tfrac12m\sum_i\dot y_i^2+\tfrac12I\dot\phi^2
+mg\sum_i y_i+\tfrac12K_\phi\phi^2+\tfrac12k\sum_i\delta_i^2.
\label{eq:store}
\end{equation}
During contact, $\dot\delta_i=a\cos\phi\dot\phi-\dot y_i$.
Multiply \eqref{eq:newton} by the corresponding velocities and differentiate
\eqref{eq:store}: the contact and torsion powers cancel internally. Hence
\begin{equation}
\dot U=-bv_R^2-c_b\dot\phi^2,\qquad
U(T)+W_R+Q_b=U(0),\quad
(W_R,Q_b)=\int_0^T(bv_R^2,c_b\dot\phi^2)\,dt.
\label{eq:work}
\end{equation}
The same identity holds across opening and closure because spring energy
vanishes at zero compression. This balance follows from the force laws.

![Computed cumulative receiver work and total mechanical storage. The latter includes signed gravitational potential. Their sum, plus bearing heat, stays at 5.886 J. Receiver work crosses the marked threshold of 1.15 times the starting energy.](figures/energy.pdf){#fig:energy width=96%}

\FloatBarrier

| Energy or work | Start (J) | End or accumulated (J) |
| :--- | ---: | ---: |
| Gravitational potential | 5.886000 | $-2.244651$ |
| Kinetic energy, both drivers and board | 0 | 0.000012 |
| Torsion spring | 0 | 0.908383 |
| Contact springs, both | 0 | 0.193519 |
| Total mechanical storage $U$ | 5.886000 | $-1.142737$ |
| Receiver work $W_R$; bearing heat $Q_b$ | 0; 0 | 6.994139; 0.034598 |

: Endpoint stores evaluated directly from the solved state; work obtained by power integration.

The extra $2.244651$ J of gravitational descent below the ready plane pays
for $1.108139$ J of output above the starting reference, $1.101914$ J of
remaining kinetic and elastic energy, and $0.034598$ J of bearing heat.
The weights finish below the plane used to count their starting energy.
That continued descent lets the receiver collect more than the starting reference.

\newpage

# Why the event COP exceeds 1.15

Keep the original zero-height plane and the fixed $1.5$ s event. There is no
external actuator input. With starting energy $D=2mgH=5.886$ J, define
$E_{\rm below}=-mg\sum_i y_i(T)$ and the remaining non-gravitational store
$U_+=K(T)+U_\phi(T)+U_c(T)$. Here $K$, $U_\phi$ and $U_c$ are the kinetic,
torsion and contact terms in \eqref{eq:store}. The work identity gives
\begin{equation}
C_{\rm event}=\frac{W_R}{D}
=1+\frac{E_{\rm below}-U_+-Q_b}{D}=1.188267.
\label{eq:cop}
\end{equation}
Gravity is already inside the stored-energy account. The extra descent appears
as negative final potential, while $D$ stays at its declared reference. Thus
\begin{equation}
C_{\rm event}>1.15\quad\Longleftrightarrow\quad
E_{\rm below}>0.15D+U_++Q_b.
\label{eq:threshold}
\end{equation}
The left side is $2.244651$ J and the required right side is $2.019413$ J.
The resulting margin is $0.225239$ J. Each weight ends $0.414406$ m below its release height;
the starting reference counts $0.30$ m. The actual gravitational release is
$8.130651$ J. This is how the stated event ratio clears 1.15.

| $k$ (N/m) | $b$ (N s/m) | Receiver work (J) | Event COP | Margin (J) |
| ---: | ---: | ---: | ---: | ---: |
| 500 | 32 | 6.994139 | 1.188267 | 0.225239 |
| 450 | 30 | 7.013120 | 1.191492 | 0.244220 |
| 450 | 34 | 7.017282 | 1.192199 | 0.248382 |
| 550 | 30 | 6.974505 | 1.184931 | 0.205605 |
| 550 | 34 | 6.978687 | 1.185642 | 0.209787 |

: Reference and four confirmation cases, with fixed event and height reference. Margin means $W_R-1.15D$; all five cases clear the threshold.

![Computed load controls at $k=500$ N/m. Higher resistance changes the force pulse and delays work transfer; a larger force need not yield more work by 1.5 s.](figures/load.pdf){#fig:load width=98%}

\FloatBarrier

At $b=16,32,64$ N s/m the work is respectively $6.959211$, $6.994139$ and
$6.977427$ J. For $b=0$, receiver work is zero and substantial motion remains.

The extra fall covers the energy still in the mechanism and the bearing heat,
then leaves enough receiver work to exceed the 15 percent target in all five tabulated cases.

\newpage

# Making the margin measurable

We integrated the symmetric Newton equations independently with two numerical
methods and timestep refinement: 21 runs covering all eight configurations.
The largest receiver-work spread was $2.66\times10^{-7}$ J; maximum storage
residual was $3.22\times10^{-7}$ J. Independent power quadrature differed by
at most $1.05\times10^{-11}$ J. These estimate numerical sensitivity, not physical-law error.

A synchronized load cell and displacement encoder give signed receiver work,
$W_R=\int F_R\,ds_R$, including the return stroke. Driver heights and board
angle distinguish gravity's contribution from compression and remaining motion;
an endpoint speed alone cannot.

| Signal or condition | Reference prediction or assumed requirement |
| :--- | :--- |
| Peak receiver force and speed | $52.40$ N; $1.637$ m/s |
| Receiver displacement range; total travel | $0$--$0.1555$ m; $0.2460$ m |
| Contact and event timing | Separation $0.427$--$0.526$ s; end $1.5$ s |
| Prospective acquisition | $200$ Hz response; $2$ kHz sampling; skew $\leq0.1$ ms |
| Assumed simultaneous energy bounds | $B_{\rm in}=0.02943$ J; $B_{\rm out}=0.06608$ J |

: Predicted signal scales and the companion's prospective instrument budget. The bounds require calibration; they are not measurements made here.

That budget includes initial mass and height, force and displacement gains,
offset, sampling, timing, bandwidth, loading and event-boundary allowances.
With those simultaneous bounds the reference result remains above 1.15:
\begin{equation}
\begin{split}
\frac{W_R-B_{\rm out}}{D+B_{\rm in}}&=1.17118>1.15,\\
(W_R-B_{\rm out})-1.15(D+B_{\rm in})&=0.125314\,\mathrm J>0.
\end{split}
\label{eq:measurement}
\end{equation}
The assumed measurement errors consume part of the predicted margin, but leave
$0.125314$ J above the target. A receiver-work trace can therefore resolve the
above-threshold result if those instrument bounds are achieved.

The drivers' final height completes the explanation: they end $0.114406$ m
below the ready plane. Against the fixed $5.886$ J reference, the receiver gets
$6.994139$ J because gravity continues releasing energy below that plane.
The work trace establishes COP above 1.15; the extra descent and endpoint stores
show exactly how it is possible.

# Reference {-}

1. Hob Nilre and Bo C. Herlin (2026), *[Mad Scientist 1][companion]*,
   part 1, “The falling-weight lever,” and its common simulation account.

[companion]: https://github.com/hobnilre/physics-mad-scientist-1
