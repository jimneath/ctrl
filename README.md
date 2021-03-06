# Ctrl

This is a simple gem to ease listing and sshing to instances in an AWS VPC.

## Installation

    $ gem install infra-ctrl

Add environment variables for AWS (direnv.net FTW):

* AWS_DEFAULT_REGION
* AWS_SECRET_ACCESS_KEY
* AWS_ACCESS_KEY_ID

As well as a couple for specifying the users to log in as when sshing to the nat and internal instances:

* CTRL_SSH_USER
* CTRL_SSH_NAT_USER

## Notes

Assumptions about your infrastructure:

1. Instances with public ips are connected to directly using the CTRL_SSH_USER
2. Each instance has a tag:Environment
3. VPC private instances use the same user to log in
4. You have the necessary keys locally, and are fine forwarding your agent

## Usage

    $ ctrl ls <env> <instance name>
    $ ctrl ssh <env> <instance name>

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/MattHall/ctrl
