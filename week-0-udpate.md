# **EPF Cohort 7 — Week 0 Update**

## **Intro**

Hello everyone, my name is Aarish Naiyer. I am a third-year undergrad Computing Science student at the University of Alberta. I'll be exploring EPF Cohort 7 permissionlessly. I'm fairly new to distributed systems and core protocol development, so I want to use this cohort and the help I can get from the mentors to build real foundational knowledge while contributing to something meaningful.

## Project: Decentralized CL Checkpoint Sync (Nimbus)

I'll be exploring the Decentralized CL Checkpoint Sync project under Nimbus, mentored by Etan Kissling.

### Why this project

Ethereum positions itself as decentralized, but the very first step of running a node today involves downloading a checkpoint state from a trusted server — meaning a new node has to simply trust that the server gave it correct data, with no cryptographic verification. That's a real gap between Ethereum's stated values and its practical bootstrapping process, and I find that an interesting and meaningful problem to work on.

This project also stood out to me because:

- It was directly recommended to me, and the mentorship from Etan, who is actively shaping the spec, so the contributions will definitely impact the protocol design, not be for the sake of contribution alone.
- This will help understand the basic consensus layer concepts, such as Merkle proofs, SSZ, libp2p, light client implementation, etc., which will apply to virtually any CL work.
- Given where I'm starting from, this project lets me build up conceptual understanding first, rather than requiring deep client internals knowledge from day one.

### What I understand the project to be

The current checkpoint sync flow has new nodes download a recent finalized state snapshot from a trusted server to bootstrap quickly, rather than syncing from genesis. This project replaces that trust assumption with a peer-to-peer approach, extending the existing Altair light client sync protocol — which already lets nodes trustlessly track the latest beacon block header — to also serve historical finalized state. The result is that new nodes can bootstrap entirely from peers, verifying what they receive via Merkle proofs instead of trusting a single server.

### What I've been doing this week

This week, I have spent some time reading the light client sync protocol specification and the checkpoint sync notes. I also attended the EPF Office Hours AMA with Shane Moore (Lighthouse core dev, cohort 6 ePBS fellow), which was useful for hearing about navigating the fellowship and the path from fellow to core dev.

### What I'm learning

I'm coming from a primarily Python background, so I'm picking up Rust through The Rust Book, and beginning to study Nim via the official Nim tutorial, given that Nimbus is written in it.

### Next steps

- I'll be reaching out to Etan to identify a concrete starting point and get oriented in the project's current status
- Get into the Nimbus codebase and start exploring its structure
- Set up a local dev environment for Nimbus
- Continue building foundational knowledge of consensus layer internals (SSZ, Merkle proofs, light client design)
