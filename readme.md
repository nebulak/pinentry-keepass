# pinentry-keepass

A gnupg pinentry program, which automatically retrieves the key from KeePass/KeePassX/KeePassXC using the KeePassHTTP-Protocol.

## Requirements
  * KeePass/KeePassX/KeePassXC
  * KeePassHTTP

## Setup
  * Add the following URL to your Gnupg-password in keepass:

        https://gnupg.org

  * Add pinentry-kphttp to bin

		chmod +x ./pinentry-keepass
		sudo cp ./pinentry-keepass /usr/local/bin/pinentry-keepass
  * edit ~/.gnupg/gpg-agent.conf and add your path:

        pinentry-program /usr/local/bin/pinentry-keepass

On first use KeePass will ask you to allow the application to access your passwords.
