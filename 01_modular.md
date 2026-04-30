## Jacobi のテータ関数の性質

指標つき Jacobi のテータ関数は, $a, b ∈ ℝ$, $z, τ ∈ ℂ$ に対して
$$
ϑ\bmqty{a \\ b}(z, τ) = ∑_{ℓ∈ℤ} e^{πi(ℓ+a)^2τ} e^{2πi(ℓ+a)(z+b)}.
$$

簡単な性質は, $n∈ℤ$ として,
$$
\begin{aligned}
  & ϑ\bmqty{a \\ b}(c(z+n), cτ) = e^{2πiacn} ϑ\bmqty{a \\ b}(cz, cτ), \\
  & ϑ\bmqty{a \\ b}(c(z+nτ), cτ) = e^{-iπcn^2τ - 2πin(cz+b)} ϑ\bmqty{a \\ b}(cz, cτ), \\
  & ϑ\bmqty{a + n \\ b}(cz, cτ) = ϑ\bmqty{a \\ b}(cz, cτ), \\
  & ϑ\bmqty{a \\ b + n}(cz, cτ) = e^{2πian} ϑ\bmqty{a \\ b}(cz, cτ), \\
  & ϑ\bmqty{a \\ b}(cz, cτ) = ϑ\bmqty{a \\ 0}(cz + b, cτ). \\
\end{aligned}
$$

