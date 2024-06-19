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

Strictly speaking, the ```description``` attribute is not needed or required.

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

Strictly speaking, the ```inputs``` attribute is not needed or required.

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

An example of an entry for ```outputs``` is a packages (here: x86_64-linux) entry. Optionally, ```outputs``` can have arguments (here: self, nixpkgs):

```
...
{
  ... more
  outputs = { self, nixpkgs }: {
    packages."x86_64-linux" = 
      ... more
  }
}
...
```

**NOTE**: ```self``` is a reference to the flake itself. This is how the flake components (usually outputs) can reference other flake components.

Strictly speaking, the ```outputs``` attribute is needed and required.

### x86_64-linux

The following attributes are valid for the ```x86_64-linux``` package, when installing nginx:

```
{
  ... more
  packages."x86_64-linux" =
    let
       pkgs = import nixpkgs { system = "x86_64-linux"; };
    in
    ... more
  ... more
}
```

In above example, we define a variable ```pkgs``` that imports nix packages (here: system for x86_64-linux).
