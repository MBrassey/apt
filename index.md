# MBrassey apt repository

apt-installable packages for [agtop](https://github.com/MBrassey/agtop).

## Install

```sh
curl -fsSL https://mbrassey.github.io/apt/pubkey.asc \
  | sudo gpg --dearmor -o /etc/apt/keyrings/agtop.gpg
echo "deb [signed-by=/etc/apt/keyrings/agtop.gpg] https://mbrassey.github.io/apt ./" \
  | sudo tee /etc/apt/sources.list.d/agtop.list
sudo apt update && sudo apt install agtop
```

After that, `sudo apt update && sudo apt upgrade` picks up new releases like
any other apt source.

## What's hosted

Updated automatically by the [agtop release pipeline](https://github.com/MBrassey/agtop/blob/main/.github/workflows/release.yml).
The repo's `Release` file is signed with the key whose public half is in
[pubkey.asc](pubkey.asc); fingerprint:

```
FC8BF673587134A114B205A0632F0658B478942A
```
