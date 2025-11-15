# Counter-Strike Authentication Plugin

This plugin adds user authentication to your Counter-Strike server using the DKon API. Players can log in with their credentials to access specific features and functionality.

## Features

- User login integration via DKon API.
- Error handling for failed logins.
- Successful login feedback and token management.

## Prerequisites

- A Counter-Strike server with **SourceMod** and **MetaMod** installed.
- Access to the **DKon API** for user authentication.

## Installation

1. **Clone this repository** to your local machine:
   ```bash
   git clone <repository-url>
   ```

2. **Compile the Plugin**:
   Use the SourceMod compiler to compile the script included in this repository. You can use the online compiler provided by SourceMod.

3. **Deploy the Plugin**:
   Copy the compiled `.smx` file to your server's `addons/sourcemod/plugins` directory.

4. **Restart the Server**:
   Restart your Counter-Strike server to load the new plugin.

## Usage

- Players can log in using the command:
  ```
  login
  ```

- The plugin will prompt for a username and password (you may need to implement a secure way to capture this input, as the current implementation is a placeholder).

## API Details

- **API Endpoint**: `https://api.dkon.app/api/v3/method/account.signIn`
- **Request Method**: POST
- **Parameters**:
  - `clientId`: Your client ID (e.g., `1302`)
  - `username`: The player's username
  - `password`: The player's password

## Error Handling

- If the login fails, players will receive a message: `Login failed. Please check your credentials.`
- If there’s an issue with the server or connection, a general error message will be displayed.

## Future Enhancements

- Implement user registration and profile management.
- Improve security measures for handling passwords.
- Add configuration options for better user experience.

## Support

htts://DKon.app/dev

## Acknowledgments

- Thanks to the DKon API for providing the authentication services.



### Notes:
- Replace `<repository-url>` with the actual URL of your plugin repository.
- Add any relevant license information under the License section.
- Feel free to modify sections to better fit your specific plugin features or requirements.
