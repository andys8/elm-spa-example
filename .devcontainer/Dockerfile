FROM nixos/nix

RUN nix-channel --add https://nixos.org/channels/nixpkgs-unstable nixpkgs
RUN nix-channel --update
RUN nix-env -iA nixpkgs.elmPackages.elm nixpkgs.elmPackages.elm-test nixpkgs.elmPackages.elm-format nixpkgs.git
