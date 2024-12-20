### Noether's theorem & Euler-Lagrangian equation

#### 1. Variation of the volume element under infinitesimal transformation

$$
det(\partial_\nu \delta x^\mu)=\partial_\mu \delta x^\mu
$$

The $dx^4$ transform as

$$
dx'^4 = Jdx^4
$$

where $J$ is the Jacobi determinant

$$
J=det(\frac{\partial x'^\mu}{\partial x^\nu})
$$

for the partial differential matrix between the old and new coordinates, a typical $J=\pm 1$ indicates the volume is not expanded or contract after the transformation. We assume a infinitesimal transformation

$$
x'^\mu=x^\mu+\delta x^\mu
$$

Then

$$
J=det(\frac{\partial x'^\mu}{\partial x^\nu})=det(\frac{\partial x^\mu}{\partial x^\nu}+\frac{\partial \delta x^\mu}{\partial x^\nu})=det(\delta^\mu_{~~\nu}+\partial_\nu \delta x^\mu)=1+\partial_\mu \delta x^\mu
$$

In the very last step, we make use of the fact that the differentiate for a determinant at $I$ is the trace (just think of identity matrix with every component added by a very small quantity, when solve for the determinant, only the linear terms at the main diagonal matter, which is the trace.）

Therefore,

$$
dx'^4 = Jdx^4=(1+\partial_\mu \delta x^\mu)dx^4
$$

And the variation of the volume element under infinitesimal transformation is

$$
\delta(dx^4)=dx'^4-dx^4=(\partial_\mu \delta x^\mu) dx^4
$$

#### 2. Variation of the Lagrangian

We assume the field quantity changes at the same time that coordinates are changed, it should have a variation:

$$
\phi(x)\rightarrow\phi'(x')+\delta \phi(x)
$$

Please note that, the variation contains two part:

##### (1) the variation of the field $\phi\rightarrow\phi'=\phi+\bar\delta \phi$ (we assume it is the same before/after the change of coordinates as is a infinitesimal transformation, for distinction we use a bar),

and

##### (2) the variation of the coordinates $x\rightarrow x'=x+\delta x$. So the field quantity has been changed, due to certain evolution of the field, while the perspective of view is also changed, such as the observer is rotated by a degree, or in a different inertial frame. The Lagrangian depends on the coordinates similarly,

$$
\delta L(x)=L'(x')-L(x)=[L'(x')-L(x')]-[L(x')-L(x)]=\bar\delta L+\partial_\mu L\delta x^\mu
$$

and

$$
\bar\delta L=L'(x)-L(x)=\frac{\partial L}{\partial \phi}\bar\delta\phi+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\partial_\mu\phi
$$

This is because the Lagrangian is the function of the field quantity and its 1st order differential.

 Overall, we have

$$
\delta L(x)=\frac{\partial L}{\partial \phi}\bar\delta\phi+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\partial_\mu\phi+\partial_\mu L\delta x^\mu
$$

#### 3. Principle of Stationary Action

Now we search for the stationary of the action by set the variation to zero:

$$
\delta S=\delta(\int d^4xL)=\int\delta(d^4x)L+\int d^4x\delta L\\
=\int d^4x(\partial_\mu \delta x^\mu)L+\int d^4x(\frac{\partial L}{\partial \phi}\bar\delta\phi+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\partial_\mu\phi+\partial_\mu L\delta x^\mu)\\
$$

Now, we put the changes arises from coordinate transformation together, which is the first integral and the their term in the second integral:

$$
\int d^4x[(\partial_\mu \delta x^\mu)L+(\partial_\mu L)\delta x^\mu]+\int d^4x(\frac{\partial L}{\partial \phi}\bar\delta\phi+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\partial_\mu\phi)\\
=\int d^4x \partial_\mu(\delta x^\mu L)+\int d^4x (\frac{\partial L}{\partial \phi}\bar\delta\phi+\partial_\mu(\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi)-\partial_\mu(\frac{\partial L}{\partial\partial_\mu\phi})\bar\delta\phi)\\
=\int d^4x\partial_\mu(L\delta x^\mu+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi)+\int d^4x\bar\delta\phi(\frac{\partial L}{\partial \phi}-\partial_\mu\frac{\partial L}{\partial\partial_\mu\phi})=0
$$

Now we consider:

##### (1) In fixed frame how the field evolves:

In this case, $\delta x^\mu=0$, the first term becomes:

$$
\int d^4x\partial_\mu(L\delta x^\mu+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi)=\int d^4x\partial_\mu(\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi)=\oint_S dS\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi=0
$$

As the field quantity is fixed at the boundary of space-time, $\delta\phi=0$ in the surface integral. Now we only have the second term. At the stationary point of action, we must have:

$$
\frac{\partial L}{\partial \phi}-\partial_\mu\frac{\partial L}{\partial\partial_\mu\phi}=0
$$

This is literally the ==Euler-Lagrangian equation==, which governs how the field evolves through time.

##### (2) Changes of frame will not affect the action:

Now the field is indeed a solution to E-L equation, this left us with the first term equals to zero. We must assure the transformed field is also a solution to E-L equation, this indicates a continue transform under which the action is invariant, and the equation of motion has the same form. This indicates:

$$
\partial_\mu(L\delta x^\mu+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi)=0
$$

We let

$$
j^\mu=L\delta x^\mu+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi$$
$$

The variation of Lagrangian containing coordinates change equals to zero:
$$
\delta\phi=\phi'(x')-\phi(x)=[\phi'(x')-\phi(x')]+[\phi(x')-\phi(x)]=\bar\delta\phi+\partial_\nu\phi\delta x^\nu=0
$$
The new field quantity at new coordinate should equals to the old field quantity at old corrdinate, otherwise there is an unique frame that we can tells apart from the transformation. Therefore, we can write the conservation current contributed purely from coordinates change:
$$
j^\mu=L\delta x^\mu+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi=j^\mu=L\delta x^\mu-\frac{\partial L}{\partial\partial_\mu\phi}\partial_\nu\phi\delta x^\nu=(Lg^\mu_{~~\nu}-\frac{\partial L}{\partial\partial_\mu\phi}\partial_\nu\phi)\delta x^\nu
$$


And we have
$$
\partial_\mu j^\mu=0
$$

which is the ==continuity equation==. $j^\mu$ here correspond to a conservation 4-current (and of course one example is the electric current). To clarify the physical meaning, we integral in a region:

$$
0=\int d^3x\partial_\mu j^\mu=\frac{\partial}{\partial t}\int d^3xj^0+\int d^3x\nabla\cdot\vec{j}=\frac{\partial}{\partial t}\int d^3xj^0+\oint_S d\vec{\sigma}\cdot\vec{j}
$$

So $\int d^3xj^0$ is the conservation charge, $j^0$ is the charge density, and $\vec{j}$ is the conservation current.

Now we come into conclusion to the so-called ==Noether's theorem==, which claims that, any invariant continue transform to the action (symmetric transformation) correspond to a conservation quantity. Here we list some of them:

<center>Space-time translation symmetry -> Energy & momentum conservation</center>

<center>Rotational symmetry -> Angular momentum conservation</center>

<center>U(1) gauge symmetry -> Electric charge conservation</center>

In later we will see how to construct the energy and momentum directly from the Lagrangian model of different kind of fields.
