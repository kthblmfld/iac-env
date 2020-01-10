# iac-env
Infrastructure as code on AWS. Cloudformation stacs management using [Sceptre](https://github.com/Sceptre/sceptre).


This is a python project that uses [Sceptre](https://github.com/Sceptre/sceptre) to build out an environment on AWS 

## Setup
### Setup a [venv](https://docs.python.org/3/library/venv.html) for python dependencies
python3 -m venv venv
. venv/bin/activate
pip3 install -r requirements.txt

### Stand up an environment by stack group:

    yes | sceptre create preprod

### List resources

    sceptre list resources preprod