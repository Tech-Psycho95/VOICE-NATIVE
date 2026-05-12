# Voice Native - Next.js ElevenLabs Demo

This is a minimal Next.js application that demonstrates a voice-native workflow using the ElevenLabs Text-to-Speech API.

## Features

- **Text-to-Speech:** Convert text input into spoken audio.
- **Speech-to-Text:** Use the browser's Web Speech API to transcribe voice input into text.
- **Simple UI:** A clean interface with a text box, a "Speak" button, and a microphone button.

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [npm](https://www.npmjs.com/)
- An [ElevenLabs](https://beta.elevenlabs.io/) account and API key.

## Getting Started

1.  **Install dependencies:**

    ```bash
    npm install
    ```

2.  **Set up environment variables:**

    Create a file named `.env.local` in the root of the project and add your ElevenLabs API key:

    ```
    ELEVENLABS_API_KEY=your_elevenlabs_api_key_here
    ```

3.  **Run the development server:**

    ```bash
    npm run dev
    ```

    Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## How to Use

1.  **Text-to-Speech:**
    -   Type some text into the input box.
    -   Click the "Speak" button.
    -   The application will call the backend, generate the audio using ElevenLabs, and play it back in the browser.

2.  **Speech-to-Text:**
    -   Click the microphone button to start recording.
    -   The browser may ask for permission to use your microphone.
    -   Speak clearly into your microphone. Your speech will be transcribed in real-time into the text box.
    -   Click the microphone button again to stop recording.

## Project Structure

-   `src/app/page.tsx`: The main frontend component with the UI and client-side logic.
-   `src/app/api/speak/route.ts`: The Next.js API route that handles the text-to-speech conversion using the ElevenLabs API.
-   `.env.local`: Configuration file for environment variables (not committed to Git).

## Customization

-   **Voice:** You can change the voice used for text-to-speech by modifying the `voice` parameter in `src/app/api/speak/route.ts`. A list of available voices can be found in your ElevenLabs account.
-   **Styling:** The application uses Tailwind CSS for styling. You can customize the appearance by editing the class names in `src/app/page.tsx` and the configuration in `tailwind.config.ts`.

