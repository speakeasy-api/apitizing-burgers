<div align="center">
 <a href="https://www.speakeasy.com/" target="_blank">
  <img width="1500" height="500" alt="Speakeasy" src="https://github.com/user-attachments/assets/0e56055b-02a3-4476-9130-4be299e5a39c" />
 </a>
 <br />
 <br />
  <div>
   <a href="https://speakeasy.com/docs/create-client-sdks/" target="_blank"><b>Docs Quickstart</b></a>&nbsp;&nbsp;//&nbsp;&nbsp;<a href="https://go.speakeasy.com/slack" target="_blank"><b>Join us on Slack</b></a>
  </div>
 <br />

</div>

<p align="center">
<img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi">
<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
</p>

<h1>
 APItizing Burgers API: an example API to manage burgers and orders in a restaurant
</h1>

</div>

This example API demonstrates Speakeasy's recommended practices for generating clear OpenAPI specifications.

## Install FastAPI

To install and run this example, you'll need a Python virtualenv with FastAPI installed.

1. Activate your Python virtualenv.
2. Install FastAPI. Run the following in the terminal:

    ```bash
    pip install "fastapi[all]"
    ```

3. Clone this repo:

    ```bash
    git clone git@github.com:ritza-co/apitizing-burgers.git
    ```

## Run FastAPI server

1. In the `app` directory, run:

    ```bash
    uvicorn main:app --reload
    ```

2. Open this link in your browser: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

## Install Speakeasy

To save OpenAPI output to a file and regenerate the SDK with Speakeasy, first install Speakeasy by following the [Speakeasy Getting Started](https://speakeasyapi.dev/docs/product-reference/speakeasy-cli/getting-started/) guide.

On macOS, you can install Speakeasy using Homebrew.

In your terminal, run:

```bash
brew install speakeasy-api/homebrew-tap/speakeasy
```

## Regenerate the `openapi.yaml`, `openapi.json` and the client SDK

In the project's directory, run:

```bash
./gen.sh
```
