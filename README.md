# caloriecam

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

CalorieCam is a simple web application that uses OpenAI's GPT-4o Vision API to estimate the calorie count of a meal from a photo. Point your camera at a dish, take a picture, and get an AI-powered nutritional estimate.

## Features

- **AI-Powered Analysis**: Estimates calories from a food photo using the OpenAI GPT-4o Vision API.
- **Live Camera Preview**: Uses your device's camera to provide a live feed directly in the browser.
- **Simple Interface**: A single button to capture an image and receive the calorie estimation.

## Getting Started

Follow these steps to run the application locally.

### Prerequisites

- [Deno](https://deno.land/) runtime installed.
- An API key from [OpenAI](https://platform.openai.com/api-keys).

### Setup and Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/code4fukui/caloriecam.git
    cd caloriecam
    ```

2.  **Create an environment file:**
    Create a `.env` file in the root of the project. This file will store your API key.

3.  **Add your API key:**
    Add your OpenAI API key to the `.env` file. For the correct format, please refer to the [openai-imagerecog](https://github.com/code4fukui/openai-imagerecog/) dependency instructions.
    ```
    # .env
    OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxx
    ```

### Running the Application

1.  **Start the server:**
    Run the following command in your terminal. The `8000` can be changed to any port you prefer.
    ```sh
    deno run -A caloriecam.js 8000
    ```

2.  **Open the application:**
    Navigate to `http://localhost:8000` in your web browser. Grant camera permissions if prompted.

## Technology

- **Backend**: The server is a lightweight Deno application.
- **API**: This project uses the OpenAI Vision API to analyze images. The connection is handled by the [openai-imagerecog](https://github.com/code4fukui/openai-imagerecog/) helper library.
- **Frontend**: Plain HTML, CSS, and JavaScript.

## License

MIT License — see [LICENSE](LICENSE).