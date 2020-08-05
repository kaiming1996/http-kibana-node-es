# http-kibana-node-es

Connects External Kibana with Amazon ES. It uses the aws-sdk to make signed requests to an Amazon ES endpoint.

## Installation

Add this folder into [elasticsearch-js/src/lib](https://github.com/elastic/elasticsearch-js/src/lib)
Change the client.js file in [elasticsearch-js/src/lib](https://github.com/elastic/elasticsearch-js/src/lib) to [http-kibana-node-es/client.js](https://github.com/kaiming1996/http-kibana-node-es/blob/master/client.js)

## Usage

Change the Kibana dependecy of elasticsearch, from elasticsearch to the modified elasticsearch-js path

Inside Kibana folder
```bash
# Reinstall the dependency
yarn add aws-sdk
yarn kbn bootstrap
yarn start --oss
```

## Credentials

The connector uses aws-sdk's default behaviour to obtain region + credentials from your environment [process.env]. If you would like to set these manually, you can change them inside client.js file:
