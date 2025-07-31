# Verify

##### People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'mgoing to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate

## SHA-256
- SHA-256 (Secure Hash Algorithm 256-bit) is a cryptographic hash function from the SHA-2 family, developed by the NSA and published by NIST.
- Websites don’t store your password directly. They store its SHA‑256 hash instead.

## solutions
```
1. ssh -p 64331 ctf-player@rhea.picoctf.net  /  Using the password 6dd28e9b
2. ls
3. cat checksum.txt
```
checksum.txt: 03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8

`4. sha256sum files/* | grep 03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8`

Output: 03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8  files/00011a60

### sha256sum

##### The sha256sum command can be used on a file to get the checksum. To get the checksum of all the files in the directory the sha256sum files/* command could be used. When paired with grep command with the known SHA256 checksum that needs to be found the correct file is displayed.

```
5. ./decrypt.sh files/00011a60
6. cat flag
```
