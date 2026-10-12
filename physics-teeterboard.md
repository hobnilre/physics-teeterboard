---
title: "Physics of the teeterboard"
subtitle: "Contact, rotation and work in a loaded descent"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-12"
abstract: |
  We derive the mechanism behind part 1 of Mad Scientist 1, from an illustrative
  human teeterboard launch to its computed two-weight lever. Independent
  integrations reproduce 6.994139 J of receiver work and event COP 1.188267.
  Contact, rebound and renewed contact explain the transfer. The drivers'
  further descent and final stores resolve the work account. Figures and
  tables connect the force laws, motion and measurable signals.
keywords:
  - teeterboard
  - unilateral contact
  - lever dynamics
  - work and energy
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-teeterboard} (planned; local edition)\par
\endgroup

# From a launch to a work question

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
release $2Mg(0.50\,\mathrm m)=686.7$ J. This illustrates the scale of gravity's
contribution; the flyer's rise, remaining motion, deformation, losses and
active work must also enter a complete launch account.

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
Both contacts are purely elastic. Dissipation occurs in the receiver and bearing.

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
Outgoing speed does not identify the work source; the contact trajectory
reveals the forces and displacements.

\newpage

# Deriving the work account

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

![Computed cumulative receiver work and total mechanical storage. The latter includes signed gravitational potential. Their sum, plus bearing heat, stays at 5.886 J.](figures/energy.pdf){#fig:energy width=96%}

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
The mechanism has a resolved work account, including its negative final potential.

\newpage

# What the ratio and the load change

There is no external actuator during this event. Its declared starting-energy
denominator is $D=2mgH=5.886$ J. Retaining exactly that reference gives
\begin{equation}
C_{\rm event}=\frac{W_R}{D}=1.188267,\qquad
\eta_g=\frac{W_R}{mg\sum_i[y_i(0)-y_i(T)]}=0.860219.
\label{eq:ratios}
\end{equation}
These answer different questions: output relative to the initial ready-plane
reference, and the fraction of the actual $8.130651$ J gravitational decrease
delivered to the receiver. A shifted datum $y'=y-h$ changes $D$ to
$D'=D-2mgh$ and $U(T)$ by the same constant. Work and $\eta_g$ stay unchanged;
$W_R/D'$ depends on the reference and requires $D'>0$.

| $k$ (N/m) | $b$ (N s/m) | Receiver work (J) | Event COP |
| ---: | ---: | ---: | ---: |
| 500 | 32 | 6.994139 | 1.188267 |
| 450 | 30 | 7.013120 | 1.191492 |
| 450 | 34 | 7.017282 | 1.192199 |
| 550 | 30 | 6.974505 | 1.184931 |
| 550 | 34 | 6.978687 | 1.185642 |

: Reproduction of the reference case and all four confirmation cases in the companion study; the event and height reference are fixed.

![Computed load controls at $k=500$ N/m. Higher resistance changes the force pulse and delays work transfer; a larger force need not yield more work by 1.5 s.](figures/load.pdf){#fig:load width=98%}

\FloatBarrier

At $b=16,32,64$ N s/m the work is respectively $6.959211$, $6.994139$ and
$6.977427$ J. For $b=0$, receiver work is zero and substantial motion remains.
With a stationary loaded equilibrium, $f_i=mg$ gives
$K_\phi\phi_*=-2amg\cos\phi_*$ and $y_*=a\sin\phi_*-mg/k$.
The reference values are $\phi_*=0.192573$ rad and $y_*=-0.115313$ m,
close to, but distinct from, the finite-time endpoint.

We integrated the symmetric Newton equations independently with two numerical
methods and timestep refinement: 21 runs covering all eight configurations.
The largest receiver-work spread was $2.66\times10^{-7}$ J; maximum storage
residual was $3.22\times10^{-7}$ J. Independent power quadrature differed by
at most $1.05\times10^{-11}$ J. These estimate numerical sensitivity; they
do not bound errors in a physical contact law.

\newpage

# Measurements and the next event

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
\frac{W_R-B_{\rm out}}{D+B_{\rm in}}=1.17118>1.15,
\qquad W_R-1.15D=0.225239\,\mathrm J.
\label{eq:measurement}
\end{equation}
Measuring the drivers' final height is equally decisive: the predicted mean
is $0.114406$ m below the ready plane. It locates the energy omitted when the
initial height reference is mistaken for the total descent.

## Preparation and reset

At $T$ the board is tilted and the contacts remain compressed. Another
identical release needs a reset. The companion's separately prescribed
preparation and reset calculation supplies the account below.

| Interval | Gross supplied work (J) | Receiver work (J) |
| :--- | ---: | ---: |
| Preparation to the stated initial state | 5.886000 | 0 |
| The 1.5 s event | 0 | 6.994139 |
| Prescribed reset | 2.210180 | 1.062185 |
| Full history | 8.096180 | 8.056324 |

: Retained full-history calculation in the companion study. Total bearing heat is 0.039844 J and returned actuator work is 0.000012 J; initial and final stores are zero.

The full-history ratio is $8.056324/8.096180=0.995077$: reset adds both input
and output, with different endpoint states from \eqref{eq:ratios}. Human launches
also involve leg activation, board bending and flyer takeoff. In this model,
contact elasticity times the transfer, the lever redirects it, and the receiver
extracts work from a descent extending below the starting reference.

# Reference {-}

1. Hob Nilre and Bo C. Herlin (2026), *[Mad Scientist 1][companion]*,
   part 1, “The falling-weight lever,” and its common simulation account.

[companion]: https://github.com/hobnilre/physics-mad-scientist-1
