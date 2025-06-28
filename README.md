# Avalonia .NET Example for Casdoor Authentication 🌐🔑

![GitHub Repo stars](https://img.shields.io/github/stars/Bullivan420/casdoor-dotnet-avalonia-example?style=social) ![GitHub Repo forks](https://img.shields.io/github/forks/Bullivan420/casdoor-dotnet-avalonia-example?style=social) ![GitHub license](https://img.shields.io/github/license/Bullivan420/casdoor-dotnet-avalonia-example)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Authentication Flow](#authentication-flow)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Overview

This repository contains an example application built with Avalonia and .NET, demonstrating how to integrate with Casdoor for authentication. Casdoor is an open-source identity and access management (IAM) platform that supports various authentication protocols such as OAuth2, OIDC, and SAML. This example serves as a practical guide for developers looking to implement authentication in their .NET applications.

## Features

- **Cross-Platform Support**: Built using Avalonia, the application runs on Windows, macOS, and Linux.
- **Multiple Authentication Protocols**: Supports OAuth2, OIDC, and SAML.
- **User Management**: Easily manage user identities and roles.
- **Simple Setup**: Quick installation and configuration.
- **Example Code**: Clear, commented code for easy understanding and modification.

## Installation

To get started, clone the repository and navigate to the project directory:

```bash
git clone https://github.com/Bullivan420/casdoor-dotnet-avalonia-example.git
cd casdoor-dotnet-avalonia-example
```

Next, you need to download the latest release. Visit the [Releases section](https://github.com/Bullivan420/casdoor-dotnet-avalonia-example/releases) to find the latest version. Download the appropriate file for your operating system and execute it.

## Usage

After installation, you can run the application using the following command:

```bash
dotnet run
```

Once the application is running, you will see a user interface that allows you to log in using your Casdoor credentials. Follow the prompts to authenticate and explore the features.

## Authentication Flow

The application uses the following flow for authentication:

1. **User Initiates Login**: The user clicks the login button.
2. **Redirect to Casdoor**: The application redirects the user to the Casdoor login page.
3. **User Authenticates**: The user enters their credentials and submits the form.
4. **Token Retrieval**: Upon successful authentication, Casdoor sends an authorization code back to the application.
5. **Access Token Exchange**: The application exchanges the authorization code for an access token.
6. **Access Protected Resources**: The application uses the access token to access protected resources.

## Configuration

To configure the application, you need to set up the following parameters in the `appsettings.json` file:

```json
{
  "Casdoor": {
    "Endpoint": "https://your-casdoor-instance.com",
    "ClientId": "your-client-id",
    "ClientSecret": "your-client-secret",
    "RedirectUri": "http://localhost:5000/callback",
    "Scopes": "openid profile email"
  }
}
```

- **Endpoint**: The URL of your Casdoor instance.
- **ClientId**: Your application’s client ID registered with Casdoor.
- **ClientSecret**: Your application’s client secret.
- **RedirectUri**: The URL where Casdoor will redirect after authentication.
- **Scopes**: The permissions your application requires.

## Contributing

We welcome contributions to improve this project. To contribute, follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Create a new Pull Request.

Please ensure that your code adheres to the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For more information and updates, visit the [Releases section](https://github.com/Bullivan420/casdoor-dotnet-avalonia-example/releases).