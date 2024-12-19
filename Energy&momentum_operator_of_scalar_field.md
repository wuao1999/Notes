---

### Energy & momentum operator of K-G scalar field

---

In this section we derive the energy and momentum (4-momentum) operator for scalar field directly from the Noether's theorem

#### 1. Noether's theorem with respect to space-time translation

Previously we knew that energy/momentum are the conservation charge for temporal/spatial  translation invariance/symmetry, the Noether's theorem gives the conservation current:
$$
j^\mu=L\delta x^\mu+\frac{\partial L}{\partial\partial_\mu\phi}\bar\delta\phi=j^\mu=L\delta x^\mu-\frac{\partial L}{\partial\partial_\mu\phi}\partial_\nu\phi\delta x^\nu=(Lg^\mu_{~~\nu}-\frac{\partial L}{\partial\partial_\mu\phi}\partial_\nu\phi)\delta x^\nu
$$

Here, for space-time translation, the coordinate variation
$$
\delta x^\nu=\epsilon^\nu
$$
is a infinitisimal constant independent of the coordinate. Therefore:
$$
j^\mu=(Lg^\mu_{~~\nu}-\frac{\partial L}{\partial\partial_\mu\phi}\partial_\nu\phi)\epsilon^\nu=-(\frac{\partial L}{\partial\partial_\mu\phi}\partial_\nu\phi-Lg^\mu_{~~\nu})\epsilon^\nu=-\mathcal{T}^\mu_{~~~~\nu}\epsilon^\nu=-\mathcal{T}^\mu{^\nu}\epsilon_\nu
$$
In the last step, we make use of:
$$
\mathcal{T}^\mu_{~~~~\nu}\epsilon^\nu=\mathcal{T}^\mu_{~~~~\rho}\epsilon^\rho=\mathcal{T}^\mu{^\nu}g_\nu{_\rho}\epsilon^\rho=\mathcal{T}^\mu{^\nu}\epsilon_\nu
$$
Here $\mathcal{T}^\mu{^\nu}$ is the ==energy-momentum tensor==
$$
\mathcal{T}^\mu{^\nu}=\frac{\partial L}{\partial\partial_\mu\phi}\partial^\nu\phi-Lg^\mu{^\nu}
$$
is a rank-2 symmetric tensor (now in contravariant form). The symmetry is general for all situations. For better comprehension, for example, in real scalar field, the K-G lagrangian model: 
$$
L=\frac{1}{2}(\partial^\mu\phi\partial_\mu\phi-m^2\phi^2)
$$
So, $\frac{\partial L}{\partial\partial_\mu\phi}=\partial^\mu\phi$, then it is easy to tell that  $\mathcal{T}^\mu{^\nu}$ is symmetric. As $\epsilon^\nu$ is a constant, we can directly define the conservation quantity:
$$
P^\nu=\int d^3x\mathcal{P}^\nu=\int d^3x\mathcal{T}^0{^\nu}=\int d^3x\frac{\partial L}{\partial\partial_0\phi}\partial^\nu\phi-Lg^0{^\nu}
$$
The conservation quantity $P^\nu$ here is the 4-momentum, and $\mathcal{P}^\nu$ the corresponding 4-momentum density. We consider the energy and momentum separately:

##### (1) The energy of the real scalar field:

$$
P^0=\int d^3x\mathcal{P}^0=\int d^3x[(\partial_0\phi)^2-L]=\int d^3x[(\partial_0\phi)^2-\frac{1}{2}(\partial^\mu\phi\partial_\mu\phi-m^2\phi^2)]=\int d^3x[(\partial_0\phi)^2-\frac{1}{2}[(\partial_0\phi)^2-(\nabla\phi)^2-m^2\phi^2]]\\
=\int d^3x\frac{1}{2}[(\partial_0\phi)^2+(\nabla\phi)^2+m^2\phi^2]=\int d^3x\frac{1}{2}[(\partial_0\phi)^2+\nabla(\phi\nabla\phi)-\phi\nabla^2\phi+m^2\phi^2]=\int d^3x\frac{1}{2}[(\partial_0\phi)^2+\nabla(\phi\nabla\phi)-\phi\nabla^2\phi-\phi(\partial_\mu\partial^\mu\phi)]\\
=\int d^3x\frac{1}{2}[(\partial_0\phi)^2-\phi\partial_0^2\phi]=\int d^3x\frac{1}{2}i\phi i\bar\partial_0(\partial_0\phi)
$$

