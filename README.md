# Node.js and React Speech-to-Text Demo

This is a simple app that demonstrates how to use the Google Speech-to-Text API in a Node.js and React application.

## Requirements

- Node.js (tested with version 14.x)
- React (tested with version 16.x)
- Google Cloud Platform Service Account Key with Speech-to-text api permissions

  > Follow this [tutorial](https://console.cloud.google.com/welcome?q=search&referrer=search&project=speech-to-text-test-371505&walkthrough_id=speech-to-text--speech-to-text-v2-nodejs) to create credentials and learn how to use the Google-Speech-To-Text API

## Setup

1.  Clone this repository: `git clone https://github.com/untilhamza/Real-time-transcription-with-Google-speech-to-text-API.git`

### Frontend part

1.  Navigate to the react-app project directory: `cd stt-client`
2.  Install dependencies: `yarn`
3.  Start the development server: `yarn start`
4.  Navigate back to the parent directory : `cd..`

The app will now be running at [http://localhost:3000](http://localhost:3000/).

### Add Credentials

1. Make sure to get a Google cloud Service Account Key as shown in this [tutorial](https://console.cloud.google.com/welcome?q=search&referrer=search&project=speech-to-text-test-371505&walkthrough_id=speech-to-text--speech-to-text-v2-nodejs)
2. Download the generated Service Account key json file save it to the server folder as `speech-to-text-key.json`.
   > This file name is already added to the .gitignore file but make sure not to push to github or any public repositories
3. Open the server folder and add this line in `index.js` file to add google credentials to our node js backend.

```
process.env.GOOGLE_APPLICATION_CREDENTIALS = "./speech-to-text-key.json"; //TODO: set this to the path for your Service account key JSON file
```

### Backend part

1.  Navigate to the server project directory: `cd server`
2.  Install dependencies: `yarn`
3.  Start the development server: `yarn run dev`
4.  Start the development server: `npm start`

The backend listens at [http://localhost:8081](http://localhost:8081/).

## Usage

To use the app, simply click the "Start Recording" button and speak into your microphone. The transcription will appear on the screen as you speak, updating in real-time. When you're finished, click the "Stop Recording" button to see the final transcription.

## Credits

This app was built by [Hamza](https://github.com/untilhamza) using the Google Speech-to-Text API.

## License

This project is licensed under the MIT License. See the [LICENSE](https://opensource.org/licenses/MIT) file for more details.
