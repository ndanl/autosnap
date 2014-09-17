#AWS snapshot tool

A simple command line tool to for managing AWS volumes and
snapshots.

###Installation

The easiest way to get up and running is to run 

    pip install -U autosnap

Alternatively, you can fork/clone this project from github.  After it has been
cloned, run

    python setup.py develop

from the autosnap root directory and you
should be good to go.

###Configuration

You will need to create a default config in the root of this directory called
`.config` that contains the following AWS account info.

```
region = us-west-1
aws_access_key_id = xxx
aws_secret_access_key = xxx
owner_id = xxx 
```

Where `region` is the default region to use for this tool, `aws_access_key_id`
is the ID for the specific user that will interface with AWS,
`aws_secret_access_key` is the associated key for the ID and `owner_id` is the associated
AWS account that contains the snapshots and volumes to work with.

This config can be overriden on the command line by passing the `-c` or
`--config` flags to the tool (not implemented yet!  I will update when it is
completed).  By default the config is expected to be placed in the root of this
project in a file called `.config`.

**Note** You can obtain your AWS owner_id by navigating to the AWS management console,
selecting your user account then `My Account`.  Under account settings there
should be an `Account ID` which corresponds to the owner ID.

###Usage

The easiest way to get started using this tool after it has been installed and
the config file has been created is to run `autosnap --help` to get a listing
of all the commands and various options.

###Contributing

Anybody is welcome to contribute to this project.  Inquiries can be directed to
me via github issues or you are more than welcome to email me directly at
`josh.reichardt@gmail.com`.

###TODO

* Error checking
* Logging
* Ability to automatically generate config
* Ability to create AMI from snapshot
* Extend command line capabilities

###License

This project is licensed under the MIT licencse.  See LICENSE for full details.

