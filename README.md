![](logo.png)

vpw - Use Hashicorp Vault KV store as a password manager.
=======================================

Uses a kv secret path ($VPW_PATH) as a password manager.

NOTE (2024-10-19): This code is over 4 years old and is imported from an old mercurial repo.
	It is not currently used in production(nor do I use it at all at the moment).
	I accept PR's, Issues, etc but I make zero promises.
	It's unknown if it will work with kv2, but it did work in production with kv1.

### List of features

*   Integrates with FZF or other chooser
*   Offloads security to your Vault admins.
*   posix shell!
*   A desktop GUI that works with vpw: https://github.com/adobe/cryptr

### Code Demo

```shell

$ vpw put test username=winner password=winnerpassword
Success! Data written to: secret/pass/zie/test
$ vpw get test
data:
  password: winnerpassword
  username: winner
lease_duration: 2764800
lease_id: ""
renewable: false
request_id: d04192c5-287b-051c-7ec1-68b7999756ee
warnings: null
$ vpw choose
winnerpassword

```

### Download & Installation

```shell
$ curl -o /usr/local/bin/vpw -L -L https://hg.sr.ht/~zie/vpw/raw/default/vpw
```
or git clone and run `make install` to symlink to /usr/local/bin


### Contributing

For sure, make it awesome!

### Authors or Acknowledgments

### License

This project is licensed under the MIT License
