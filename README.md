# About
Small python CLI tool to automatically generate a simple API schema.

## Usage
Make sure your `domain` is correct and complete, containing any versioning or other API details like `api.domain.com/v1` if applicable. You can both save the schema and source an existing schema using the optional `--file` argument.

| Argument | Required |  Type  |          Description          |
|----------|----------|--------|-------------------------------|
| url      | True     | String | URL to the desired endpoint.  |
| file     | False    | String | File to use as both the source input and target output for the schema. Only requires a file name and uses the working directory by default. Can include the complete path or relative path if desired. |

**Call Without File**
```bash
spi 'https://domain.com/v1/endpoint/etc?params={param}'
```

**Call With File**
```bash
spi 'https://api.domain.com/v1/endpoint/etc' --file='schema.json'
```

## Installation
You can either clone this repo and run `pip install .` or `pip install -e .`, or use the below command to install schemAPIe. The URL contains a Linux installation script for the CLI tool. Python, Git, and pipx are required to successfully install using the installation script.
```bash
curl -fsSL https://schemapie.com/install.sh | sh
```