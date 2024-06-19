# 100 - NginX Flake

See examples/nginx/flake.nix

The file is named ```flake.nix```.

## Top-Level Attributes

### Description

Starting the ```flake.nix``` file is a ```description```, that looks like:

```
{
  description = "Some description";
  ... more
}
```

## Inputs

At the same level as the ```description``` is a ```inputs``` attribute, that looks like:

```
{
   ... more
   inputs = {
      ... more
   };
   ... more
}
```

An example of an entry for ```inputs``` is the location (here: url) to the packages for a specific NixOS version (here: 22.11):

```
...
  inputs = {
    nixpkgs.url = github:NixOS/nixpkgs/nixos-22.11;
  };
...
```

## Outputs

At the same level as the ```description``` is an ```outputs``` attribute, that looks like:

```
{
  ... more
  outputs = {
    ... more
  };
  ... more
}
```

An example of an entry for ```outputs``` is ...

MORE
