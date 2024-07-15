# Simple Clock Project

This project is a simple clock application built using React. It displays the current time and updates every second. The application also includes a button to manually update the time.

## Code Overview

The core functionality of the clock is implemented in the `App` component, which is defined in `App.js`. The clock updates every second using the `setInterval` function and React's state management.

```jsx
import React from 'react';

function App() {
  setInterval(updateTime, 1000);
  const now = new Date().toLocaleTimeString('it-IT');
  const [time, setTime] = React.useState(now);

  function updateTime() {
    const newTime = new Date().toLocaleTimeString('it-IT');
    setTime(newTime);
  }

  return (
    <div className="container">
      <h1>{time}</h1>
      <button onClick={updateTime}>Get Time</button>
    </div>
  );
}

export default App;
```
## How It Works

* **State Initialization**: The current time is initialized using the `useState` hook.
* **Time Update**: The `setInterval` function is used to call the `updateTime` function every second.
* **Manual Update**: A button is provided to manually update the time by calling the `updateTime` function on click.

## Running the Project

To run this project locally, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/simple-clock.git
   cd simple-clock
   ```
2. **Install Dependencies**:
  ```bash
    npm install
  ```
3. **Start the Application**:
  ```bash
  npm start
  ```
4. View in Browser: Open your browser and navigate to http://localhost:3000 to see the clock in action.
   
   ## Project Structure
```plaintext
.
├── src
│   ├── App.js     # Main application file containing the clock logic
│   ├── index.js   # Entry point of the React application
│   └── index.css  # Styling for the application
├── public
│   ├── index.html # Main HTML file
│   └── ...
├── package.json   # Project dependencies and scripts
├── .gitignore     # Files and directories to ignore in git
└── README.md      # Project documentation
```

![Screenshot (343)](https://user-images.githubusercontent.com/106341416/170888156-853b9aa0-28d4-4539-969f-7f5845d24448.png)
