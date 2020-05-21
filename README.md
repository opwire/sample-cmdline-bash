# opwire-agent: sample command line in Bash

## Install

### Checkout source code

Clone example source code from github repository:

```shell
git clone https://github.com/opwire/sample-cmdline-bash.git
```

Change the current working directory to the project folder:

```shell
cd sample-cmdline-bash
```

### Download `opwire-agent`

To download the latest `opwire-agent` on Linux/macOS/BSD systems, run:

```shell
curl https://opwire.org/opwire-agent/install.sh | bash
```

For other systems, manually download and extract the latest [`opwire-agent`](https://github.com/opwire/opwire-agent/releases/latest) program into this directory.

## Test the service using `curl`

Execute the following command:

```shell
./opwire-agent serve -p=8888
```

Run the default command:

```curl
curl --request GET \
  --url http://localhost:8888/run
```

Execute any bash command from request body (This is a dangerous command in production environment. Please consider before use in production servers):

```curl
curl --request POST \
  --url http://localhost:8888/run/spawn \
  --data 'ps -All'
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b your-new-feature`)
3. Commit your changes (`git commit -am "Add some feature"`)
4. Push to the branch (`git push origin your-new-feature`)
5. Create new Pull Request

## License

MIT

See [LICENSE](LICENSE) to see the full text.
