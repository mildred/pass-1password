# pass-1password

A [pass](https://www.passwordstore.org/) extension for using 1password accounts
(using the `op` command-line).

**Warning:** To get started, this is a fork of pass-otp and the plugis is not
yet implemented.

## Usage

```
Usage:

    pass otp [code] [--clip,-c] pass-name
        Generate an OTP code and optionally put it on the clipboard.
        If put on the clipboard, it will be cleared in 45 seconds.

    pass otp insert [--force,-f] [--echo,-e] [pass-name]
        Prompt for and insert a new OTP key URI. If pass-name is not supplied,
        use the URI label. Optionally, echo the input. Prompt before overwriting
        existing password unless forced. This command accepts input from stdin.

    pass otp append [--force,-f] [--echo,-e] pass-name
        Appends an OTP key URI to an existing password file. Optionally, echo
        the input. Prompt before overwriting an existing URI unless forced. This
        command accepts input from stdin.

    pass otp uri [--clip,-c] [--qrcode,-q] pass-name
        Display the key URI stored in pass-name. Optionally, put it on the
        clipboard, or display a QR code.

    pass otp validate uri
        Test if the given URI is a valid OTP key URI.

More information may be found in the pass-otp(1) man page.
```

## Examples

TBD

## Installation

### From git

```
git clone https://github.com/tadfisher/pass-otp
cd pass-otp
sudo make install
```

### Others

Please contribute

## Requirements

- `pass` 1.7.0 or later for extension support
- `op` for 1password

### Build requirements

- `make test`
  - `pass` >= 1.7.0
  - `git`
  - `op`
  - `expect`
- `make lint`
  - `shellcheck`

