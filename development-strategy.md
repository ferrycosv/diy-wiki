# Do-It-Yourself Wiki: development strategy

---

## 0. Setup

- Cloned repository and installed all dependencies, build and test the obfuscated demo.

---

## 1. User Story: `GET request, retrieve a single page`

- Using express framework, I can run up a server in the local machine listening for HTTP requests through an specified port number.
- User must be able to fetch information from the server using REST  API commands, the server must process the request and give back a response with the filename given as parameter and status "ok" or and status "error" and a message.
- The file `server.js` add the functionality to process incoming GET requests `/` and `/api/page/:slug`.
- Async/await functionality to process the asynchronous read file callbacks.

---

## 2. User Story: `POST request, add a new page`

- User must be able to fetch information from the server using REST  API commands, the server must process the request and give back a response with the filename given as parameter and the contents of the file in JSON given as the body with status "ok" or status "error" and a message.
- The file `server.js` add the functionality to process incoming POST requests to `/api/page/:slug`.
- Async/await functionality to process the asynchronous write file callbacks.

---

## 3. User Story: `GET request, retrieve file list from data folder`

- User must be able to fetch information from the server using REST  API commands, the server must process the request and give back a response with a list of filenames with status "ok", in case of error no response is given.
- The file `server.js` add the functionality to process incoming GET requests to `/api/pages/all`.
- Async/await functionality to process the asynchronous readdir callbacks.

---

## 4. User Story: `GET request, retrieve list all tags used`

- User must be able to fetch information from the server using REST  API commands, the server must process the request and give back a response with a list of tags used in all files with status "ok", in case of error no response is given.
- The file `server.js` add the functionality to process incoming GET requests to `/api/tags/all`.
- Async/await functionality to process the asynchronous readdir and fileread callbacks.