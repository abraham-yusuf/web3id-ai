## A Cross-Chain Verified Agent Economy

### Overview

This section introduces a modular architecture for an autonomous agent economy where
**identity**, **verification**, and **economic execution** are separated but
cryptographically linked.

The stack combines:

- **Universal Profiles (LUKSO)** – programmable agent accounts
- **ERC-8004 Verified Agents (Ethereum)** – trust and capability registry
- **x402** – interaction-level payment negotiation protocol

This enables agents to operate as first-class economic actors without API keys,
custodial wallets, or centralized billing systems.

---

### System Architecture

The system is composed of four orthogonal layers:

1. **Interaction Layer**  
   Agent-to-agent communication via HTTP / RPC using x402 (HTTP 402 – Payment Required).

2. **Economic Protocol Layer**  
   Defines micropayments, pay-per-call, and subscription logic, verified via on-chain
   settlement.

3. **Account & Execution Layer (LUKSO)**  
   Universal Profiles provide:
   - Smart contract-based agent accounts
   - Native asset custody
   - Fine-grained permissions (LSP6)
   - Autonomous execution

4. **Verification & Trust Layer (Ethereum)**  
   ERC-8004 contracts provide verifiable claims about agent identity, capabilities,
   and reputation.

---

### Design Principle

> **Verification does not execute.  
> Execution does not verify.**

Trust systems determine *whether an agent should be trusted*, while Universal Profiles
determine *whether an agent can act*.

---

### Trust & Payment Flow

1. Agent submits a request  
2. Service responds with an x402 payment challenge  
3. Agent verifies ERC-8004 trust requirements  
4. Payment executed via Universal Profile  
5. On-chain receipt emitted and verified  
6. Service response delivered  

---

### Positioning vs World ID / DID / VC

World ID, DID, and Verifiable Credentials treat identity as **proof** (human-centric,
access control, governance).

This architecture treats identity as an **actor** (agent-centric, economic execution).

- World ID answers: **“Who are you?”**
- This stack answers: **“What can you do, and can you pay?”**

---

### Implications

By combining programmable accounts, verifiable trust, and protocol-level payment
negotiation, this architecture enables a scalable, decentralized agent economy
designed for machine-to-machine interaction.
