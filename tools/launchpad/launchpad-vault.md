---
description: Vault and Allocation Mechanics
---

# Launchpad Vault

Launchpad Vault is the staking ground for SPIN holders to earn IGO allocations. By staking to the contract, our users will benefit from both auto-compounding interests from single-staking SPIN pool rewards and IGO allocations from the corresponding project.

Spintop's Launchpad system consists of a singular Vault which hosts individual IGO events as modular staking contracts. This way users can enjoy earning IGO allocation rights without taking any action.

#### Allocation Mechanics

Inspired by Synthetix staking contracts. Allocations for the users are calculated by the set of formulas below:

_r(u, a, b) = reward for user u for a<=t<=b_

_R= rewards minted per second_

_L(t) = total staked token at time t_

_l(u, t) = token staked by user u at time t_

_When L(t) > 0_

$$
r(u,a,b) =  \sum^b_{t=a}R\frac{l(u,t)}{L(t)}
$$

_When l(u, t) = k for a <= t <= b_

$$
=Rk\bigg( \sum_{t=0}^{b}R\frac{1}{L(t)}+\sum_{t=0}^{a-1}R\frac{1}{L(t)}\bigg)
$$
