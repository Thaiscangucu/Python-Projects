# Tay Tay Says...

A desktop app that shows a random Taylor Swift quote every time you click her picture. Developed as part of the **100 Days of Code: The Complete Python Pro Bootcamp**, this project combines a graphical interface built with Tkinter and requests to a public REST API.

## Features

* **Random quotes**: each click on Taylor's picture fetches a new quote from the API
* **Graphical interface**: a window built with Tkinter, with a background image and the quote displayed on a canvas
* **API integration**: sends a `GET` request and reads the quote from the JSON response
* **Error handling**: `raise_for_status()` stops the request if the API returns an error

## Getting Started

This project requires an internet connection to communicate with the API.

### Prerequisites
* **Python 3.x** installed (Tkinter comes with Python).
* **Requests** library installed:
  ```bash
  pip install requests
  ```
* Ensure the image files `background.png` and `taylor.png` are in the same directory as `main.py`.

### How to Run
To start the app, navigate to the project folder and run the following command in your terminal:

```bash
python3 main.py
```

Click Taylor's picture to get a new quote.

## How It Works

1. When you click the button, `get_quote()` sends a `GET` request to the Taylor Swift API (`https://taylorswiftapi.onrender.com/get`).
2. The response comes back as JSON, and the app reads the value of the `quote` field.
3. The quote text on the canvas is updated with `canvas.itemconfig()`, without reopening the window.

## Project Structure

```
Taylor Swift Quotes/
├── main.py          # Window, canvas, button and API request
├── background.png   # Background image behind the quote
└── taylor.png       # Taylor's picture, used as the button
```

## What I Learned

* Building a graphical interface with **Tkinter** (window, canvas, images and buttons)
* Consuming a **REST API** with the `requests` library
* Reading data from a **JSON** response
* Updating the interface dynamically in response to user actions

> Note: the API is a free community service hosted on Render. The first request after a while may take a few seconds while the server wakes up.
