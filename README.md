# iac-env
Infrastructure as code on AWS. Cloudformation stack management using [Sceptre](https://github.com/Sceptre/sceptre).

Managing Cloudformation (CF) stacks involves a learning curve. That is: Standing up and updating simple systems using CF 
is an involved process. Often there are multiple ways to solve the problem, unexpected gaps between integrating 
services, and key sequences to follow in order to successfully integrate services. This complexity increases when AWS 
releases new services and the design of your system's architecture evolves. The convenience of infrastructure-as-code is 
improved when the constituent parts of the system are well organized and easily stood up/torn down. 

My objective in this project is to build out an environment from scratch - to have a general set of templates that can
be used to stamp out the environments typically connected in by a delivery pipeline.


## Setup
### Setup a [venv](https://docs.python.org/3/library/venv.html) for python dependencies
python3 -m venv venv
. venv/bin/activate
pip3 install -r requirements.txt

### Stand up an environment by stack group:

    yes | sceptre create preprod

### List resources

    sceptre list resources preprod
    
TODO:

* Account creation accepts a list
* Create an environment account (federated users within?)
* To presentation: Stack Groups, resolvers