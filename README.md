# GitHub Pull Request Fetcher

A web application to fetch, display, and filter pull requests from GitHub repositories. This application utilizes a backend service to interact with the GitHub API.

## Features

- Fetch pull requests by repository owner, name, and a specified date range.
- Securely input GitHub Personal Access Token (input is masked).
- Filter fetched pull requests by their state (all, open, closed).
- Apply an additional date range filter on the fetched results.
- Paginated display of pull requests for easier navigation.
- User-friendly interface with styling reminiscent of GitHub.

## Setup and Installation

To get this project running locally, follow these steps:

1.  **Prerequisites:**
    *   Node.js and npm (or yarn) must be installed on your system.

2.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    ```

3.  **Navigate to the project directory:**
    ```bash
    cd <project-directory-name>
    ```

4.  **Install dependencies:**
    ```bash
    npm install
    ```

## Usage

1.  **Start the development server:**
    ```bash
    npm start
    ```
    This command will bundle the application using Parcel and usually serves it on `http://localhost:1234`. Open this URL in your web browser.

2.  **Using the Application:**
    *   Enter the **Owner** of the GitHub repository (e.g., `Microsoft`).
    *   Enter the **Repository** name (e.g., `vscode`).
    *   Select the **Start Date** and **End Date** to define the period for which pull requests should be fetched.
    *   Enter your **GitHub Token**. This is a Personal Access Token (PAT) with appropriate permissions to read repository data. The input field will mask your token.
    *   Click the **"Fetch Pull Requests"** button.
    *   Once results are loaded, you can:
        *   Filter by state (All, Open, Closed) using the filter buttons.
        *   Apply an additional date filter using the "Filter Start Date" and "Filter End Date" inputs and clicking "Apply Date Filter".
        *   Navigate through multiple pages of results using the pagination controls.

## Backend Service

This frontend application relies on an external backend service hosted at `https://consume-backend.onrender.com/pulls` to fetch data from the GitHub API. The GitHub token you provide is passed to this backend service, which then makes the actual requests to GitHub.

## Available Scripts

In the project directory, you can run the following scripts:

*   ### `npm start`
    Runs the app in development mode using Parcel. Open [http://localhost:1234](http://localhost:1234) (or the port Parcel assigns) to view it in the browser.

*   ### `npm build`
    Builds the app for production to the `dist` folder using Parcel. It correctly bundles JavaScript in production mode and optimizes the build for the best performance.

## Technologies Used

*   HTML
*   CSS
*   JavaScript (ES6+)
*   Parcel (for bundling and development server)
*   Font Awesome (for icons)

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

This project is licensed under the ISC License (as specified in the `package.json` file).
