# Fly Factorio Server

This is a Factorio server in fly.io using GitHub Actions and without needing to use Terraform and have to manage state.

Unfortunately this cannot scale to zero since Factorio uses UDP, and fly.io does not start the machine on UDP traffic. Therefore this server has to run all the time.

## Setup

You will need a fly.io account, then install and setup the [fly.io CLI](https://fly.io/docs/flyctl/install/) then run:

```bash
fly launch --remote-only --copy-config --name <factorio server>
```

Where `<factorio server>` is the globally unique name of your minecraft server in Fly.io

## Licence

MIT
