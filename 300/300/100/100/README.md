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

MORE
