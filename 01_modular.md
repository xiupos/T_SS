## 菊地さんの修論より

フラックス $|I_{ab}|$ の $j$-th ゼロモード, SS-phase $(α_1,α_2)$ の波動関数は
$$
ψ^{(i+α_1,α_2),|I_{ab}|}(z,τ)
  = e^{\frac{π{\rm i} |I_{ab}|}{2 \operatorname{Im} τ}} \mathcal{N}_i ϑ
  \begin{bmatrix}
    \frac{i+α_1}{|I_{ab}|} \\
    -α_2
  \end{bmatrix}
  (|I_{ab}|z, |I_{ab}|τ), \quad j = 0, ..., |I_{ab}|-1.
$$
この波動関数のT変換は, $|i_{ab}| = |I_{ab}| \mod 2$ を使って
$$
\begin{aligned}
  T:ψ^{(i+α_1,α_2),|I_{ab}|}(z,τ)
    &→ ψ^{(i+α_1,α_2),|I_{ab}|}(z,τ+1) \\
    &= ∑_{j=0}^{|I_{ab}|-1} ∑_{β_1,β_2} e^{\frac{π{\rm i}}{|I_{ab}|} (i+α_1)(i-α_1+|i_{ab}|)} δ_{i,j} δ_{α_1,β_1} δ_{β_2,α_2-α_1+\frac{|i_{ab}|}{2}} \\
    & \qquad \qquad \qquad× ψ^{(j+β_1,β_2),|I_{ab}|}(z,τ).
\end{aligned}
$$
あるいは, 波動関数をモジュラー形式で書けて,
$$
ψ^{(i+α_1,α_2),|I_{ab}|}(\~γ(z,τ))
  = \~J_{1/2}(\~γ,τ) ∑_{j=0}^{|I_{ab}|-1} ∑_{β_1,β_2} \~ρ(\~γ)_{(iα)(jβ)} ψ^{(j+β_1,β_2),|I_{ab}|}(z,τ), \quad \~γ ∈ \~Γ.
