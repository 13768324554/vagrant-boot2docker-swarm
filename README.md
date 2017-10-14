# Multi-Machine Docker Swarm Vagrant Environment

This repository contains a `Vagrantfile` and scripts that allow to start a multi-machine Docker swarm Vagrant environment. It is based on the [31z4/boot2docker](https://app.vagrantup.com/31z4/boxes/boot2docker) Vagrant box.

## Usage

To start the environment, first install the following prerequisites:

* [VirtualBox](http://www.virtualbox.org)
* [Vagrant](http://www.vagrantup.com)

Then just run the following command and wait a couple of minutes:

    $ vagrant up

The swarm has a single manager and two worker nodes:

```console
$ vagrant status
Current machine states:

manager1                  running (virtualbox)
worker1                   running (virtualbox)
worker2                   running (virtualbox)

This environment represents multiple VMs. The VMs are all listed
above with their current state. For more information about a specific
VM, run `vagrant status NAME`.
```

## Contributing

Contributions are greatly appreciated. The project follows the typical GitHub pull request model. Before starting any work, please either comment on an existing issue, or file a new one.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
