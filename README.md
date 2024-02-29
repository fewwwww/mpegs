# mpegs

> For a detailed overview and technical discussion of **mpegs**, please refer to our [speaking session](https://www.youtube.com/watch?v=Cpf1yHwr3wQ).
>

**Crypto Infra for the AI Age**

In an era where AI-generated and deepfake content challenge traditional verification methods, **mpegs** pioneers a crypto-based infrastructure designed to authenticate and trace media data. This project leverages advanced zero-knowledge proofs and blockchain scalability solutions to secure media provenance in a decentralized ecosystem.

## Background

Modern digital ecosystems are confronted with:
- **AI Generated Content:** Fully synthetic content on platforms like Facebook raises questions about the integrity of digital media.
- **Deepfake Content:** Sophisticated synthetic media undermines KYC processes, authentication protocols, and can damage reputations.
- **Lack of Media Provenance:** The inability to verify the authenticity and history of media data complicates trust in digital content.

## Our Experiment

**mpegs** is an experimental research project that builds an MVP capable of making any media data and its associated processing verifiable. The system is architected around three core components:
- **zkVM:** A virtual machine that enables zero-knowledge computations over media processing tasks.
- **Media Processing Algorithm:** A custom algorithm designed to mimic and eventually extend the functionality of FFmpeg, ensuring that every transformation applied to media is cryptographically verifiable.
- **Arbitrum Stylus:** A layer-2 scaling solution providing a WASM-based execution environment where our Groth16 verifier, implemented in Rust, runs efficiently.

## Technical Innovations

### Full Workflow Implementation
- **Image Input/Capturing:** Direct integration with media capture interfaces, ensuring raw media data is securely input into the verification pipeline.
- **Circuit & Prover:** Development of custom ZK circuits that capture the media processing logic. The prover generates succinct proofs that attest to the correctness of media transformations.
- **Verifier:** Implementation of a Groth16 verifier optimized for the Arbitrum Stylus environment, allowing on-chain verification of off-chain computations.

### Media Processing Algorithm in zkVM
- **Extendable Architecture:** The algorithm is modular, designed to be iteratively enhanced to support a full range of FFmpeg-like functionalities.
- **Optimized for Zero-Knowledge Proofs:** Carefully engineered to balance the complexity of media transformations with the computational overhead of generating zero-knowledge proofs.

### Groth16 Verifier on Arbitrum Stylus
- **Rust-based Implementation:** Utilizes Rust for system-level safety and performance.
- **WASM Environment:** Runs within the Arbitrum Stylus WASM execution environment, enabling compatibility with blockchain smart contract ecosystems.
- **Optimized Verification:** Balances verification cost with throughput, making it suitable for scalable decentralized applications.

## Challenges

The development of **mpegs** presented several technical challenges:
- **Complex System Architecture:**
  - Integration across multiple components including a frontend, backend server, prover, verifier, and explorer.
  - Coordinating asynchronous interactions between off-chain computations and on-chain verifications.
- **ZK Stack Decision Making:**
  - Evaluating trade-offs between developing custom circuits, using a pre-built zkVM, or employing a dedicated ZK compiler.
- **Verifier Performance:**
  - Achieving an optimal balance between verification cost (gas efficiency) and throughput, especially within the constraints of a blockchain environment.

## Future Directions

### Full FFmpeg Support
- **Extended Command Set:** Evolve the media processing algorithm to support approximately 3000 options and commands, matching FFmpeg’s capabilities.

### Video as Input
- **Large File Handling:** Enhance the system to process large video files.
- **Continuation Feature:** Develop a continuation mechanism within zkVM to manage stateful processing across large data streams.

### Platforms and Applications
- **Media Rollup Solutions:** Explore the creation of aggregated media proofs that can be used across platforms.
- **Composable NFTs:** Investigate use cases in NFTs, such as generating variations or pop art styles that are verifiably authentic.

## Repo Structure

This repository aggregates sub-repositories developed by different team members, each focusing on a specific component of the **mpegs** project.