2つのテータ関数の積は $a_1,a_2,b_1,b_2∈ℝ$, $c_1,c_2∈ℤ$, $d≡\gcd(c_1,c_2)$ に対して
$$
\begin{aligned}
ϑ\bmqty{a_1/c_1 \\ b_1}(c_1z, c_1τ) × ϑ\bmqty{a_2/c_2 \\ b_2}(c_2z, c_2τ) = ∑_{r=0}^{c_3/d-1} ϑ\bmqty{\frac{(c_2a_1-c_1a_2) + c_1c_2r}{c_1c_2c_3/d} \\ (c_2b_1-c_1b_2)/d}\pqty{0, \frac{c_1c_2c_3}{d^2} τ} \\ × ϑ\bmqty{(a_3 + c_1r)/c_3 \\ b_3}(c_3z, c_3τ).
\end{aligned}
$$
{#eq:theta_product}
ただし, $a_3≡a_1+a_2$, $b_3≡b_1+b_2$, $c_3≡c_1+c_2$ (どれも mod の意味でない) とした.

直交性は,
$$
\begin{aligned}
  ∫_{T^2} dz d\=z e^{\frac{π i c_1}{\Im τ} z \Im z} ϑ\bmqty{a_1/c_1 \\ b_1}(c_1 z, c_1 τ) \pqty{e^{\frac{π i c_2}{\Im τ} z \Im z} ϑ\bmqty{a_2/c_2 \\ b_2}(c_2 z, c_2 τ)}^* \\
  = \sqrt{\frac{\Im τ}{2c_1}} \exp\bqty{2πi \frac{a_1}{c_1} (b_1 - b_2)} δ_{c_1,c_2} δ_{a_1,a_2}^{({\rm mod}\ c_1)}.
\end{aligned}
$$
{#eq:theta_orthogonal}
ただし,
$$
\begin{cases}
  a_1 = a_2 \mod 1, \\
  b_1 = b_2 \mod 1,
\end{cases}
\quad
\left(
⇔
\begin{cases}
  a_1 - a_2 ∈ ℤ, \\
  b_1 - b_2 ∈ ℤ
\end{cases}
\right)
$$
を仮定している.

T変換 $τ→τ+1$ は
$$
\begin{aligned}
  ϑ \bmqty{a/c \\ b} (cz, c(τ+1))
    &= e^{\frac{πi}{c}a(c-a)} ϑ \bmqty{a/c \\ b + a - c/2} (cz, cτ) \\
    &= ∑_{a',b'} ∑_{m∈ℤ} e^{\frac{πi}{c}a(c-a+2m)} δ_{a,a'} δ_{b+a-\frac{c}{2}-m,b'} ϑ \bmqty{a'/c \\ b'} (cz, cτ).
\end{aligned}
$$
{#eq:theta_t}

## 波動関数の性質 with SS phase

フラックス $M$ の $j$-th ゼロモード, SS phase $(α_1,α_2)$ の波動関数は
$$
ψ^{(j+α_1,α_2),M}(z,τ)
  = e^{\frac{πi M}{\Im τ} z \Im z} \mathcal{N}_j ϑ \bmqty{\frac{j+α_1}{M} \\ -α_2} (Mz, Mτ), \quad j = 0, ..., M-1.
$$
SS phase の並進に関する性質は, $n∈ℤ$ について
$$
\begin{aligned}
  & ψ^{(j+α_1+nM,α_2),M}(z,τ) = ψ^{(j+α_1,α_2),M}(z,τ), \\
  & ψ^{(j+α_1,α_2+n),M}(z,τ) = e^{-2πin\frac{j+α_1}{M}} ψ^{(j+α_1,α_2),M}(z,τ). \\
\end{aligned}
$$

### 積

積は, [@eq:theta_product] より
$$
ψ^{(j+α_1,α_2),M}(z,τ) ⋅ ψ^{(k+β_1,β_2),N}(z,τ)
  = ∑_{m=0}^{P/d-1} Y_{j,k,α,β,m}^{M,N,P}(τ) ψ^{(j+k+mM+γ_1,γ_2),P}(z,τ),
$$
{#eq:wave_function_product}
$$
Y_{j,k,α,β,m}^{M,N,P}(τ) ≡ \mathcal{A}^{-1/2} \pqty{\frac{MN}{P}}^{1/4} ϑ \bmqty{\frac{N(j+α_1)-M(k+β_1)+MNm}{MNP/d} \\ (Nα_2-Mβ_2)/d} \pqty{0, \frac{MNP}{d^2} τ}.
$$
ただし $γ≡α+β$ (mod の意味でない), $P≡M+N$, $d≡\gcd(M,N)$ とした. また, $0≤α,β<1$ と取れば $0≤γ<2$ となることに注意.

### 直交性

直交性は, [@eq:theta_orthogonal] より
$$
\begin{aligned}
  ∫_{T^2} dz d\=z ψ^{(j+α_1,α_2),M}(z,τ) \pqty{ψ^{(k+β_1,β_2),N}(z,τ)}^* = (\Im τ)^{-1/2} e^{2πi \frac{j+α_1}{M} (α_2-β_2)} δ_{M,N} δ_{j+α_1,k+β_1}^{({\rm{mod}}\ M)}.
\end{aligned}
$$
{#eq:wave_function_orthogonal}
ただし, $α = β \mod 1$ を仮定.

### 3-point coupling

3-point coupling は, [@eq:wave_function_product; @eq:wave_function_orthogonal] より,
$$
\begin{aligned}
d^{(jα)(kβ)(ℓγ)}
  &= ∫_{T^2} dzd\=z ψ^{(j+α_1,α_2),M}(z,τ) ⋅ ψ^{(k+β_1,β_2),N}(z,τ) ⋅ \pqty{ψ^{(ℓ+γ_1,γ_2),P}(z,τ)}^* \\
  &= (\Im τ)^{-1/2} e^{2πi \frac{ℓ+γ_1}{P} (α_2+β_2-γ_2)} δ_{M+N,P} \\
  & \qquad × ∑_{m=0}^{(M+N)/d-1} Y_{j,k,α,β,m}^{M,N,P}(τ) δ_{(j+α_1)+(k+β_1)-(ℓ+γ_1),-mM}^{({\rm{mod}}\ M+N)}. \\
\end{aligned}
$$
{#eq:yukawa}
ただし, SS phase について, $0≤α_1,β_1,γ_1<1$ および
$$
\begin{cases}
  α_1 + β_1 = γ_1 \mod 1, \\
  α_2 + β_2 = γ_2 \mod 1
\end{cases}
$$
{#eq:rule_SS}
を仮定している.
ここで最後の Kronecker のデルタが non zero になるのは
$$
(j+α_1)+(k+β_1)-(ℓ+γ_1) = -mM \mod{M+N}
$$
の時で, これを満たす $m$ が存在する条件は, $\gcd(M+N,M)=\gcd(N,M)$ より
$$
\boxed{(j+α_1)+(k+β_1) = (ℓ+γ_1) \mod \gcd(M, N)}
$$
{#eq:rule_jkl2}
あるいは
$$
j + k - ℓ = - (α_1 + β_1 - γ_1) \mod \gcd(M, N)
$$
{#eq:rule_jkl}
である. $m$ の総和のうち, この条件を満たすものを $m=m^*$ と書くことにすれば,
$$
\begin{aligned}
d^{(jα)(kβ)(ℓγ)}
  &= ∫_{T^2} dzd\=z ψ^{(j+α_1,α_2),M}(z,τ) ⋅ ψ^{(k+β_1,β_2),N}(z,τ) ⋅ \pqty{ψ^{(ℓ+γ_1,γ_2),P}(z,τ)}^* \\
  &= (\Im τ)^{-1/2} e^{2πi \frac{ℓ+γ_1}{P} (α_2+β_2-γ_2)} Y_{j,k,α,β,m^*}^{M,N,P}(τ) × δ_{M+N,P} δ_{(j+α_1)+(k+β_1)-(ℓ+γ_1),0}^{({\rm{mod}}\ \gcd(M,N))}
\end{aligned}
$$
と書ける.

### T変換

波動関数のT変換は, [@eq:theta_t]より
$$
\begin{aligned}
  T:ψ^{(j+α_1,α_2),M}(z,τ)
    &→ ψ^{(j+α_1,α_2),M}(z,τ+1) \\
    &= ∑_{k=0}^{M-1} ∑_{β_1,β_2} e^{\frac{πi}{M} (j+α_1)(j-α_1+M)} δ_{j,k} δ_{α_1,β_1} δ_{β_2,α_2-α_1+\frac{M}{2}}^{({\rm mod}\ 1)} \\
    & \qquad \qquad \qquad× ψ^{(k+β_1,β_2),M}(z,τ).
\end{aligned}
$$
あるいは, 波動関数をモジュラー形式で書けて,
$$
ψ^{(j+α_1,α_2),M}(\~γ(z,τ))
  = \~J_{1/2}(\~γ,τ) ∑_{k=0}^{M-1} ∑_{β_1,β_2} \~ρ(\~γ)_{(jα)(kβ)} ψ^{(k+β_1,β_2),M}(z,τ), \quad \~γ ∈ \~Γ.
$$
モジュラー変換の生成子 $S$, $T$ の表現は,
$$
\~ρ(\~S)_{(jα)(kβ)} = e^{iπ/4} \frac1{\sqrt{M}} e^{\frac{2πi}{M} \qty{(j+1)k+(1-α_1)β_1}} δ_{α_2,β_1} δ_{1-α_1,β_2},
$$
$$
\~ρ(\~T)_{(jα)(kβ)} = e^{\frac{πi}{M} (j+α_1)(j-α_1+M)} δ_{j,k} δ_{α_1,β_1} δ_{β_2,α_2-α_1+\frac{M}{2}}^{({\rm mod}\ 1)}.
$$
{#eq:rho_T}
これは $M = {\rm even}$ のとき $(α_1,α_2)=(0,0)$ で, $M = {\rm odd}$ のとき $(α_1,α_2)=(\frac12,\frac12)$ で, 添字 $j$ を足とした表現として閉じている.

## SS phase $α_1,α_2 = 0, \frac12$ のとき

### 境界条件を満たす基底

3-point coupling ([@eq:yukawa]) が non-zero になる条件は[@eq:rule_SS; @eq:rule_jkl] の
$$
\begin{gathered}
  α_1 + β_1 = γ_1 \mod 1, \\
  α_2 + β_2 = γ_2 \mod 1, \\
  (j+α_1)+(k+β_1) = (ℓ+γ_1) \mod \gcd(M, N).
\end{gathered}
$$
1つ目の条件を満たす $(α_1β_1γ_1)$ の組は $(000)$, $(0\frac12\frac12)$, $(\frac120\frac12)$, $(\frac12\frac120)$ の3通りのみで, その上で $α_2$, $β_2$ を適当に振ったときに制限を満たす項を持つのは以下の16通り.

| $(α_1α_2)$ | $(β_1β_2)$ | $(γ_1γ_2)$ | # | $j + k - ℓ$ | $(j+α_1)+(k+β_1)-(ℓ+γ_1)$ |
| :-: | :-: | :-: | :-: | :-: | :-: |
| $(00)$/$(0\frac12)$ | $(00)$/$(0\frac12)$ | $(0γ_2)$ | 4 | $0$ | $0$ |
| $(00)$/$(0\frac12)$ | $(\frac120)$/$(\frac12\frac12)$ | $(\frac12γ_2)$ | 4 | $0$ | $0$ |
| $(\frac120)$/$(\frac12\frac12)$ | $(00)$/$(0\frac12)$ | $(\frac12γ_2)$ | 4 | $0$ | $0$ |
| $(\frac120)$/$(\frac12\frac12)$ | $(\frac120)$/$(\frac12\frac12)$ | $(0γ_2)$ | 4 | $-1$ | $0$ |
: [@eq:rule_SS] を満たす SS phase の組み合わせと $jkℓ$ の条件([@eq:rule_jkl]). $γ_2$ は $α_2$, $β_2$ で一通りに決まる phase.

右の2列について, $j + k - ℓ$ については
$$
j + k - ℓ = 0 \mod \gcd(M, N)
$$
は既知であり, 最下段
$$
j + k - ℓ = -1 \mod \gcd(M, N)
$$
が整数 SS phase の時には無かった選択則. ただし,
$$
(j+α_1)+(k+β_1)-(ℓ+γ_1) = 0 \mod \gcd(M, N)
$$
と見て $j+α_1$ をまとめてモードだと思えば今までと同じ選択則.

### T不変な基底

#### $M = {\rm odd}$

$M = {\rm odd}$ のとき $M = 1$. T 変換([@eq:rho_T])は
$$
\~ρ(\~T)_{(iα)(jβ)} = e^{\frac{πi}{M} (i+α_1)(i-α_1+1)} δ_{i,j} δ_{α_1,β_1} δ_{β_2,α_2-α_1+\frac{1}{2}}^{({\rm mod}\ 1)}
$$
であるから, 添字の組 $iα ≡ i(α_1,α_2)$ を足としたときのT変換の表現行列は
$$
\begin{array}{c}
  i(0,0) \\
  i(0,\frac12) \\
  i(\frac12,0) \\
  i(\frac12,\frac12) \\
\end{array}
\left(
  \begin{array}{cc:cc}
    0   & A_i & 0   & 0   \\
    A_i & 0   & 0   & 0   \\ \hdashline
    0   & 0   & B_i & 0   \\
    0   & 0   & 0   & B_i \\
  \end{array}
\right)
$$
の形になる. ただし, $A_i = e^{\frac{πi}{M}i(i+1)}$, $B_i = e^{\frac{πi}{M} (i+\frac12)(i-\frac12+1)} = e^{\frac{πi}{M} (i+\frac12)^2}$. したがって, T変換を対角化するような基底は
$$
\begin{aligned}
  Ψ^{i(0,±),M}(z,τ) &≡ ψ^{(i+0,0),M}(z,τ) ± ψ^{(i+0,\frac12),M}(z,τ), \\
  Ψ^{i(\frac12,α_2),M}(z,τ) &≡ ψ^{(i+\frac12,α_2),M}(z,τ), \\
\end{aligned}
$$
{#eq:basis_odd}
T変換の固有値はそれぞれ
$$
T Ψ^{i(0,±),M} = ± A_i Ψ^{i(0,±),M}, \quad T Ψ^{i(\frac12,α_2),M} = B_i Ψ^{i(\frac12,α_2),M}.
$$

新しい基底 $Ψ^{iα,M}$ を取ったとき, 3-point coupling ([@eq:yukawa]) が non-zero になる条件を考える. SS phase の制限 $α + β = γ \mod 1$ ([@eq:rule_SS])について, $(α_1β_1γ_1)$ の組は $(000)$, $(0\frac12\frac12)$, $(\frac12\frac120)$ の3通りのみだから, その上で $α_2$, $β_2$ を適当に振ったときに制限を満たす項を持つのは以下の32通り.

| $(α_1α_2)$ | $(β_1β_2)$ | $(γ_1γ_2)$ | # | $j + k - ℓ$ | $(j+α_1)+(k+β_1)-(ℓ+γ_1)$ |
| :-: | :-: | :-: | :-: | :-: | :-: |
| $(0+)$/$(0-)$ | $(0+)$/$(0-)$ | $(0+)$/$(0-)$ | 8 | $0$ | $0$ |
| $(0+)$/$(0-)$ | $(\frac120)$/$(\frac12\frac12)$ | $(\frac120)$/$(\frac12\frac12)$ | 8 | $0$ | $0$ |
| $(\frac120)$/$(\frac12\frac12)$ | $(0+)$/$(0-)$ | $(\frac120)$/$(\frac12\frac12)$ | 8 | $0$ | $0$ |
| $(\frac120)$/$(\frac12\frac12)$ | $(\frac120)$/$(\frac12\frac12)$ | $(0+)$/$(0-)$ | 8 | $-1$ | $0$ |
:$M = {\rm odd}$ のときに[@eq:rule_SS]を満たす SS phase の組み合わせと $jkℓ$ の条件([@eq:rule_jkl]).

#### $M = {\rm even}$

$M = {\rm even}$ のとき $M = 0$. T 変換([@eq:rho_T])は
$$
\~ρ(\~T)_{(iα)(jβ)} = e^{\frac{πi}{M} (i+α_1)(i-α_1)} δ_{i,j} δ_{α_1,β_1} δ_{β_2,α_2-α_1}
$$
であるから, 添字の組 $iα ≡ i(α_1,α_2)$ を足としたときのT変換の表現行列は
$$
\begin{array}{c}
  i(0,0) \\
  i(0,\frac12) \\
  i(\frac12,0) \\
  i(\frac12,\frac12) \\
\end{array}
\left(
  \begin{array}{cc:cc}
    A'_i& 0   & 0   & 0   \\
    0   & A'_i& 0   & 0   \\ \hdashline
    0   & 0   & 0   & B'_i\\
    0   & 0   & B'_i& 0   \\
  \end{array}
\right)
$$
の形になる. ただし, $A'_i = e^{\frac{πi}{M}i^2}$, $B'_i = e^{\frac{πi}{M} (i+\frac12)(i-\frac12)}$. したがって, T変換を対角化するような基底は
$$
\begin{aligned}
  Ψ^{i(0,α_2),M}(z,τ) &≡ ψ^{(i+0,α_2),M}(z,τ), \\
  Ψ^{i(\frac12,±),M}(z,τ) &≡ ψ^{(i+\frac12,0),M}(z,τ) ± ψ^{(i+\frac12,\frac12),M}(z,τ), \\
\end{aligned}
$$
{#eq:basis_even}
T変換の固有値はそれぞれ
$$
T Ψ^{i(0,α_2),M} = A'_i Ψ^{i(0,α_2),M}, \quad T Ψ^{i(\frac12,±),M} = ± B'_i Ψ^{i(\frac12,±),M}.
$$

3-point coupling ([@eq:yukawa]) が non-zero になる $(αβγ)$ の組は以下の28通り. ただし, 最上段の $γ_2$ は, $α_2$, $β_2$ の選択によって必然的に選択される phase.

| $(α_1α_2)$ | $(β_1β_2)$ | $(γ_1γ_2)$ | # | $j + k - ℓ$ | $(j+α_1)+(k+β_1)-(ℓ+γ_1)$ |
| :-: | :-: | :-: | :-: | :-: | :-: |
| $(00)$/$(0\frac12)$ | $(00)$/$(0\frac12)$ | $(0γ_2)$ | 4 | $0$ | $0$ |
| $(00)$/$(0\frac12)$ | $(\frac12+)$/$(\frac12-)$ | $(\frac12+)$/$(\frac12-)$ | 8 | $0$ | $0$ |
| $(\frac12+)$/$(\frac12-)$ | $(00)$/$(0\frac12)$ | $(\frac12+)$/$(\frac12-)$ | 8 | $0$ | $0$ |
| $(\frac12+)$/$(\frac12-)$ | $(\frac12+)$/$(\frac12-)$ | $(00)$/$(0\frac12)$ | 8 | $-1$ | $0$ |
:$M = {\rm even}$ のときに[@eq:rule_SS]を満たす SS phase の組み合わせと $jkℓ$ の条件([@eq:rule_jkl]). $γ_2$ は $α_2$, $β_2$ で一通りに決まる phase.

## 証明集

### テータ関数の積の公式([@eq:theta_product])の証明

まず, 定義式を代入して,
$$
\begin{aligned}
  ({\rm LHS})
    &= ∑_{n_1,n_2∈ℤ} e^{πi \pqty{n_1+\frac{a_1}{c_1}}^2 c_1τ} e^{2πi \pqty{n_1+\frac{a_1}{c_1}} (c_1z+b_1)} e^{πi \pqty{n_2+\frac{a_2}{c_2}}^2 c_2τ} e^{2πi \pqty{n_2+\frac{a_2}{c_2}} (c_2z+b_2)} \\
    &= ∑_{n_1,n_2∈ℤ} e^{πi \bqty{\frac{\pqty{n_1c_1+a_1}^2}{c_1} + \frac{\pqty{n_2c_2+a_2}^2}{c_2}} τ} e^{2πi \bqty{(n_1c_1+a_1) + (n_2c_2+a_2)} z} e^{2πi \bqty{\frac{b_1(n_1c_1+a_1)}{c_1} + \frac{b_2(n_2c_2+a_2)}{c_2}}} \\
    &= ∑_{n_1,n_2∈ℤ} \exp\bqty{πi \pqty{\frac{N_1^2}{c_1} + \frac{N_2^2}{c_2}} τ + 2πi (N_1 + N_2) z + 2πi \pqty{\frac{b_1N_1}{c_1} + \frac{b_2N_2}{c_2}}}. \\
\end{aligned}
$$
ただし最後の行で $N_1 ≡ n_1c_1+a_1$, $N_2 ≡ n_2c_2+a_2$ と置いた. ここで以下の記法を導入する.
$$
\begin{aligned}
  &X = X_1 + X_2, \\
  &\~X = c_2 X_1 - c_1 X_2, \\
  &\=X = c_1 c_2 X, \\
  &X' = X/d, \quad d ≡ \gcd(c_1, c_2), \\
  &x = c_1 X_1 + c_2 X_2.
\end{aligned}
$$
この表記法と, 等式
$$
\frac{A_1B_1}{c_1} + \frac{A_2B_2}{c_2} = \frac{AB}{C} + \frac{\~A\~B}{\=C}
$$
を使えば, 左辺は
$$
\begin{aligned}
  ({\rm LHS})
    &= ∑_{n_1,n_2∈ℤ} \exp\bqty{πi \pqty{\frac{N^2}{C} + \frac{\~N^2}{\=C}} τ + 2πiNz + 2πi \pqty{\frac{BN}{C} + \frac{\~B\~N}{\=C}}} \\
    &= ∑_{n_1,n_2∈ℤ} \exp\bqty{πi \frac{\~N^2}{\=C} τ + 2πi\~N \pqty{0 + \frac{\~B}{\=C}}} \exp\bqty{πi \frac{N^2}{C} τ + 2πiN\pqty{z + \frac{B}{C}}} \\
\end{aligned}
$$
となって, $N$ と $\~N$ の部分に分離できる. 次に変数 $(n_1,n_2)∈ℤ×ℤ$ をこれらに対応する別の変数に変換することを考える. $N$ と $\~N$ は定義から
$$
\begin{aligned}
  &N = (n_1c_1+a_1) + (n_2c_2+a_2) = n + A, \\
  &\~N = c_2(n_1c_1+a_1) - c_1(n_2c_2+a_2) = c_1c_2(n_1 - n_2) + \~A.
\end{aligned}
$$
ただし, 表記法より $n = n_1c_1 + n_2c_2$. フラックス $c_1$ と $c_2$ の最大公約数を $d ≡ \gcd(c_1,c_2)$ とすれば, 明らかに $n$ は $d$ の倍数である. これを踏まえて $(n_1,n_2)$ を以下のように変数を変換する.

1. $(n_1, n_2) → (n, k) ∈ dℤ×ℤ$: Bézout の補題から, 整数の等式
    $$
    n_{1} c_1 + n_{2} c_2 = n
    $$
    の特殊解 $(n_1,n_2) = (n_{10},n_{20})$ が存在し, 一般解は
    $$
    (n_1,n_2) = (n_{10} + c_2'k, n_{20} - c_1'k), \quad k∈ℤ
    $$
    である. ただし, 表記法より $c_i = c_i'd$ i.e. $\gcd(c_1',c_2')=1$. また,
    $$
    p_1c'_1 + p_2c'_2 = 1
    $$
    となる $(p_1, p_2) = (p_{10}, p_{20})$ を一つ選んできて, $(n_{10}, n_{20}) = (p_{10}n', p_{20}n')$ とすればこれは解となるから, 以下では $(p_1, p_2)$ を使って
    $$
    (n_1,n_2) = (n'p_{10} + c_2'k, n'p_{20} - c_1'k), \quad k∈ℤ
    $$
    と書く.
2. $(n, k) → (k, m_2, ℓ) ∈ ℤ × ℤ × \{0, 1, ..., C'-1\}$: $n$ は $d$ の倍数であるから, $n'$ は整数. これを $C'$ で割った商と余りをそれぞれ $m_2$, $ℓ$ とする. つまり,
    $$
    n' = (c_1' + c_2') m_2 + ℓ, \quad m_2 ∈ ℤ, \quad ℓ = 0, 1, ..., c_1' + c_2' - 1.
    $$
3. $(k, m_2, ℓ) → (m_1, m_2, ℓ) ∈ ℤ × ℤ × \{0, 1, ..., C'-1\}$: ここまでの変数変換を $N$, $\~N$ に代入すると
    $$
      N = (C'm_2 + ℓ) d + A = Cm_2 + dℓ + A,
    $$
    $$
    \begin{aligned}
      \~N
        &= c_1c_2[(n'p_{10} + c_2'k) - (n'p_{20} - c_1'k)] + \~A \\
        &= c_1c_2n'(p_{10} - p_{20}) + \=C'k + \~A \\
        &= c_1c_2(C'm_2+ℓ)(p_{10} - p_{20}) + \=C'k + \~A \\
        &= \=C'[k + m_2(p_{10} - p_{20})] + (p_{10} - p_{20})\bar{ℓ} + \~A. \\
    \end{aligned}
    $$
    ここで, $k + m_2(p_{10} - p_{20})$ は $m_2$ を固定すれば整数全体を走るから, これを $m_1$ とおく. 結局
    $$
    \~N = \=C'm_1 + (p_{10} - p_{20})\bar{ℓ} + \~A, \quad m_1 ∈ ℤ.
    $$
4. $(m_1, m_2, ℓ) → (m_1, m_2, r) ∈ ℤ × ℤ × \{0, 1, ..., C'-1\}$: $r ≡ (p_{10} - p_{20}) ℓ \mod C'$ とする. つまり, ある整数 $s$ が存在して,
    $$
    (p_{10} - p_{20}) ℓ = r + s C', \quad r = 0, 1, ..., c_1' + c_2' - 1.
    $$
    ここで, $c_1'p_{10} = 1 - c_2'p_{20}$ より,
    $$
    c_1'(p_{10}-p_{20}) = 1 - c_2'p_{20} - c_1'p_{20} = 1 - C'p_{20}
    $$
    だから,
    $$
    c_1'r = c_1'(p_{10}-p_{20})ℓ - c_1'sC' = (1 - C'p_{20})ℓ - c_1'sC' = ℓ - (p_{20}ℓ + c_1's)C'
    $$
    より, 整数 $t = p_{20}ℓ + c_1's$ に対して
    $$
    ℓ = c_1'r + tC'.
    $$
    これらを使って $N$ と $\~N$ を整理すると,
    $$
    N = C \pqty{m_2 + \frac{c_1r + A}{C} + t}, \quad \~N = \=C'\pqty{m_1 + \frac{\=r + \~A}{\=C'} + s}.
    $$

結局, 変数変換 $(n_1, n_2) → (m_1, m_2, r)$ によって, 示したい式の左辺は
$$
\begin{aligned}
  ({\rm LHS})
    &= ∑_{r=0}^{C'-1} ∑_{m_1,m_2∈ℤ} \exp\bqty{πi \frac{\~N^2}{\=C} τ + 2πi\~N \pqty{0 + \frac{\~B}{\=C}}} \exp\bqty{πi \frac{N^2}{C} τ + 2πiN\pqty{z + \frac{B}{C}}} \\
    &= ∑_{r=0}^{C'-1} ∑_{m_1∈ℤ} \exp\bqty{πi \pqty{m_1 + \frac{\=r + \~A}{\=C'} + s}^2 \=C'' τ + 2πi \pqty{m_1 + \frac{\=r + \~A}{\=C'} + s} \pqty{0 + \~B'}} \\
    & \qquad × ∑_{m_2∈ℤ} \exp\bqty{πi \pqty{m_2 + \frac{c_1r + A}{C} + t}^2 Cτ + 2πi \pqty{m_2 + \frac{c_1r + A}{C} + t}\pqty{Cz + B}} \\
    &= ∑_{r=0}^{C'-1} ϑ\bmqty{\frac{\=r + \~A}{\=C'} + s \\ \~B'}(0, \=C''τ) × ϑ\bmqty{\frac{c_1r + A}{C} + t \\ B}(Cz, Cτ) \\
    &= ∑_{r=0}^{C'-1} ϑ\bmqty{\frac{\=r + \~A}{\=C'} \\ \~B'}(0, \=C''τ) × ϑ\bmqty{\frac{c_1r + A}{C} \\ B}(Cz, Cτ) \quad (∵s,t∈ℤ) \\
\end{aligned}
$$
となって, 公式が得られた.

## テータ関数の直交性の公式([@eq:theta_orthogonal])の証明

まず, 定義を代入して
$$
\begin{aligned}
  ({\rm LHS})
    &= ∫_{T^2} dz d\=z \exp\qty{\frac{π i}{\Im τ} (c_1z-c_2\=z) \Im z} ϑ\bmqty{a_1/c_1 \\ b_1}(c_1 z, c_1 τ) \overline{ϑ\bmqty{a_2/c_2 \\ b_2}(c_2 z, c_2 τ)} \\
    &= ∑_{n_1,n_2∈ℤ} ∫_{T^2} dz d\=z e^{\frac{π i}{\Im τ} (c_1z-c_2\=z) \Im z} \\
    & \qquad × e^{πi \pqty{n_1 + \frac{a_1}{c_1}}^2 c_1τ} e^{2πi \pqty{n_1 + \frac{a_1}{c_1}}(c_1z + b_1)} × e^{-πi \pqty{n_2 + \frac{a_2}{c_2}}^2 c_2\=τ} e^{- 2πi \pqty{n_2 + \frac{a_2}{c_2}}(c_2\=z + b_2)} \\
    &= e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} ∑_{n_1,n_2∈ℤ} ∫_{T^2} dz d\=z e^{\frac{π i}{\Im τ} (c_1z-c_2\=z) \Im z + πi \bqty{\frac{(n_1c_1+a_1)^2}{c_1}τ - \frac{(n_2c_2+a_2)^2}{c_2}\=τ}} \\
    & \qquad × e^{2πi[(n_1c_1+a_1)z - (n_2c_2+a_2)\=z] + 2πi (b_1 n_1 - b_2 n_2)} \\
\end{aligned}
$$
ここで, $c_1≠c_2$ のとき, $z→z+1$ で指数関数の肩の第一項が不変でない($z$ 依存性が残る)から, 被積分関数がトーラス上で一価でない. したがって, $c_1 = c_2$ が要求され,
$$
\begin{aligned}
  ({\rm LHS})
    &= e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} ∫_{T^2} dz d\=z e^{- \frac{2π c_1}{\Im τ} (\Im z)^2 + \frac{πi}{c_1} \bqty{(n_1c_1+a_1)^2τ - (n_2c_1+a_2)^2\=τ}} \\
    & \qquad \qquad \qquad \qquad \qquad × e^{2πi[(n_1c_1+a_1)z - (n_2c_1+a_2)\=z] + 2πi(b_1 n_1 - b_2 n_2)}. \\
\end{aligned}
$$
$z=x+τy$ とおいて, $dzd\=z = (\Im τ) dxdy$ に注意すれば,
$$
\begin{aligned}
  ({\rm LHS})
    &= (\Im τ) e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} ∫_0^1 dx ∫_0^1 dy e^{- \frac{2π c_1}{\Im τ} (\Im τ)^2 y^2 + \frac{πi}{c_1} \bqty{(n_1c_1+a_1)^2τ - (n_2c_1+a_2)^2\=τ}} \\
    & \qquad \qquad \qquad \qquad \qquad × e^{2πi[(n_1c_1+a_1)(x+τy) - (n_2c_1+a_2)(x+\=τy)] + 2πi(b_1 n_1 - b_2 n_2)} \\
    &= (\Im τ) e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} ∫_0^1 dx e^{2πi[a_1 - a_2 + (n_1 - n_2)c_1]x} \\
    & \quad × ∫_0^1 dy e^{- \frac{2π c_1}{\Im τ} (\Im τ)^2 y^2 + 2πi[(n_1c_1+a_1)τ - (n_2c_1+a_2)\=τ]y + \frac{πi}{c_1} \bqty{(n_1c_1+a_1)^2τ - (n_2c_1+a_2)^2\=τ} + 2πi(b_1 n_1 - b_2 n_2)}. \\
\end{aligned}
$$
ここで $∫_0^1 dx e^{2πi(p-q)x} = δ_{p,q}$ (ただし $p-q∈ℤ$ を仮定)だから, $x$ 積分を実行して
$$
∫_0^1 dx e^{2πi[a_1 - a_2 + (n_1 - n_2)c_1]x} = δ_{a_1, a_2-(n_1-n_2)c_1}.
$$
したがって,
$$
\begin{aligned}
  ({\rm LHS})
    &= (\Im τ) e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} δ_{a_1, a_2 - (n_1 - n_2)c_1} \\
    & \quad × ∫_0^1 dy e^{- \frac{2π c_1}{\Im τ} (\Im τ)^2 y^2 + 2πi[(n_1c_1+a_1)τ - (n_2c_1+a_2)\=τ]y + \frac{πi}{c_1} \bqty{(n_1c_1+a_1)^2τ - (n_2c_1+a_2)^2\=τ} + 2πi(b_1 n_1 - b_2 n_2)} \\
    &= (\Im τ) e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} δ_{a_1, a_2 - (n_1 - n_2)c_1} \\
    & \quad × ∫_0^1 dy e^{- 2π c_1 (\Im τ) y^2 - 4π (\Im τ) (n_1c_1+a_1) y - \frac{2π}{c_1} (\Im τ) (n_1c_1+a_1)^2 + 2πi(b_1 n_1 - b_2 n_2)} \\
    &= (\Im τ) e^{2πi \pqty{\frac{a_1b_1}{c_1} - \frac{a_2b_2}{c_2}}} δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} δ_{a_1, a_2 - (n_1 - n_2)c_1} \\
    & \quad × ∫_0^1 dy e^{- 2π c_1 (\Im τ) \pqty{y + n_1 + \frac{a_1}{c_1}}^2 + 2πi(b_1 n_1 - b_2 n_2)} \\
    &= (\Im τ) δ_{c_1,c_2} ∑_{n_1,n_2∈ℤ} δ_{a_1, a_2 - (n_1 - n_2)c_1} e^{2πi(b_1 - b_2) \pqty{n_1 + \frac{a_1}{c_1}}} ∫_0^1 dy e^{- 2π c_1 (\Im τ) \pqty{y + n_1 + \frac{a_1}{c_1}}^2}. \\
\end{aligned}
$$
ここで $m ≡ n_2 - n_1$ と置いて $n_2$ の総和を $m$ についての総和に直せば,
$$
∑_{n_1,n_2∈ℤ} δ_{a_1, a_2 - (n_1 - n_2)c_1} = ∑_{m∈ℤ} δ_{a_1, a_2 + mc_1}
$$
となって, これは $n_1$ によらない. これを $δ_{a_1,a_2}^{({\rm mod}\ c_1)}$ と書くことにする. また仮定より $b_1-b_2∈ℤ$ だから $e^{2πi(b_1 - b_2) n_1} = 1$. したがって,
$$
\begin{aligned}
  ({\rm LHS})
    &= (\Im τ) e^{2πi \frac{a_1}{c_1} (b_1 - b_2)} δ_{c_1,c_2} δ_{a_1,a_2}^{({\rm mod}\ c_1)} ∑_{n_1∈ℤ} ∫_0^1 dy e^{- 2π c_1 (\Im τ) \pqty{y + n_1 + \frac{a_1}{c_1}}^2}. \\
\end{aligned}
$$
最後に $∑_{n_1∈ℤ} ∫_0^1 dy f(y+n_1) = ∫_{-∞}^{∞} dy f(y)$ に注意して $y$ 積分を実行すれば,
$$
\begin{aligned}
  ({\rm LHS})
    &= (\Im τ) e^{2πi \frac{a_1}{c_1} (b_1 - b_2)} δ_{c_1,c_2} δ_{a_1,a_2}^{({\rm mod}\ c_1)} ∫_{-∞}^{∞} dy e^{- 2π c_1 (\Im τ) \pqty{y + \frac{a_1}{c_1}}^2} \\
    &= (\Im τ) e^{2πi \frac{a_1}{c_1} (b_1 - b_2)} δ_{c_1,c_2} δ_{a_1,a_2}^{({\rm mod}\ c_1)} \frac1{\sqrt{2c_1 \Im τ}} \\
    &= \sqrt{\frac{\Im τ}{2c_1}} e^{2πi \frac{a_1}{c_1} (b_1 - b_2)} δ_{c_1,c_2} δ_{a_1,a_2}^{({\rm mod}\ c_1)} \\
\end{aligned}
$$
となって右辺が得られた.

## テータ関数のT変換 ([@eq:theta_t]) の証明

左辺を定義で展開して
$$
\begin{aligned}
  ({\rm LHS})
    &= ∑_{ℓ∈ℤ} e^{πi\pqty{ℓ+\frac{a}{c}}^2 c(τ+1)} e^{2πi \pqty{ℓ+\frac{a}{c}}(cz+b)} \\
    &= ∑_{ℓ∈ℤ} e^{πi\pqty{ℓ+\frac{a}{c}}^2 c} e^{πi\pqty{ℓ+\frac{a}{c}}^2 cτ} e^{2πi \pqty{ℓ+\frac{a}{c}}(cz+b)}. \\
\end{aligned}
$$
一つ目の指数関数の肩を変形して,
$$
\begin{aligned}
  \exp\bqty{πi\pqty{ℓ+\frac{a}{c}}^2 c}
    &= \exp\bqty{πi\pqty{ℓ^2 + 2ℓ\frac{a}{c} + \frac{a^2}{c^2}} c} \\
    &= \exp\bqty{πicℓ(ℓ+1) + 2πiℓ\pqty{a - \frac{c}{2}} + πi\frac{a^2}{c}} \\
    &= \exp\bqty{πicℓ(ℓ+1) + 2πi\pqty{ℓ + \frac{a}{c}}\pqty{a - \frac{c}{2}} + \frac{πi}{c}a(c-a)}. \\
\end{aligned}
$$
ここで, $ℓ(ℓ+1)$ は必ず偶数だから落ちる. したがって,
$$
\begin{aligned}
  ({\rm LHS})
    &= e^{\frac{πi}{c}a(c-a)} ∑_{ℓ∈ℤ} e^{πi\pqty{ℓ+\frac{a}{c}}^2 c} e^{πi\pqty{ℓ+\frac{a}{c}}^2 cτ} e^{2πi \pqty{ℓ+\frac{a}{c}}\pqty{cz+b+a-\frac{c}{2}}} \\
    &= e^{\frac{πi}{c}a(c-a)} ϑ\bmqty{a/c \\ b + a - c/2}(cz,cτ) \\
\end{aligned}
$$
となって1行目の右辺が得られる.

$a$, $b$ を離散的と仮定する. ある $n$ で等分割して, $(a,b) = (p/n,q/n)$ ($p,q=0,1,...,n-1$) と書くと,
$$
\begin{aligned}
  ({\rm LHS})
    &= e^{\frac{πi}{c}\frac{p}{n}\pqty{c-\frac{p}{n}}} ϑ\bmqty{\frac{p/n}{c} \\ q/n + p/n - c/2}(cz,cτ) \\
    &= ∑_{p',q'∈ℤ} δ_{\frac{p}{n},\frac{p'}{n}} δ_{\frac{q}{n},\frac{q'}{n} - \frac{p'}{n} + \frac{c}{2}} e^{\frac{πi}{c}\frac{p'}{n}\pqty{c-\frac{p'}{n}}} ϑ\bmqty{\frac{p'/n}{c} \\ q'/n}(cz,cτ). \\
\end{aligned}
$$
ここで, $p$ に関する Kronecker のデルタから $p'$ の総和は $p'=0,1,...,n-1$ の範囲しか寄与しない. また, $q' = q'' + mn$ ($q'' = 0,1,...,n-1$) と置換して,
$$
\begin{aligned}
  ({\rm LHS})
    &= ∑_{p',q''=0}^{n-1} ∑_{m∈ℤ} δ_{\frac{p}{n},\frac{p'}{n}} δ_{\frac{q}{n},\frac{q''}{n} + m - \frac{p'}{n} + \frac{c}{2}} e^{\frac{πi}{c}\frac{p'}{n}\pqty{c-\frac{p'}{n}}} ϑ\bmqty{\frac{p'/n}{c} \\ q''/n + m}(cz,cτ) \\
    &= ∑_{p',q''=0}^{n-1} ∑_{m∈ℤ} δ_{\frac{p}{n},\frac{p'}{n}} δ_{\frac{q}{n},\frac{q''}{n} + m - \frac{p'}{n} + \frac{c}{2}} e^{\frac{πi}{c}\frac{p'}{n}\pqty{c-\frac{p'}{n}}} e^{2πi\frac{p'/n}{c}m} ϑ\bmqty{\frac{p'/n}{c} \\ q''/n}(cz,cτ) \\
    &= ∑_{p',q''=0}^{n-1} ∑_{m∈ℤ} δ_{\frac{p}{n},\frac{p'}{n}} δ_{\frac{q}{n},\frac{q''}{n} + m - \frac{p'}{n} + \frac{c}{2}} e^{\frac{πi}{c}\frac{p'}{n}\pqty{c-\frac{p'}{n} + 2m}} ϑ\bmqty{\frac{p'/n}{c} \\ q''/n}(cz,cτ). \\
\end{aligned}
$$
$(a',b') = (p'/n,q''/n)$ と書くことにすれば,
$$
\begin{aligned}
  ({\rm LHS})
    &= ∑_{a',b'} ∑_{m∈ℤ} δ_{a,a'} δ_{b,b' - a' + \frac{c}{2} + m} e^{\frac{πi}{c}a'\pqty{c - a' + 2m}} ϑ\bmqty{a'/c \\ b'}(cz,cτ) \\
\end{aligned}
$$
となって2行目の右辺が得られる.
