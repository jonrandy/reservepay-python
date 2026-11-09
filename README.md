# reservepay-python

Typed Python clients (both sync and async) to allow usage of the Reservepay APIs - [Merchant](https://developer.reservepay.com/api/merchants), [SDK](https://developer.reservepay.com/api/sdk)
, and [Terminal](https://developer.reservepay.com/api/terminals).

The clients (found in `src/reservepay/`) were generated using the [WebFunction CLI tool](https://github.com/webfunction-protocol/webfunction-cli).

## Usage

Each import (`merchant`, `sdk`, `terminal`) provides both a synchronus and and asynchronus client class -  `Client` and `AsynxClient` respectively. They each have a `new_client` method which will return a fully configured client, ready to access the associated API.

```python
from reservepay.merchant import Client

merchant_client = Client.new_client(bearer_auth="MY_API_KEY")
available_api_versions = merchant_client.available_api_versions()
```
```
