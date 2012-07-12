s8fleet-deploy(1) -- Push code to drones.
=======================================

## SYNOPSIS

    s8fleet deploy [<options>]

## DESCRIPTION

Push code to all the drones. The drones will check out the code into a new
directory.

## OPTIONS

* commit - Push a particular commit by hash. Defaults to the latest commit.
* repo - Push code into this repo name. Defaults to the closest directory name
  with a `.git/` in it.
* branch - Select the branch to push. Defaults to the current branch.
* force - Whether to perform a force update. Defaults to false.

If you haven't set a remote with `s8fleet remote`, you'll need to specify these
options:

* hub - location of the hub as a "host:port" string
* secret - optional passphrase to connect to the hub

## EXAMPLE

Usually you'll just want to:

    s8fleet deploy

but sometimes you'll want to deploy a specific commit:

    s8fleet deploy --commit=8431261ee2149e6d39863a6f3d70fe88375c6210
