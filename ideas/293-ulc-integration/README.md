---
id: 293-ulc-integration
title: ULC integration
status: In Progress
created: 2018-08-06
category: core
lead-contributor: mandrigin
contributors:
    - mandrigin Clojure dev
    - b00ris Go dev
    - jeka Go dev
exit-criteria: yes
success-metrics: yes
clear-roles: yes
future-iteration: yes
okrs:
    - Core. [P0] LES and/or ULC are operational and used by at least 10% of all users.
---

## Preamble

    Idea: 293-ulc-integration
    Title: ULC integration
    Status: In Progress
    Created: 2018-08-06
    Requires (*optional): #254

## Summary
Status app can use LES and ULC as Ethereum providers instead of Infura.

## Swarm Participants
- Lead Contributor: @mandrigin
- Contributor: @jeka
- Contributor: @b00ris
- Contributor: TBD
- QA: TBD

## Product Overview
We need LES client enabled on mobile device to be really decentralized and to enable all web3 features for dApps.

### Requirements & Dependencies
ULC integration depends on research swarm #254

### Security and Privacy Implications
* Free slots for LES servers(can be resolved by les service model, onlyannounce servers, vipnode)
* Trusted nodes selection(trusted nodes list can be automatically expanded or changed)

### Minimum Viable Product
* LES can work as the second Ethereum provider in status app.
* ULC can work as the third Ethereum provider in status app with static trusted nodes.

### Iteration 0

Goal Date: 2018-09-10

Description:
* Add LES as an option for test networks
* ULC in go-ethereum master(#254)
* Add LES servers to our staging fleet

### Iteration 1

Goal Date: 2018-09-14

Description:
* investigate les integration problems and add it to backlog

### Iteration 2

Goal Date: 2018-09-25

Description:
* run in our cluster onlyAnnounce LES servers 
* update go-ethereum with ULC in status-go 
* graceful downgrade(use infura by default and if it fails, start ULC node)

### Iteration 3—...

Goal Date: 2018-09-25
 * TBD

## Success Metrics
* Status app can use LES and ULC provider instead of Infura (10% of users are using it).

## Exit criteria
* Running on Mainnet

## Copyright

Copyright and related rights waived
via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
