

---
title: Consensus Rule Changes
linktitle: Consensus Rule Changes
description: How the consensus rules are changed by the network - Understanding forks
date: 2018-05-25
layout: single
keywords: ["GDPR", "Privacy", "Data Protection"]
menu:
  docs:
    parent: "about"
    weight: 15
weight: 15
sections_weight: 15
draft: false
aliases: [/privacy/,/gdpr/]
toc: true
---
To maintain consensus, all full nodes validate blocks using the same consensus rules. However, sometimes the consensus rules are changed to introduce new features or prevent network abuse. When the new rules are implemented, there will likely be a period of time when non-upgraded nodes follow the old rules and upgraded nodes follow the new rules, creating two possible ways consensus can break:

A block following the new consensus rules is accepted by upgraded nodes but rejected by non-upgraded nodes. For example, a new transaction feature is used within a block: upgraded nodes understand the feature and accept it, but non-upgraded nodes reject it because it violates the old rules.

A block violating the new consensus rules is rejected by upgraded nodes but accepted by non-upgraded nodes. For example, an abusive transaction feature is used within a block: upgraded nodes reject it because it violates the new rules, but non-upgraded nodes accept it because it follows the old rules.

In the first case, rejection by non-upgraded nodes, mining software which gets block chain data from those non-upgraded nodes refuses to build on the same chain as mining software getting data from upgraded nodes. This creates permanently divergent chains—one for non-upgraded nodes and one for upgraded nodes—called a hard fork.

## Hard Fork

In the second case, rejection by upgraded nodes, it’s possible to keep the block chain from permanently diverging if upgraded nodes control a majority of the hash rate. That’s because, in this case, non-upgraded nodes will accept as valid all the same blocks as upgraded nodes, so the upgraded nodes can build a stronger chain that the non-upgraded nodes will accept as the best valid block chain. This is called a soft fork.

## Soft Fork

Although a fork is an actual divergence in block chains, changes to the consensus rules are often described by their potential to create either a hard or soft fork. For example, “increasing the block size requires a hard fork.” In this example, an actual block chain fork is not required—but it is a possible outcome.

Consensus rule changes may be activated in various ways. Originally soft forks where performed by just releasing the backwards-compatible change in a client that began immediately enforcing the new rule. Multiple soft forks such since then have been activated via a flag day where the new rule began to be enforced at a preset time or block height. Such forks activated via a flag day are known as User Activated Soft Forks (UASF) as they are dependent on having sufficient users (nodes) to enforce the new rules after the flag day.

Now soft forks wait for a majority of hash rate (typically 75%) to signal their readiness for enforcing the new consensus rules by staking blocks with the new version. Once the signalling threshold has been passed, all nodes will begin enforcing the new rules. Such forks are known as Node Activated Soft Forks (NASF) as they are dependent on stakers for activation.
