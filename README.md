# mb_task_assignment

Basically, only docker-compose file that pulls and starts images that together 
make up a task assigment.

There are links to the apps' repositories:
- [the Meter app](https://github.com/RandyRomero/meter)
- [the PV_Simulator app](https://github.com/RandyRomero/pv_simulator)

The first app publishes a message to a broker (rabbitmq), the second one consumes the message,
creates its own value and writes both values and their sum to the disk.

Where you can find the output file?

It's `./pv_simulator/logs/output.log` within a `pv_simulator` container
or, if you want to find it on a host machine (assuming it runs Linux),
you need to execute `docker volume inspect mobility_house_mobility_house` and check
`Mountpoint` key

## Requirements

- docker

- docker-compose

## How to install and run

```
git clone git@github.com:RandyRomero/mb_task_assignment.git

cd mb_task_assigment

docker-compose up
```