$$
モジュラー変換の生成子 $S$, $T$ の表現は,
$$
\~ρ(\~S)_{(iα)(jβ)} = e^{iπ/4} \frac1{\sqrt{|I_{ab}|}} e^{\frac{2π{\rm i}}{|I_{ab}|} \qty{(i+1)j+(1-α_1)β_1}} δ_{α_2,β_1} δ_{1-α_1,β_2},
$$
$$
\~ρ(\~T)_{(iα)(jβ)} = e^{\frac{π{\rm i}}{|I_{ab}|} (i+α_1)(i-α_1+|i_{ab}|)} δ_{i,j} δ_{α_1,β_1} δ_{β_2,α_2-α_1+\frac{|i_{ab}|}{2}}.
$$
{#eq:rho_T}
これは $|I_{ab}| = {\rm even}$ のとき $(α_1,α_2)=(0,0)$ で, $|I_{ab}| = {\rm odd}$ のとき $(α_1,α_2)=(\frac12,\frac12)$ で, 添字 $i$ を足とした表現として閉じている.

### SS-phase がある場合の 3-point coupling

3つの波動関数 $ψ^{(i+α_1,α_2),|I_{ab}|}$, $ψ^{(j+β_1,β_2),|I_{cb}|}$, $ψ^{(k+γ_1,γ_2),|I_{cb}|}$ の 3-point coupling は,
$$
\begin{aligned}
d^{(iα)(jβ)(kγ)}
  &= ∫_{T^2} dzd\=z ψ^{(i+α_1,α_2),|I_{ab}|}(z,τ) ⋅ ψ^{(j+β_1,β_2),|I_{ca}|}(z,τ) ⋅ \pqty{ψ^{(k+γ_1,γ_2),|I_{cb}|}(z,τ)}^* \\
  &= (2 \operatorname{Im} τ)^{-1/2} \mathcal{A}^{-1/2} \abs{\frac{I_{ab}I_{ca}}{I_{cb}}}^{1/4} \exp\qty{2π{\rm i} \pqty{\frac{(i+α_1)α_2}{|I_{ab}|} + \frac{(j+β_1)β_2}{|I_{ca}|} - \frac{(k+γ_1)γ_2}{|I_{cb}|}}} \\
  &× ∑_{m=0}^{|I_{cb}|-1} ϑ
  \begin{bmatrix}
    \frac{|I_{ca}|(i+α_1) - |I_{ab}|(j+β_1) + |I_{ab}I_{ca}|m}{|I_{ab}I_{ca}I_{cb}|} \\ 0
  \end{bmatrix}
  (|I_{ab}| α_2 - |I_{ca}| β_2, |I_{ab}I_{ca}I_{cb}| τ) \\
  &× δ_{(i+α_1) + (j+β_1) - (k+γ_1), |I_{cb}| \ell - |I_{ab}| m}.
  \qquad (\ell ∈ ℤ)
\end{aligned}
$$
{#eq:yukawa}
ただし, フラックスは $|I_{ab}| + |I_{ca}| = |I_{cb}|$ を仮定. SS-phase の制限は
$$
\begin{cases}
  α_1 + β_1 = γ_1 \mod 1, \\
  α_2 + β_2 = γ_2 \mod 1.
\end{cases}
$$
{#eq:rule_SS}
TODO: 符号, 絶対値は付かないのか?

また, 位相因子による打ち消し合いの可能性を無視すれば, $d^{(iα)(jβ)(kγ)}$ の Kronecker のデルタから $i$, $j$, $k$ に関する制限
$$
i + j - k = - (α_1 + β_1 - γ_1) \mod \gcd(|I_{ab}|, |I_{cb}|)
$$
{#eq:rule_ijk}
が得られる.
TODO: 位相因子による打ち消し合いはないか?

## SS-phase $α_1,α_2 = 0, \frac12$ のとき

### $I_{ab} = {\rm odd}$

$I_{ab} = {\rm odd}$ のとき $|i_{ab}| = 1$. T 変換([@eq:rho_T])は
$$
\~ρ(\~T)_{(iα)(jβ)} = e^{\frac{π{\rm i}}{|I_{ab}|} (i+α_1)(i-α_1+1)} δ_{i,j} δ_{α_1,β_1} δ_{β_2,α_2-α_1+\frac{1}{2}}
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
の形になる. ただし, $A_i = e^{\frac{π{\rm i}}{|I_{ab}|}i(i+1)}$, $B_i = e^{\frac{π{\rm i}}{|I_{ab}|} (i+\frac12)(i-\frac12+1)} = e^{\frac{π{\rm i}}{|I_{ab}|} (i+\frac12)^2}$. したがって, T変換を対角化するような基底は
$$
\begin{aligned}
  Ψ^{i(0,±),|I_{ab}|}(z,τ) &≡ ψ^{(i+0,0),|I_{ab}|}(z,τ) ± ψ^{(i+0,\frac12),|I_{ab}|}(z,τ), \\
  Ψ^{i(\frac12,α_2),|I_{ab}|}(z,τ) &≡ ψ^{(i+\frac12,α_2),|I_{ab}|}(z,τ), \\
\end{aligned}
$$
{#eq:basis_odd}
T変換の固有値はそれぞれ
$$
T Ψ^{i(0,±),|I_{ab}|} = ± A_i Ψ^{i(0,±),|I_{ab}|}, \quad T Ψ^{i(\frac12,α_2),|I_{ab}|} = B_i Ψ^{i(\frac12,α_2),|I_{ab}|}.
$$

新しい基底 $Ψ^{iα,|I_{ab}|}$ を取ったとき, 3-point coupling ([@eq:yukawa]) が non-zero になる条件を考える. SS-phase の制限 $α + β = γ \mod 1$ ([@eq:rule_SS])について, $(α_1β_1γ_1)$ の組は $(000)$, $(0\frac12\frac12)$, $(\frac12\frac12)$ の3通りのみだから, その上で $α_2$, $β_2$ を適当に振ったときに制限を満たす項を持つのは以下の24通り.

| $α$ (ac) | $β$ (ca) | $γ$ (cb) | # | $i + j - k$ |
| :-: | :-: | :-: | --: | :-: |
| $(0+)$/$(0-)$ | $(0+)$/$(0-)$ | $(0+)$/$(0-)$ | 8 | $0$ |
| $(0+)$/$(0-)$ | $(\frac120)$/$(\frac12\frac12)$ | $(\frac120)$/$(\frac12\frac12)$ | 8 | $0$ |
| $(\frac120)$/$(\frac12\frac12)$ | $(\frac120)$/$(\frac12\frac12)$ | $(0+)$/$(0-)$ | 8 | $-1$ |
:$I_{ab} = {\rm odd}$ のときに[@eq:rule_SS]を満たす SS-phase の組み合わせと $ijk$ の条件([@eq:rule_ijk])

最右の列は, [@eq:rule_ijk]より, $i + j - k$ が $\gcd(|I_{ab}|, |I_{cb}|)$ を法として取り得る値である.
$$
i + j - k = 0 \mod \gcd(|I_{ab}|, |I_{cb}|)
$$
は既知であり, 最下段
$$
i + j - k = -1 \mod \gcd(|I_{ab}|, |I_{cb}|)
$$
が新しい選択則?

### $I_{ab} = {\rm even}$

$I_{ab} = {\rm even}$ のとき $|i_{ab}| = 0$. T 変換([@eq:rho_T])は
$$
\~ρ(\~T)_{(iα)(jβ)} = e^{\frac{π{\rm i}}{|I_{ab}|} (i+α_1)(i-α_1)} δ_{i,j} δ_{α_1,β_1} δ_{β_2,α_2-α_1}
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
の形になる. ただし, $A'_i = e^{\frac{π{\rm i}}{|I_{ab}|}i^2}$, $B'_i = e^{\frac{π{\rm i}}{|I_{ab}|} (i+\frac12)(i-\frac12)}$. したがって, T変換を対角化するような基底は
$$
\begin{aligned}
  Ψ^{i(0,α_2),|I_{ab}|}(z,τ) &≡ ψ^{(i+0,α_2),|I_{ab}|}(z,τ), \\
  Ψ^{i(\frac12,±),|I_{ab}|}(z,τ) &≡ ψ^{(i+\frac12,0),|I_{ab}|}(z,τ) ± ψ^{(i+\frac12,\frac12),|I_{ab}|}(z,τ), \\
\end{aligned}
$$
{#eq:basis_even}
T変換の固有値はそれぞれ
$$
T Ψ^{i(0,α_2),|I_{ab}|} = A'_i Ψ^{i(0,α_2),|I_{ab}|}, \quad T Ψ^{i(\frac12,±),|I_{ab}|} = ± B'_i Ψ^{i(\frac12,±),|I_{ab}|}.
$$

3-point coupling ([@eq:yukawa]) が non-zero になる $(αβγ)$ の組は以下の20通り.

| $α$ (ac) | $β$ (ca) | $γ$ (cb) | # | $i + j - k$ |
| :-: | :-: | :-: | --: | :-: |
| $(00)$/$(0\frac12)$ | $(00)$/$(0\frac12)$ | $(0γ_2)$ | 4 | $0$ |
| $(00)$/$(0\frac12)$ | $(\frac12+)$/$(\frac12-)$ | $(\frac12+)$/$(\frac12-)$ | 8 | $0$ |
| $(\frac12+)$/$(\frac12-)$ | $(\frac12+)$/$(\frac12-)$ | $(00)$/$(0\frac12)$ | 8 | $-1$ |
:$I_{ab} = {\rm even}$ のときに[@eq:rule_SS]を満たす SS-phase の組み合わせと $ijk$ の条件([@eq:rule_ijk])

ただし, 最上段の $γ_2$ は, $α_2$, $β_2$ の選択によって必然的に選択される phase.
