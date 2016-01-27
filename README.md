# keymaker
Safely execute command line with secret environment variables

## Install

```bash
curl -fLo /usr/local/bin/keymaker https://raw.githubusercontent.com/nsarno/keymaker/master/keymaker && sudo chmod a+x /usr/local/bin/keymaker
```

### Setup

You only need to do this once.

```bash
keymaker --init
```

Enter the AWS credentials when prompted and choose a password.

Keymaker will create an encrypted `.keychain` file in your home directory by default. Optionally, you can change where the encrypted file is stored by setting the `KEYCHAIN` env variable.

### Usage

```bash
keymaker [COMMAND]
```

Optionally you can specify where to read keychain file from by setting the KEYCHAIN env variable.

e.g.

```bash
keymaker make deploy
```

or

```bash
KEYCHAIN=/path/to/keychain keymaker make deploy
```
