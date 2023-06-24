# Lemmy on K8S

This repo serves as a base for a quick setup on a kubernetes cluster. Please note that this is not a clone and run type of repo, you will need to customize it to your needs to some extent. 

### Things this repo assumes about your environment:
- You have a traefik setup for reverse-proxy, and it picks up ingresses with `traefik-external` class
- You have a working PostgreSQL DB with a lemmy user and database running
- You have a PVC provisioner setup. In my cluster I'm running Longhorn. If you are not, change the storageClassName in the `pict-rs.yaml` file
- You have a Minio running for Pict-RS (optional, change the pict-rs config if you dont need it)




### Minimum to get it running
- Have the stuff above
- Add your hostname to `lemmy-ingresses.yaml` and `lemmy-ui.yaml`  
- Edit the config in the following files:
    - `lemmy-config.secret.yaml`
    - `pict-rs-config.yaml`
    - `pict-rs.secret.yaml`



## Resources:

https://join-lemmy.org/docs/en/administration/administration.html

https://raw.githubusercontent.com/LemmyNet/lemmy/release/v0.17/docker/prod/docker-compose.yml

https://raw.githubusercontent.com/LemmyNet/lemmy/release/v0.17/docker/prod/lemmy.hjson

https://git.asonix.dog/asonix/pict-rs/

https://git.asonix.dog/asonix/pict-rs/src/branch/main/pict-rs.toml