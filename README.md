## Discomy

Distributed Compiling Manager for RockY Linux !

Under the hood tools

`icecream`
`distcc`

### How it works ?

Follow steps on https://gitlab.com/SkipGrube/RockyLinux/-/blob/master/Build_Steps.md

* Design interactions with Koji and Mock

* Prepare job queues

* Connect to agents

* Check agents availability

* Signal agents for green light

* Check the jobs queue for priority

* Start jobs distribution

* Monitor jobs execution

* Check job finishing

* Update queue

* Notify CI/CD server of the conclusion


--------------------

Possible batch execution

Users apply for a subscription to include their computing capacity, filling a form with the info necessary to provisioning. After, can download provisioning playbooks and manifests, or just configure by hand and insert the info of compiling grid.

Calculate the theoretical peak to finish the compiling step, and give an estimate of how much computing and storage is necessary for all

Run sync with repos and mirror after finishing, checking integrity of past jobs
