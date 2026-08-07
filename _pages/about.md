---
layout: about
title: About
permalink: /
subtitle:

---

- 📅 Fri, July 31, 2026
- 📍 [Frances C. Arrillaga Alumni Center (326 Galvez St, Stanford, CA)](https://maps.app.goo.gl/VRgS4WshhgrDs5fFA) (Due to construction near the main entrance, please use the [side entrance off Campus Drive](https://maps.app.goo.gl/U5kYa7b9ugjurLuG7))
- **Parking**: Park at a "P" spot in the [Track house lot](https://maps.app.goo.gl/1iFm9UxbVaZLWmTH6) and pay as per the instructions posted at the parking lot. Please **DO NOT** park at the Galvez lot or at spots marked with letters other than "P".
- Co-located with the [Science of Blockchain Conference 2026](https://www.sbc-conference.com/2026/)

**Registration: Attendance is free but registration is mandatory. [Registration link](https://forms.gle/DX4zVUTguzwczpXaA)**

---

With a market capitalization of more than a trillion USD, Bitcoin is the world's largest cryptocurrency — yet its highly constrained programming environment limits its applications. Despite this, there is growing interest in building secure applications on Bitcoin, from faster and private payments to bridging Bitcoin to other blockchains. There is also a concerted effort to make Bitcoin post-quantum secure by upgrading its signature schemes. Meeting these challenges has spurred significant cryptographic innovation, with implications well beyond Bitcoin itself. This workshop showcases these advances and brings together researchers from academia and industry to tackle the open problems that remain.

---

**Organizers:**
- [Srivatsan Sridhar](https://ssrivatsan97.github.io) (University of California, Berkeley)
- [Sanjam Garg](https://people.eecs.berkeley.edu/~sanjamg/) (University of California, Berkeley)

---



<!-- **Speakers:**
- Ariel Futoransky and Sergio Lerner (Fairgate Labs) - From cut-and-choose to constant-size proofs of garbling correctness
- Dan Boneh (Stanford) - TBD
- David Heath (UIUC) - Duty-free bits: projectivizing garbling schemes
- Michel Abdalla ([[alloc]init]) - Implementable witness encryption from arithmetic affine determinant programs
- Robin Linus (Stanford, ZeroSync) - Shielded CSV: private and efficient client-side validation
- Srivatsan Sridhar (UC Berkeley) - BABE: verifying proofs on Bitcoin made 1000x cheaper
- William Wang (NYU) - Flock: SHA256 proving, fast enough for post-quantum Bitcoin
- Zeta Avarikioti (TU Vienna) - Ark: offchain transaction batching in Bitcoin
-->

---

**Schedule:**

<table class="schedule-table">
<tbody>
<tr><td class="time">9:30 – 9:55</td><td>Registration</td></tr>
<tr><td class="time">9:55 – 10:00</td><td>Welcome remarks</td></tr>
<tr><td class="time">10:00 – 10:30</td><td>
  <details>
    <summary><strong><a href="https://eprint.iacr.org/2026/065">BABE: Verifying proofs on Bitcoin made 1000x cheaper</a></strong> — Srivatsan Sridhar (UC Berkeley)</summary>
    <p><em>Endowing Bitcoin with the ability to verify succinct proofs has been a longstanding problem with important applications such as scaling Bitcoin and allowing the Bitcoin asset to be used in other blockchains trustlessly. It is a challenging problem due to the lack of expressiveness in the Bitcoin scripting language and the small Bitcoin block space. BitVM2 is the state-of-the-art verification protocol for Bitcoin used in several mainnets and testnets, but it suffers from very high on-chain Bitcoin transaction fees in the unhappy path (over $14,000 in a recent experiment). Recent research BitVM3 dramatically reduces this on-chain cost by using a garbled SNARK verifier circuit to shift most of the verification off-chain, but each garbled circuit is 42 Gibytes in size, so the off-chain storage and setup costs are huge. This paper introduces BABE, a new proof verification protocol on Bitcoin, which preserves BitVM3's savings of on-chain costs but reduces its off-chain storage and setup costs by three orders of magnitude. BABE uses a witness encryption scheme for linear pairing relations to verify Groth16 proofs. Since Groth16 verification involves non-linear pairings, this witness encryption scheme is augmented with a secure two-party computation protocol implemented using a very efficient garbled circuit for scalar multiplication on elliptic curves. The design of this garbled circuit builds on a recent work, Argo MAC, which gives an efficient garbling scheme to compute homomorphic MACs on such curves.</em></p>
  </details>
</td></tr>
<tr><td class="time">10:30 – 11:00</td><td>
  <details>
    <summary><strong><a href="https://eprint.iacr.org/2026/476">Duty-free bits: Projectivizing garbling schemes</a></strong> — David Heath (UIUC)</summary>
    <p><em>Starting with the seminal work on BitVM, techniques based on Yao’s Garbled Circuit (GC) have recently emerged as a key ingredient for constructing trust-minimized Bitcoin bridges. However, GC-based techniques are often expensive in that they involve the transmission and storage of large cryptographic encodings; a naive encoding for the problem at hand has size on the order of tens of gigabytes. Exciting recent works BABE (Garg et al.) and Argo MAC (Eagen and Lai) demonstrated substantial improvement by integrating Yao-style garbling with so-called decomposable affine randomized encodings (DAREs) aka information-theoretic garbled circuits (IT-GCs). This integration led to encodings on the order of tens of megabytes — dramatically improved, but still large. The bottleneck of these recent approaches is a need to convert the way values are encoded, from simple bit-by-bit Yao-style garbled labels to efficient IT-GC-style labels. This conversion is essential, as Yao-style labels have a simple property crucial to the Bitcoin setting — projectivity, which means input values are encoded in a straightforward bit-by-bit manner. Existing works take a natural approach to the conversion, leading to the need to transmit and store an encoding whose size grows roughly quadratically in the size of the labels output by the conversion.</em></p>
    <p><em>Our work combines and extends modern advances in garbled circuits to substantially improve this Yao-style to IT-GC-style label conversion, ultimately leading to an encoding that scales only linearly with the output labels — crossing the border is duty-free. We use our improved conversion technique as a drop-in replacement for the natural conversions used by prior works. At the cost of a modest increase in local computation, we improve the total size of the garbled encoding for BABE (resp. Argo MAC) by 45x (resp. 20x).</em></p>
    <p><em>This work was completed in collaboration with Alpen.</em></p>
  </details>
</td></tr>
<tr><td class="time">11:00 – 11:30</td><td>Coffee break</td></tr>
<tr><td class="time">11:30 – 12:00</td><td>
  <details>
    <summary><strong>From cut-and-choose to constant-size proofs of garbling correctness</strong> — Ariel Futoransky and Sergio Lerner (Fairgate Labs)</summary>
    <p><em>Garbled circuits underpin a growing class of Bitcoin protocols — bridges, vaults, and covenant-like constructions — that express rich spending conditions without consensus changes. These rest on garbling correctness: a verifier must be convinced that a garbled circuit was produced honestly from an agreed Boolean circuit. The standard tool is cut-and-choose, in which the garbler commits to many circuit copies and opens a random subset; verifier communication and storage therefore grow as O(k·n) in the security parameter k and circuit size n.</em></p>
    <p><em>We replace cut-and-choose with a direct succinct proof. Given a public Boolean circuit and a commitment to the garbled tables, we prove that the committed tables are a correct garbling of the circuit under a Free-XOR scheme, and recursively compose per-gate local proofs into a single final artifact. Verification then costs O(1) in added communication and storage, independent of n, for arbitrary circuits.</em></p>
    <p><em>We present the construction and two implementations: a STARK-recursive prover for Free-XOR garbled circuits, and a Nova-based IVC prover for the same garbling-correctness statement, with the STARK prover reaching 25k gates/s on commodity hardware.</em></p>
  </details>
</td></tr>
<tr><td class="time">12:00 – 12:30</td><td>
  <details>
    <summary><strong><a href="https://eprint.iacr.org/2026/175"> Improving Bitcoin's Programmability via Witness Encryption</a></strong> — Michel Abdalla ([[alloc]init])</summary>
    <p><em>Bitcoin's limited scripting language and the lack of covenant-enabling opcodes significantly restrict its programmability. In this talk, we present Bitcoin PIPEs v2, a cryptographic approach to improving Bitcoin's programmability without requiring consensus changes. PIPEs v2 use witness encryption to encrypt a Bitcoin signing key under an NP statement, allowing it to be recovered only upon presenting a valid witness, such as a SNARK proof. The recovered key can then produce an ordinary Schnorr signature, making the resulting transaction indistinguishable from a standard Bitcoin spend. We then describe a concrete candidate instantiation based on Arithmetic Affine Determinant Programs (AADPs), a new witness encryption construction designed to natively support arithmetic constraints and efficient SNARK verification. Finally, we discuss ongoing work on the security of AADPs and the current state of their cryptanalysis.This talk is based on our ePrint papers <a href="https://ia.cr/2026/175">2026/175</a> and <a href="https://ia.cr/2026/186">2026/186</a>.</em></p>
  </details>
</td></tr>
<tr><td class="time">12:30 – 2:00</td><td>Lunch break</td></tr>
<tr><td class="time">2:00 – 2:30</td><td>
  <details>
    <summary><strong>Post-quantum Signatures for Blockchains</strong> — Dan Boneh (Stanford)</summary>
    <p><em>Due to the looming quantum threat, some major blockchains are planning to transition to post-quantum hash-based signatures.  These signatures lack some capabilities that blockchains are accustomed to.  This work aims to fill in some of the gaps.  This is joint work with Benedikt Bünz, Justin D., Yavor Litchev, and Kamilla Nazirkhanova.</em></p>
  </details>
</td></tr>
<tr><td class="time">2:30 – 3:00</td><td>
  <details>
    <summary><strong><a href="https://eprint.iacr.org/2026/1329.pdf">Flock: SHA256 proving, fast enough for post-quantum Bitcoin</a></strong> — William Wang (NYU)</summary>
    <p><em>For many applications of SNARKs, a key bottleneck is proving large batches of standard
    cryptographic hash evaluations, such as SHA-256, Keccak, or BLAKE3. We introduce Flock, a
    hash-based SNARK for extremely fast proving of such batched Boolean computations. Flock
    proves batches of the same R1CS circuit (plus input/output relations between them), can prove
    hash-chains and Merkle path openings, and in principle can be extended to full-fledged hash-
    based signature verification. At its core, Flock combines new optimizations for the lincheck and
    zerocheck protocols with an aggressively optimized proof-of-concept implementation co-designed
    by coding agents.</em></p>
    <p><em>On a single core of an M4 Max processor, Flock proves 82k evaluations of the BLAKE3
    compression function, 42k SHA-256 compressions, and 30k Keccak permutations per second —
    less than a 250x overhead over native execution. On ten cores, throughput exceeds 660k BLAKE3
    compressions per second; in proving SHA-256, Flock is more than 9x faster than Binius64, the
    prior state of the art, and more than 500x faster than the fastest elliptic curve-based SNARK
    we measured against.</em></p>
  </details>
</td></tr>
<tr><td class="time">3:00 – 3:30</td><td>Coffee break</td></tr>
<tr><td class="time">3:30 – 4:00</td><td>
  <details>
    <summary><strong><a href="https://arxiv.org/abs/2605.20952">Ark: Offchain transaction batching in Bitcoin</a></strong> — Ioannis Alexopoulos (TU Wien)</summary>
    <p><em>Bitcoin is the cryptocurrency with the largest market capitalisation, but its widespread adoption is fundamentally limited by the scalability constraints of its consensus algorithm, which requires every transaction to be confirmed onchain. To address this, several Layer-2 scalability solutions have been proposed to move payments offchain -- most notably, the Lightning Network. However, their deployment remains hindered by cumbersome setup requirements: users must lock funds onchain to participate and engage in complex auxiliary protocols (e.g., for channel rebalancing, top-ups, and routing). Other solutions, like payment pools, sidechains and rollups, cannot be implemented in a non-custodial way on Bitcoin due to its limited scripting capabilities, or require all protocol participants to update the offchain state.</em></p>
    <p><em>In this work, we present Ark, the first Bitcoin-compatible commit-chain. Ark enables offchain transactions of virtual UTXOs (VTXOs), through an untrusted operator who aggregates them into succinct onchain commitments. A distinctive feature of Ark is its ease of deployment: users can receive offchain payments without locking any funds beforehand and Ark state updates can be performed only requiring the users involved in that update.
    We formally define the Ark protocol and prove its security. During this process, we identified two attacks affecting the testnet implementation, which we responsibly disclosed and proposed fixes for, which have been now integrated into the mainnet implementation. Our experimental evaluation demonstrates that Ark can commit onchain to batches of arbitrarily many VTXOs with a constant-sized footprint of approximately 200 vB. Cooperative exits add one output per user, while unilateral exits require O(log n) transactions of roughly 150 vB per VTXO for a batch of n VTXOs.</em></p>
  </details>
</td></tr>
<tr><td class="time">4:00 – 4:30</td><td>
  <details>
    <summary><strong><a href="https://eprint.iacr.org/2025/068">Shielded CSV: Private and efficient client-side validation</a></strong> — Robin Linus (Stanford, ZeroSync)</summary>
    <p><em>Shielded CSV is a client-side validation protocol for private, scalable cryptocurrency payments. It keeps transaction validation off-chain, writes only a 64-byte nullifier to the blockchain per transaction, and uses succinct coin proofs whose size and verification cost do not grow with transaction history. This makes it a promising way to add efficient private payments to Bitcoin and similar systems.</em></p>
  </details>
</td></tr>
</tbody>
</table>
