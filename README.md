# kixer

Generate exhaustive password/character wordlists of a fixed length for security research, CTF challenges, and password-strength demonstrations.

`kixer` enumerates every combination of a 53-character set — lowercase letters, digits, and common symbols (`a–z 0–9 !@#$%^,:;?/_-(){}%`) — and writes them to a file. A length of `n` produces **53ⁿ** lines.

## What it does

- Prompts for an output filename and a character length
- Writes every possible combination of that length to the file
- No dependencies beyond the Python standard library

## Install

```bash
git clone https://github.com/nub-coders/kixer
cd kixer
```

**Termux:**

```bash
pkg update && pkg install git python
git clone https://github.com/nub-coders/kixer
cd kixer
```

## Usage

```bash
python3 kixer.py
```

```
your file name: wordlist.txt
your character size: 3
```

This writes all `53³ = 148,877` three-character combinations to `wordlist.txt`.

> ⚠️ **Size grows fast.** Each extra character multiplies the output by 53:
>
> | Length | Combinations | Approx. file size |
> |---|---|---|
> | 2 | 2,809 | ~8 KB |
> | 3 | 148,877 | ~580 KB |
> | 4 | ~7.9 million | ~39 MB |
> | 5 | ~418 million | ~2.4 GB |
>
> Lengths above 5 are impractical on most machines.

## Use cases

- Generating candidate wordlists for **CTF** challenges
- Penetration testing on **systems you are authorized to test**
- Demonstrating why short passwords are weak

## Warning

For **educational and authorized use only**. Using generated wordlists to attack systems without explicit permission is illegal. You are responsible for how you use this tool.
