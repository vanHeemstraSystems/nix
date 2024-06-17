# 300 - Building Our Application

## 100 - Building a Hello World container with Nix and Docker

Run the following command, after having installed nix and docker.

```
$ nix build .#my-container-image
$ ls -lah result
docker load < result
docker run my-container-image
```

It makes use of the file ```flake.nix```. 
