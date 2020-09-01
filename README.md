# Selenium Headless Chromium Lambda Layer

This repository provides an AWS Lambda layer that can run Selenium in
a headless chromium browser.


## Getting Started


### Prerequisites

*  [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)
*  [Docker](https://docs.docker.com/get-docker/)

Properly configured [AWS credentials](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) are
also required for SAM to work properly.


### Building

To build the layer, run the following:

```bash
sam build --use-container
```

To deploy the layer to an AWS account, run this command, and follow the prompts:

```bash
sam deploy --guided
```

### Usage

Once the layer is deployed, it can be used in a Lambda function per the
[documentation](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html).

The layer uses the Python 3.6 runtime, and includes the [requestium](https://pypi.org/project/requestium/)
package for doing Selenium tests.


## Contributing

Pull requests are welcomed. Please review the [Contributing Guidelines](CONTRIBUTING.md)
and the [Code of Conduct](CODE_OF_CONDUCT.md).


## Authors

*  Jud Neer (judneer@amazon.com)


## License

This project is licensed under the MIT-0 License. See the [LICENSE](LICENSE) file for details.
