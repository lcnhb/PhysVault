---
Alias:
- Poisson bracket
tags:
- qftII
---
# Definition in [[../AnalyticalMech/canonical coordinates]]
In [[../AnalyticalMech/canonical coordinates]] (also known as [[../AnalyticalMech/canonical coordinates|Darboux coordinates]]) $(q_i,\, p_i)$ on the [[phase space]], given two functions $f(p_i,\, q_i, t)$ and $g(p_i,\, q_i, t)$, $f(p_i,\, q_i,\, t)$ means $f$ is a function of the $2N + 1$ independent variables: momentum, $p_{1…N}$; position, $q_{1…N}$; and time, $t$ the Poisson bracket takes the form

$$\{f, g\} = \sum_{i=1}^{N} \left( \frac{\partial f}{\partial q_{i}} \frac{\partial g}{\partial p_{i}} - \frac{\partial f}{\partial p_i} \frac{\partial g}{\partial q_i}\right).$$

The Poisson brackets of the [[../AnalyticalMech/canonical coordinates]] are

$$\begin{align}
  \{q_i,q_j\} &= 0 \\
  \{p_i,p_j\} &= 0 \\
  \{q_i,p_j\} &= \delta_{ij}
\end{align}$$

where ''$\delta_{ij}$'' is the [[Kronecker delta]].
# Properties
Given two functions f and g that depend on [[phase space]] and time, their Poisson bracket $$\{f, g\}$$ is another function that depends on phase space and time. The following rules hold for any three functions $f,\, g,\, h$ of [[phase space]] and time:
- [[Antisymmerty]]: $\{f, g\} = -\{g, f\}$
- [[Bilinearity]]: $\{af + bg, h\} = a\{f, h\} + b\{g, h\}, \quad \{h, af + bg\} = a\{h, f\} + b\{h, g\}, \quad a, b \in \mathbb R$
- [[Product rule|Leibniz's rule]]: $\{fg, h\} = \{f, h\}g + f\{g, h\}$
- [[Jacobi identity]]: $\{f, \{g, h\}\} + \{g, \{h, f\}\} +  \{h, \{f, g\}\} = 0$

Also, if a function $k$ is constant over [[phase space]] (but may depend on time), then $\{f,\, k\} = 0$ for any $f$.



# Hamilton's equations of motion 
[[Hamilton's equations of motion]] have an equivalent expression in terms of the Poisson bracket. This may be most directly demonstrated in an explicit coordinate frame. Suppose that $f(p, q, t)$ is a function on the solution’s trajectory-manifold. Then from the multivariable [[chain rule]],

$$\frac{d}{dt} f(p, q, t) = \frac{\partial f}{\partial q} \frac{dq}{dt} + \frac {\partial f}{\partial p} \frac{dp}{dt} + \frac{\partial f}{\partial t}.$$

Further, one may take $p=p(t)$ and $q=q(t)$ to be solutions to [[Hamilton's equations]]; that is,

$$\begin{cases}
  \dot{q} =  \frac{\partial H}{\partial p} = \{q, H\}; \\ 
  \dot{p} = -\frac{\partial H}{\partial q} = \{p, H\}.
\end{cases}$$

Then 
$$\begin{align}
  \frac {d}{dt} f(p, q, t) &= \frac{\partial f}{\partial q} \frac{\partial H}{\partial p} - \frac{\partial f}{\partial p} \frac{\partial H}{\partial q} + \frac{\partial f}{\partial t} \\
                                             &= \{f, H\} + \frac{\partial f}{\partial t} ~.
\end{align}$$

Thus, the time evolution of a function $f$ on a [[symplectic manifold]] can be given as a [[flow (mathematics|one-parameter family]]) of [[symplectomorphism]]s (i.e., [[canonical transformations]], area-preserving diffeomorphisms), with the time $t$ being the parameter:  [[../AnalyticalMech/Hamiltonian]] motion is a canonical transformation generated by the [[../AnalyticalMech/Hamiltonian]]. That is, Poisson brackets are preserved in it, so that ''any time $t$'' in the solution to Hamilton's equations, 

: $$ q(t) = \exp (-t \{ H, \cdot \} ) q(0), \quad  p(t) = \exp (-t \{ H, \cdot \}) p(0), $$ 

can serve as the bracket coordinates. ''Poisson brackets are [[../AnalyticalMech/canonical transformation|canonical invariants]]''.

Dropping the coordinates, 
$$\frac{d}{dt} f = \left(\frac{\partial}{\partial t} - \{H, \cdot\}\right)f.$$

The operator in the convective part of the derivative, $i\hat{L} = -\{H, \cdot\}$, is sometimes referred to as the Liouvillian (see [[Hamiltonian)](Liouville's theorem (Hamiltonian|Liouville's theorem (Hamiltonian)]])).

# Constants of motion 
An [[integrable dynamical system]] will have [[constants of motion]] in addition to the energy. Such constants of motion will commute with the [[../AnalyticalMech/Hamiltonian]] under the Poisson bracket. Suppose some function $f(p, q)$ is a constant of motion. This implies that if $p(t), q(t)$ is a [[trajectory]] or solution to [[Hamilton's equations of motion]], then

$$0 = \frac{df}{dt}$$

along that trajectory. Then

$$0 = \frac{d}{dt} f(p,q) = \{f, H\} + \frac{\partial f}{\partial t}$$

where, as above, the intermediate step follows by applying the equations of motion and we supposed that $f$ does not explicitly depend on time. This equation is known as the [[Liouville's theorem (Hamiltonian]]#Liouville%20equations%7CLiouville%20equation). The content of [[Liouville's theorem (Hamiltonian|Liouville's theorem]]) is that the time evolution of a [[measure (mathematics|measure]]) (or "[[Distribution function (physics|distribution function]])" on the phase space) is given by the above.

If the Poisson bracket of $f$ and $g$ vanishes ($$\{f,g\} = 0$$), then $f$ and $g$ are said to be '''in involution'''.  In order for a [[../AnalyticalMech/Hamiltonian]] system to be [[completely integrable]], $n$ independent constants of motion must be in [[Distribution (differential geometry]]#Involutive%20distributions%7Cmutual%20involution), where $n$ is the number of degrees of freedom.

Furthermore, according to '''Poisson's Theorem''', if two quantities $A$ and $$B$$ are explicitly time independent ($A(p, q), B(p, q)$) constants of motion, so is their Poisson bracket $\{A,\, B\}$. This does not always supply a useful result, however, since the number of possible constants of motion is limited ($2n - 1$ for a system with $n$ degrees of freedom), and so the result may be trivial (a constant, or a function of $A$ and $B$.)

# The Poisson bracket in coordinate-free language# 
Let $M$ be a [[symplectic manifold]], that is, a [[manifold]] equipped with a [[symplectic form]]: a [[Differential form|2-form]] $\omega$ which is both '''closed''' (i.e., its [[exterior derivative]] $d \omega$ vanishes) and '''non-degenerate'''.  For example, in the treatment above, take $M$ to be $\mathbb{R}^{2n}$ and take

$$\omega = \sum_{i=1}^{n} d q_i \wedge d p_i.$$

If $\iota_v \omega$ is the [[interior product]] or [[Tensor contraction|contraction]] operation defined by $(\iota_v \omega)(w) =  \omega(v,\, w)$, then non-degeneracy is equivalent to saying that for every one-form $\alpha$ there is a unique vector field $\Omega_\alpha$ such that $\iota_{\Omega_\alpha} \omega =  \alpha$. Alternatively, $\Omega_{d H} = \omega^{-1}(d H)$. Then if $H$ is a smooth function on $M$, the [[Hamiltonian vector field]] $X_H$ can be defined to be $\Omega_{d H}$.  It is easy to see that

$$\begin{align}
  X_{p_i} &=  \frac{\partial}{\partial q_i} \\
  X_{q_i} &= -\frac{\partial}{\partial p_i}.
\end{align}$$

The '''Poisson bracket''' $\{\cdot,\, \cdot\}$ on (''M'', ω) is a [[bilinear map|bilinear operation]] on [[differentiable function]]s, defined by $\{f,\, g\} \;=\; \omega(X_f,\, X_g)$; the Poisson bracket of two functions on ''M'' is itself a function on ''M''.  The Poisson bracket is antisymmetric because:

$$\{f, g\} = \omega(X_f, X_g) = -\omega(X_g, X_f) = -\{g, f\} $$.

Furthermore,

{{NumBlk|:|$$\begin{align}
  \{f, g\} &= \omega(X_f, X_g) = \omega(\Omega_{df}, X_g) \\
           &= (\iota_{\Omega_{df}}\omega)(X_g) = df(X_g) \\
           &= X_gf = \mathcal{L}_{X_g} f
\end{align}$$.|{{EquationRef|1}}}}

Here ''X<sub>g</sub>f'' denotes the vector field ''X<sub>g</sub>'' applied to the function ''f'' as a directional derivative, and $$\mathcal{L}_{X_g} f$$ denotes the (entirely equivalent) [[Lie derivative]] of the function ''f''.

If α is an arbitrary one-form on ''M'', the vector field Ω<sub>α</sub> generates (at least locally) a [[flow (mathematics|flow]]) $\phi_x(t)$ satisfying the boundary condition $\phi_x(0) = x$ and the first-order differential equation

$$\frac{d\phi_x}{dt} = \left. \Omega_\alpha \right|_{\phi_x(t)}.$$

The $\phi_x(t)$ will be [[symplectomorphism]]s ([[../AnalyticalMech/canonical transformation]]s) for every ''t'' as a function of ''x'' if and only if $\mathcal{L}_{\Omega_\alpha}\omega \;=\; 0$; when this is true, Ω<sub>α</sub> is called a [[symplectic vector field]].  Recalling [[Cartan's identity]] $\mathcal{L}_X\omega \;=\; d (\iota_X \omega) \,+\, \iota_X d\omega$ and ''d''ω = 0, it follows that $\mathcal{L}_{\Omega_\alpha}\omega \;=\; d\left(\iota_{\Omega_\alpha} \omega\right) \;=\; d\alpha$. Therefore, Ω<sub>α</sub> is a symplectic vector field if and only if α is a [[Closed and exact differential forms|closed form]].  Since $d(df) \;=\; d^2f \;=\; 0$, it follows that every [[../AnalyticalMech/Hamiltonian]] vector field ''X<sub>f</sub>'' is a symplectic vector field, and that the Hamiltonian flow consists of canonical transformations.  From {{EquationNote|1|(1)}} above, under the Hamiltonian flow ''X<sub>H</sub>'',

$$\frac{d}{dt}f(\phi_x(t)) = X_Hf = \{f,H\}.$$

This is a fundamental result in Hamiltonian mechanics, governing the time evolution of functions defined on phase space.  As noted above, when ''{f,H} = 0'', ''f'' is a constant of motion of the system.  In addition, in [[../AnalyticalMech/canonical coordinates]] (with $\{p_i,\, p_j\} \;=\; \{q_i,q_j\} \;=\; 0$ and $\{q_i,\, p_j\} \;=\; \delta_{ij}$), Hamilton's equations for the time evolution of the system follow immediately from this formula.

It also follows from {{EquationNote|1|(1)}} that the Poisson bracket is a [[derivation (abstract algebra|derivation]]); that is, it satisfies a non-commutative version of Leibniz's [[product rule]]:

{{NumBlk|:|$$\{fg,h\} = f\{g,h\} + g\{f,h\}$$, and $$\{f,gh\} = g\{f,h\} + h\{f,g\}$$|{{EquationRef|2}}}}

The Poisson bracket is intimately connected to the [[Lie bracket of vector fields|Lie bracket]] of the Hamiltonian vector fields.  Because the Lie derivative is a derivation,

$$\mathcal L_v\iota_w\omega = \iota_{\mathcal L_vw}\omega + \iota_w\mathcal L_v\omega = \iota_{[v,w]}\omega + \iota_w\mathcal L_v\omega$$.

Thus if ''v'' and ''w'' are symplectic, using $\mathcal{L}_v\omega \;=\; 0$, Cartan's identity, and the fact that $\iota_w\omega$ is a closed form,

$$\iota_{[v,w]}\omega = \mathcal L_v\iota_w\omega = d(\iota_v\iota_w\omega) + \iota_vd(\iota_w\omega) = d(\iota_v\iota_w\omega) = d(\omega(w,v)).$$

It follows that $[v,w] = X_{\omega(w,v)}$, so that
{{NumBlk|:|$[X_f,X_g] = X_{\omega(X_g,X_f)} = -X_{\omega(X_f,X_g)} = -X_{\{f,g\}}$.|{{EquationRef|3}}}}

Thus, the Poisson bracket on functions corresponds to the Lie bracket of the associated Hamiltonian vector fields.  We have also shown that the Lie bracket of two symplectic vector fields is a Hamiltonian vector field and hence is also symplectic.  In the language of [[abstract algebra]], the symplectic vector fields form a [[subalgebra]] of the [[../math/Lie theory]] of smooth vector fields on ''M'', and the Hamiltonian vector fields form an [[algebraic ideal|ideal]] of this subalgebra.  The symplectic vector fields are the [[../math/Lie algebras|Lie algebra]] of the (infinite-dimensional) [[../math/Lie group]] of [[symplectomorphism]]s of ''M''.

It is widely asserted that the [[Jacobi identity]] for the Poisson bracket,

$$\ \{f,\{g,h\}\} + \{g,\{h,f\}\} + \{h,\{f,g\}\} = 0$$

follows from the corresponding identity for the Lie bracket of vector fields, but this is true only up to a locally constant function.  However, to prove the Jacobi identity for the Poisson bracket, it is [[Jacobi identity#Examples|sufficient]] to show that:

$$\operatorname{ad}_{\{f,g\}}=[\operatorname{ad}_f,\operatorname{ad}_g]$$

where the operator $\operatorname{ad}_g$ on smooth functions on ''M'' is defined by $\operatorname{ad}_g(\cdot) \;=\; \{\cdot,\, g\}$ and the bracket on the right-hand side is the commutator of operators, $ [\operatorname A,\, \operatorname B] \;=\; \operatorname A\operatorname B - \operatorname B\operatorname A$.  By {{EquationNote|1|(1)}}, the operator $\operatorname{ad}_g$ is equal to the operator ''X<sub>g</sub>''.  The proof of the Jacobi identity follows from {{EquationNote|3|(3)}} because the Lie bracket of vector fields is just their commutator as differential operators.

The [[Algebra over a field|algebra]] of smooth functions on M, together with the Poisson bracket forms a [[Poisson algebra]], because it is a [[../math/Lie theory]] under the Poisson bracket, which additionally satisfies Leibniz's rule {{EquationNote|2|(2)}}.  We have shown that every [[symplectic manifold]] is a [[Poisson manifold]], that is a manifold with a "curly-bracket" operator on smooth functions such that the smooth functions form a Poisson algebra.  However, not every Poisson manifold arises in this way, because Poisson manifolds allow for degeneracy which cannot arise in the symplectic case.

# A result on conjugate momenta# 
Given a smooth [[vector field]] $X$ on the configuration space, let $P_X$ be its [[conjugate momentum]]. The conjugate momentum mapping is a [[../math/Lie theory]] anti-homomorphism from the Poisson bracket to the [[Lie bracket of vector fields|Lie bracket]]:

$$\{P_X, P_Y\} = -P_{[X, Y]}.\,$$

This important result is worth a short proof. Write a vector field $X$ at point $q$ in the [[Configuration space (physics|configuration space]]) as

$$X_q = \sum_i X^i(q) \frac{\partial}{\partial q^i}$$

where the $\scriptstyle \frac{\partial}{\partial q^i}$ is the local coordinate frame. The conjugate momentum to $X$ has the expression

$$P_X(q, p) = \sum_i X^i(q) \;p_i$$

where the $p_i$ are the momentum functions conjugate to the coordinates. One then has, for a point $(q,p)$ in the [[phase space]],

$$\begin{align}
  \{P_X,P_Y\}(q,p) &=  \sum_i \sum_j \left\{ X^i(q) \;p_i, Y^j(q)\; p_j \right\} \\
                   &=  \sum_{ij} p_i Y^j(q) \frac{\partial X^i}{\partial q^j} -  p_j X^i(q) \frac{\partial Y^j}{\partial q^i} \\
                   &= -\sum_i p_i \; [X, Y]^i(q) \\
                   &= - P_{[X, Y]}(q, p). 
\end{align}$$

The above holds for all $(q, p)$, giving the desired result.

# Quantization# 
Poisson brackets [[Deformation theory|deform]] to [[Moyal bracket]]s upon [[Weyl quantization|quantization]], that is, they generalize to a different Lie algebra, the [[Moyal bracket|Moyal algebra]], or, equivalently in [[../math/Hilbert space]], quantum [[commutator]]s. The Wigner-İnönü [[group contraction]] of these (the classical limit, {{math|ħ → 0}})  yields the above Lie algebra.

To state this more explicitly and precisely, the [[universal enveloping algebra]] of the [[Heisenberg algebra]] is the [[Weyl algebra]] (modulo the relation that the center be the unit). The Moyal product is then a special case of the star product on the algebra of symbols. An explicit definition of the algebra of symbols, and the star product is given in the article on the [[universal enveloping algebra]].

In [[mathematics]] and [[classical mechanics]], the '''Poisson bracket''' is an important [[binary operation]] in [[Hamiltonian mechanics]], playing a central role in Hamilton's equations of motion, which govern the time evolution of a Hamiltonian [[dynamical system]]. The Poisson bracket also distinguishes a certain class of coordinate transformations, called ''[[canonical transformations]]'', which map [[../AnalyticalMech/canonical coordinates|canonical coordinate systems]] into canonical coordinate systems. A "canonical coordinate system" consists of canonical position and momentum variables (below symbolized by $q_i$ and $p_i$, respectively) that satisfy canonical Poisson bracket relations. The set of possible canonical transformations is always very rich. For instance, it is often possible to choose the Hamiltonian itself $$H =H(q, p; t)$$ as one of the new canonical momentum coordinates.

In a more general sense, the Poisson bracket is used to define a [[Poisson algebra]], of which the algebra of functions on a [[Poisson manifold]] is a special case. There are other general examples, as well: it occurs in the theory of [[../math/Lie theory]]s, where the [[tensor algebra]] of a Lie algebra forms a Poisson algebra; a detailed construction of how this comes about is given in the [[universal enveloping algebra]] article. Quantum deformations of the universal enveloping algebra lead to the notion of [[quantum group]]s.

All of these objects are named in honor of [[Siméon Denis Poisson]].