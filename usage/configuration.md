# Configuration

`@solana-suite/config`

A tool to modify the config of Solana Suite. It is usually installed as
Dependency.

{% hint style="info" %} Good to know:

Configuration values are described in the JSON file
`node_modules/@solana-suite/config/solana-suite.json` {% endhint %}

{% tabs %}

{% tab title="npm" %}

```shell
npx solana-suite-config --help
```

{% endtab %}

{% tab title="yarn" %}

```shell
yarn solana-suite-config --help
```

{% endtab %}

{% tab title="pnpm" %}

```shell
pnpm solana-suite-config --help
```

{% endtab %}

{% endtabs %}

### example

```shell
Usage: solana-suite-config [options]

Setup solana-suite.json

Options:
  -V, --version                                  output the version number
  -c --cluster <cluster type>                    connect to cluster type. "prd", "dev", "test", "localhost"
  -cc --custom-cluster <cluster url...>          connect to cluster url. "https://...", if you set more than one url, please separate them with
                                                 a space
  -d --debug <true or false>                     display debug log on terminal. defalut "false"
  -n --nftstorage <apikey>                       Set apikey of nft.storage. "eyJhbGciO..."
  -das --das-api-url <digital asset api url...>  connect to digital asset api url. "https://...", if you set more than one url, please separate
                                                 them with a space
  -s --show                                      Show value current solana-suite.json
  -h, --help                                     display help for command
```
