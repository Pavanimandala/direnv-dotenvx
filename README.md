# direnv-dotenvx 🌍

![GitHub release](https://img.shields.io/github/release/Pavanimandala/direnv-dotenvx.svg) ![License](https://img.shields.io/github/license/Pavanimandala/direnv-dotenvx.svg)

Welcome to the **direnv-dotenvx** repository! This project is a direnv plugin designed to streamline your environment variable management. With this tool, you can easily load `.env` or `.env.{env}` files using dotenvx. It automatically detects variables and exports them in a shell-safe manner.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Features ✨

- **Automatic Variable Detection**: The plugin scans your `.env` files and identifies variables automatically.
- **Shell-Safe Exports**: It ensures that your environment variables are exported safely for your shell sessions.
- **Easy Integration**: Seamlessly integrates with direnv to enhance your development workflow.
- **Support for Multiple Environments**: Load environment variables from different `.env` files based on the environment you are working in.
  
## Installation ⚙️

To get started with **direnv-dotenvx**, you need to install it first. You can download the latest release from the [Releases section](https://github.com/Pavanimandala/direnv-dotenvx/releases). Make sure to download the appropriate file for your system and execute it.

### Step-by-Step Installation

1. **Prerequisites**: Ensure you have `direnv` and `dotenvx` installed on your system.
   
   - To install `direnv`, you can follow the instructions [here](https://direnv.net/docs/installation.html).
   - To install `dotenvx`, visit their [GitHub repository](https://github.com/dotenvx/dotenvx).

2. **Clone the Repository**:

   ```bash
   git clone https://github.com/Pavanimandala/direnv-dotenvx.git
   cd direnv-dotenvx
   ```

3. **Install the Plugin**:

   Follow the instructions in the `INSTALL.md` file located in the cloned repository.

4. **Configure direnv**:

   Add the following line to your `.envrc` file:

   ```bash
   eval "$(direnv dotenvx)"
   ```

5. **Allow direnv**:

   Run the command below to allow direnv to load your new configuration:

   ```bash
   direnv allow
   ```

Now you are ready to use **direnv-dotenvx**!

## Usage 📚

Using **direnv-dotenvx** is straightforward. Here’s how you can load your environment variables.

### Basic Usage

1. Create a `.env` file in your project directory:

   ```bash
   touch .env
   ```

2. Add your environment variables to the `.env` file:

   ```plaintext
   DATABASE_URL=postgres://user:password@localhost:5432/mydb
   API_KEY=your_api_key_here
   ```

3. Create a `.env.{env}` file for specific environments (e.g., `.env.production`):

   ```plaintext
   DATABASE_URL=postgres://user:password@localhost:5432/prod_db
   ```

4. Activate the environment by setting the `env` variable in your `.envrc`:

   ```bash
   export ENV=production
   ```

5. When you enter the directory, **direnv** will automatically load the appropriate environment variables based on your `.env` and `.env.{env}` files.

### Advanced Usage

- **Custom Variable Prefixes**: You can customize variable prefixes in your `.env` files. Just add a prefix in your `.envrc`:

  ```bash
  export PREFIX=MYAPP_
  ```

- **Debugging**: If you encounter issues, you can enable debugging by setting:

  ```bash
  export DEBUG=true
  ```

This will provide more information about what the plugin is doing.

## Contributing 🤝

We welcome contributions to **direnv-dotenvx**! If you have suggestions or improvements, feel free to fork the repository and submit a pull request.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Submit a pull request to the main repository.

### Issues

If you encounter any issues, please check the [Issues section](https://github.com/Pavanimandala/direnv-dotenvx/issues) to see if it has already been reported. If not, feel free to open a new issue.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support 💬

For support, please visit the [Releases section](https://github.com/Pavanimandala/direnv-dotenvx/releases) to check for updates or reach out to the community.

---

Thank you for checking out **direnv-dotenvx**! We hope it makes your development experience smoother and more efficient.