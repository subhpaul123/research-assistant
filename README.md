# AI-POWERED RESEARCH ASSISTANT

## Overview

The AI-Powered Research Assistant is a Spring Boot application designed to process research requests using an AI model. It allows users to submit content and specify operations such as summarization or topic suggestion, leveraging an external AI service.

This application also comes with a **Chrome Extension**  that interacts with the backend to process highlighted content on webpages.

## Features

- **Content Processing**: Users can submit text content for processing.

-   **AI Integration**: Utilizes an external AI model to generate summaries or suggest related topics.

-   **RESTful API**: Exposes endpoints for interaction with the application.

-   **Chrome Extension**: Allows users to send content directly from any webpage for quick processing.

## Technologies Used

- **Java**: The primary programming language.

- **Spring Boot**: Framework for building the application.

- **Lombok**: For reducing boilerplate code.

- **WebClient**: For making HTTP requests to the AI model API.

- **Jackson**: For JSON processing.

## Getting Started

### Prerequisites

-   Java 21 or higher

-   Maven

-   Google Chrome

### Installation

#### Backend Setup

1.  Clone the repository:

    ```bash
    git clone https://github.com/subhpaul123/research-assistant.git 
    cd research-assistant
    ```

2.  Set up environment variables for the AI API:

    ```bash
    export GEMINI_API_URL=<your_api_url>
    export GEMINI_API_KEY=<your_api_key>
    ```

3.  Build the project:

    ```bash
    mvn clean install
    ```

4.  Run the application:

    ```bash
    mvn spring-boot:run
    ```

#### Chrome Extension Setup

1.  Open Google Chrome and go to `chrome://extensions/`

2.  Enable **Developer mode** (top right toggle).

3.  Click **Load unpacked**  and select the `chrome-extension`  folder from this project directory.

4.  Once loaded, the extension will appear in your Chrome toolbar.

5.  Highlight text on any webpage and use the extension to send content to the backend for summarization or topic suggestions.

### API Endpoints

-   **POST /api/research/process**

    -   **Request Body**:

        ```json
        {
          "content": "Your text content here",
          "operation": "summarize" // or "suggest"
        }
        ```

    -   **Response**: Returns the processed result as a string.

## Usage

Send a POST request to `/api/research/process`  with the required JSON body to get the AI-generated response. The Chrome extension simplifies this process by allowing you to send highlighted text directly from any webpage.

## Testing

To run the tests, use:


```bash
mvn test
```

## License

This project is licensed under the MIT License.
