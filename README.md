# Learning Splunk with Docker

Learn the basic of Splunk administration with docker (search head clustering, index clustering, deployment server, license server)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine. 
### Prerequisites

This repo has been tested with the packages versions and OS version:

```
docker-compose version 1.27.4, build 40524192
Docker version 19.03.13, build 4484c46d9d
CentOS Linux release 8.2.2004 (Core)
```

### Installing

A step by step series of examples that tell you how to get a development env running

Install docker and docker-compose by following the official docs https://docs.docker.com/engine/install/centos/ and https://docs.docker.com/compose/install/

Then clone the repo:

```
git clone https://github.com/GitarPlayer/learning_splunk.git
```

Change into the repository and start the containers (-d starts the containers in the background):

```
cd learning_splunk && docker-compose up -d 
```
The familiar Splunk login page should greet you at localhost:8000 to localhost:8006. You can log in with the default admin user and the password is password. 
**If you are running this inside of a VM you need to configure port forwarding!**

## Running the tests

Running docker ps should show you six splunk container running. You could write a simple bash script that curls localhost:8000-80006 -L (follow redirects) for example.

### Useful commands

This will show each container name and its associated ports. We use Go Templates when we specify --format (Docker was written in Go). For more information please visit the Docker doc https://docs.docker.com/config/formatting/
```  
docker ps --format "table {{.Names}}\t{{.Ports}}"
```

## Contributing

Pull requests are always welcome.

## Authors

* **Christian Moore-Bucheli** 

See also the list of [contributors](https://github.com/GitarPlayer/learning_splunk/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
