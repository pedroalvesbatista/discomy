## Discomy

Distributed Compiling Manager for RockY Linux !

What about doing some High Performance Computing (HPC) all along the process of building from zero Rocky Enterprise Linux ?

A lot of people and organizations has offered computing resources to help Rocky Linux be lifted off asap ! So, why not combine all that in one shot, helping development, testing, integration, packages compatibility checks as well other fundamental tasks and get Rocky ready for action any time soon ?

Under the hood tools

`icecream`
`distcc`

### How it works ?

Follow steps on https://gitlab.com/SkipGrube/RockyLinux/-/blob/master/Build_Steps.md

Those are some desirable features to be reached :

[] Design interactions with Koji and Mock

[] Prepare job queues

[] Connect to agents

[] Check agents availability

[] Signal agents for green light

[] Check the jobs queue for priority

[] Start jobs distribution

[] Monitor jobs execution

[] Check job finishing

[] Update queue

[] Notify CI/CD server of the conclusion

To acomplish all that, the following packages will be the core of `discomy` :

`job_listener`

Through web hooks, catch all work done in remote code repo's, read the pipeline specifications, and start to distribute the incoming jobs to the queue.

`job_queue`

`host_scheduler`

`host_agregator`

`host_executor`

`queue_executor`

`final_agregator`



For dealing with config files, and interfacing with API's, two more packages are in place :

`config_manager`

`api`

--------------------

Other non-functional requirements in turn to make possible :

* Possible batch execution - ex. package sanitization functions, compatibility checking

* Users apply for a subscription to include their computing capacity, filling a form with the info necessary to provisioning ("disco playlists"). After then, can download provisioning playbooks and manifests, or just configure by hand and insert the info of compiling grid.

* Calculate the theoretical peak to finish the compiling step, and give an estimate of how much computing and storage is necessary for all - based on the number of available hosts, CPU I/O, storage, network paths.

* Run sync with repos and mirror after finishing, checking integrity of past jobs


### Testing sandbox

To test the basics, and check each step of desired features, virtual envs as well network of hosts is created, jobs assigned to it and the `discomy` monitoring tool (`moniscomy` or monitoring for discomy).

For the initial steps, Vermin[https://github.com/mhewedy/vermin] can be used to spawn some virtual machines, inject discomy through an installation and configuration script (install.sh and configure.sh), test the outputs and get the final results.

A RPM package creation will be placed, and the steps for building versions of the same package (maybe following `git-flow`) to get a "stable" branch of the package.

In more fine grained way, package checks can be done too, to test tool capability, limitations and bottlenecks.

## Contributing

To make some contribution, just fork the repo, do your stuff, and make a PR so we can align our work
