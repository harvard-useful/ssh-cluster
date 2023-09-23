# ssh-cluster

ssh into the [fas cluster](https://www.rc.fas.harvard.edu/) without having to enter your password or 2fa code for Linux or Mac.

The way this program works is by using a tool called [expect](https://linux.die.net/man/1/expect) and [oathtool](https://www.cyberciti.biz/faq/use-oathtool-linux-command-line-for-2-step-verification-2fa/). `expect` allows you to put your password and 2FA code into this script once so you don't have enter them each time. The 2FA code is generated by `oathtool` and a 2FA seed. You can find your harvard 2FA seed [here](https://two-factor.rc.fas.harvard.edu/) at the section "ADDITIONAL INFORMATION AND HINTS".

## Installation

0. Install oathtool. Mac oathtool can be installed from [here](https://formulae.brew.sh/formula/oath-toolkit) and linux from [here](https://www.cyberciti.biz/faq/use-oathtool-linux-command-line-for-2-step-verification-2fa/). `expect` should already be installed by default.

1. In the `cluster` script, replace `<PASSWORD> `with your actual password and `<2FA>` with the code from [here](https://two-factor.rc.fas.harvard.edu/)

2. Move this script to somewhere in your PATH.

3. Profit! You can now ssh into the cluster easily with the command `cluster`.