Here in the last three step, we respectively use: (1) $\phi$ is a solution to the Klein-Gordan equation, (2) Second term is a full-space integral of a gradient, according to Gauss's law, it's equivalent to a surface integral at infinity, where the field vanishes, and (3) $Ai\bar\partial_0B$ is defined as $Ai\partial_0B-Bi\partial_0A$. Here, the normal $i$ shows up as an imarginary unit.

##### (2) The momentum of the real scalar field:

$$
P^i=\int d^3x\mathcal{P}^i=\int d^3x\partial_0\phi\partial_i\phi=\frac{1}{2}\int d^3x2\partial_0\phi\partial_i\phi=\frac{1}{2}\int d^3x[\partial_0\phi\partial_i\phi-\partial_i(\phi\partial_0\phi)+\partial_0\phi\partial_i\phi]\\
=\frac{1}{2}\int d^3x[\partial_0\phi\partial_i\phi-\phi\partial_0\partial_i\phi]=\int d^3x\frac{1}{2}i\phi i\bar\partial_0(\partial_i\phi)
$$

Similarly we make use of Gauss's law and the definition of $\bar\partial_0$. Combining (1) and (2), we have
$$
P^\mu=\int d^3x\mathcal{P}^\mu=\int d^3x\frac{1}{2}i\phi i\bar\partial_0(\partial_\mu\phi)
$$
We expand it in momentum space and implement second quantization:
$$
P^\mu=\int d^3x\frac{1}{2}i\phi i\bar\partial_0(\partial_\mu\phi)=\int d^3x\iint d^3kd^3k'[\frac{1}{2}i(a_k\varphi_k(x)+a^\dagger_k\varphi^\star_k(x)) i\bar\partial_0\partial_\mu(a_{k'}\varphi_{k'}(x)+a^\dagger_{k'}\varphi^\star_{k'}(x))]\\
=\int d^3x\iint d^3kd^3k'[\frac{1}{2}i(a_k\varphi_k(x)+a^\dagger_k\varphi^\star_k(x)) i\bar\partial_0ik'^\mu(-a_{k'}\varphi_{k'}(x)+a^\dagger_{k'}\varphi^\star_{k'}(x)]
$$
According to the orthornomality relation of field operator, only the cross terms are non-zero:
$$
P^\mu=\iint  d^3kd^3k'\int d^3x\frac{k'^\mu}{2}[-a_ka^\dagger_{k'}\varphi_k(x)i\bar\partial_0\varphi^\star_{k'}(x)+a^\dagger_ka_{k'}\varphi^\star_k(x)i\bar\partial_0\varphi_{k'}(x)]\\
=\iint  d^3kd^3k'\frac{k'^\mu}{2}[a_ka^\dagger_{k'}\delta(k-k')+a^\dagger_ka_{k'}\delta(k-k')]=\int  d^3k\frac{k^\mu}{2}(a_ka^\dagger_{k}+a^\dagger_ka_{k})
$$
Convert to box normalization:
$$
P^\mu=\sum_k\frac{k^\mu}{2}(a_ka^\dagger_{k}+a^\dagger_ka_{k})\sum_k\frac{k^\mu}{2}(2a^\dagger_ka_{k}+1)=\sum_kk^\mu(N_k+\frac{1}{2})
$$
where $N_k$ is the particle number operator. We see that the real scalar field is indeed a infinite degree-of-freedom harmonic oscillator ensemble (finite, if localized, eg. in a box), with each of 4-momentum $k^\mu$ (that is, with energy $\omega$ and momentum $\vec{k}$), and a nonneglegible zero-point energy $\frac{1}{2}k^\mu$.
