# NixOS Workshop material

## Introduction
  - structure of day
  - definition
  - components overview:
    - nixlang
    - nixpkgs
    - Package manager tools (node2nix, bundix)
    - (NixOS)
    - (NixOps)
    - (Vulnix)
  - model: proper dependency graph
    - content presentation FOSDEM

## Nix language
  - Semantics
    - build datastructure
    - pure lazy program --> 1 side effect: generate derivations
  - Types (shown in shell)
    - primitive types (numbers, strings, paths, uri's etc)
    - lists
    - attr sets
  - Output of Nix program (explain derivation)
  - Language constructs
    - let ... in E
    - with E1; E2;
    - functions
      - 1 arg lambda
      - attrset argument
    - import
    - nixpkgs library functions
    - play with tour of nix / nix-instantiate --eval --strict

## Packaging
  - Show how a package is packged in nixpkgs.
    - top-level.nix, callPackage
    - stdenv.mkDerivation
    - specialized build functions
  - Package example applictions:
    - C / C++
    - Ruby (with bundix)
    - Javascript (with node2nix)
    - Rust
    - Python (pypy2nix)
    - Go (go2nix)

## NixOS
  - Concepts
    - module system
    - generations
    - configuration.nix
    - updating your OS
    - rolling back to a previous version
      - note that your configuration.nix is not versioned! Just the resulting DRV files.
  - Using modules
    - Setup HTTP server
    - Setup samba
  - Creating modules --> run custom app

## NixOps
  - Concepts
    - two evaluations: network vs "nixos"
  - VirtualBox guestbook + redis HA

## Show off
At end of day allow people to share what they have done.
