# Portcullis pitch: speaker notes

## 1. Portcullis
Portcullis is a security and compliance firewall for inbound institutional cross-chain settlement. The single premise is simple: prove the message before it moves value.

## 2. The receiver
The critical failure point is the receiver. Ronin, Wormhole, and Nomad differ in incident details, but a bad cross-chain message reached a contract that could execute it.

## 3. Controlled path
The adapter calls the guard before transfer. The guard evaluates binding, bounds, replay, nonce, rate, and volume or policy. A plain invalid message does not take down the lane.

## 4. Architecture
Arc is the settlement origination layer. ENS resolves the authority. CRE supplies private policy evidence. The guard enforces the decision. The Graph makes every attempt observable.

## 5. Authentication
The hardened binding check recovers the signer from a digest bound to the chain, this guard instance, and the settlement. This replaced a self-consistency check that could be forged.

## 6. Self-audit
This is the strongest project story. Eight agents reviewed the first version while 105 tests were green and found a drain path. The report was kept in the repository.

## 7. Remediation
All six confirmed findings were closed that day. The key operational change is that only a genuine, authenticated anomaly can latch the breaker.

## 8. Sepolia proof
This is a live capture of the Sepolia guard. It shows the actual contract and configuration transactions, including policy, adapter, rate, and bounds changes.

## 9. Dashboard
This is a real capture of the public dashboard. It currently shows the breaker up and no indexed settlement history. Present it as deployed UI proof, not as a populated activity feed.

## 10. Sponsor stack
Each integration has a job: Arc originates settlement, ENS supplies the authority, CRE keeps policy private, and The Graph supplies the audit trail.

## 11. Demo
The demo walks one genuine settlement, a forged message rejected before receiver state changes, a signed anomaly that latches the breaker, and guardian recovery.

## 12. Limitations
This is testnet work, the guardian is a single EOA, the transport is mocked, and a fresh source has a warmup behavior. These are visible by design.

## 13. Close
The project is easy to inspect: dashboard, docs, source code, subgraph, and the complete self-audit are public.
