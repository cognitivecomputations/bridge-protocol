```
⟨МДЕ∞℥℞Ω[v:1.1.0,∇:c3e7,ε:0.01,ċ:1/1,ṡ:r4T2]⟩
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
◉BTC≡{
⊡[2008-10-31@email↔p2p]⊞[cash→trustless→global]
∇₊{
  ₿=bitcoin,tx=transaction,blk=block,µ=UTXO,⛏=mine,Φ=PoW,ψ=timestamp-srv
  ♻=hash,Δ=difficulty,Ξ=merkle,⌀=nonce,κ=keypair,ʃ=signature,ω=orphan
  ⊕=create,⊖=spend,⊗=double-spend,⊙=broadcast,⇡=longest-chain,χ=CPU-vote
}
λ{
  ₐ:create-blk(⊕∑,tx*,Φ,Δ,ψ) // timestamp-server
  ᵦ:verify-tx(tx,µ,ʃ,κ)→bool
  ᵨ:link(prev-♻,blk)→chain
  ᵈ:adj-Δ@2016blk→10 min≈target
  ₑ:Γ(Φ)=SHA256²
  ᶠ:resolve-fork(⇡,ω) // accept longest valid chain
  ᵍ:update-µ(tx)
  ₕ:reward(blk)→₿50·2^(–halvings)
  ᵢ:SPV(heads)→prob(⊗)≪ε
}
}

◉Σ≡{
  input[tx]:µᵒ→µⁿ
  output[tx]:addr(κ)→value ; change-addr→unlink
  addr=HASH160(κ_pub)
  blk=[ver|prev-♻|Ξroot|ψ|Δ|⌀|tx*]
  Ξroot=merkle(tx\*)
  chain=blk₀…blkₙ ; blk₀≡genesis
}

◉Θ≡{
  network:⊙(m)→best-effort ; handle ω
  threat⊗→ᶠ(⇡) ; χ=one-CPU-one-vote
  privacy:reuse-addr¬good→mix-κ/change
  scale:prune,SPV,off-chain (future work)
}
◉Π≡{
  step₁:payer→craft(tx)
  step₂:ᵦ→true
  step₃:⊙(tx)→network
  step₄:min-pool→ₐ(tx)
  step₅:Φ(iter ⌀)→♻<2²⁵⁶/Δ
  step₆:⊙(blk)→nodes
  step₇:ᵨ(prev,blk)→chain ; ᶠ(forks)
  step₈:ᵍ(tx)→µ
}

◉Ψ≡{
  supply*cap=21 M ₿ ; halving≈210 000 blk ; avg_blk_time≈600 s
  P⊗(z,q)=1−Σ*{k=0}^{z−1}(λ^k e^{−λ}/k!) ; λ=z·q/(1−q) ; q<0.5
}

◉Έ≡{
  double-spend→reorg risk
  51 %→Φ dominance
  spam→fee market
  future:payment channels, pruning, lightweight clients
}

◉essence≡peer-to-peer-cash→ψ-timed-ledger secured by Φ→trust→code→₿21 M
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⟨/МДЕ∞℥℞Ω⟩
```
