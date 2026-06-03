React Last Minute Questionnaire
##What is micro-frontend?
<details>
<summary>
Micro-frontends extend the concept of microservices to the frontend, enabling modular and scalable development by breaking monolithic applications into smaller, independently deployable components.
</summary>
This is possible by using the Webpack Module Federation
https://medium.com/@chirag.dave/a-complete-guide-to-react-micro-frontends-930229dc812a
</details>
##What is Context API?
<details>
<summary>
Context API is a built-in feature that allows you to manage global state and share data across your application without prop drilling.
</summary>
</details>
##What is Virtual DOM? How is it different from Real DOM? What is Shadow DOM
<details>
<summary>

</summary>
</details>

How do you handle race conditions in React when fetching data from multiple sources?
<details>
<summary>

</summary>
</details>
Race conditions can occur when multiple requests are made to the server and the responses come back in a different order than expected. To handle this in React, you can use a state variable to keep track of the latest request and ignore previous responses. Alternatively, you can use a library like Redux-Saga to handle complex asynchronous logic and ensure that actions are dispatched in the correct order.

How do you handle file uploads in React using Axios or Fetch?
<details>
<summary>

</summary>
</details>
To handle file uploads in React, you can use the FormData API to create a new FormData object that contains the file data. You can then send this data to the server using Axios or Fetch. It's important to set the Content-Type header to multipart/form-data to indicate that you are uploading a file.

How do you handle file downloads in React using Axios or Fetch?
<details>
<summary>

</summary>
</details>
To handle file downloads in React, you can send a GET request to the server using Axios or Fetch. The server should then respond with the file data and set the Content-Disposition header to attachment to indicate that the response should be downloaded rather than displayed in the browser. You can then use the FileSaver library to save the file to the user's computer.

How do you handle binary data in React using Axios or Fetch?
<details>
<summary>

</summary>
</details>
To handle binary data in React, you can set the responseType option to arraybuffer or blob when making a request with Axios or Fetch. This will ensure that the response is returned as binary data that can be processed in the browser.

How do you implement a file upload progress bar in React using Axios or Fetch?
<details>
<summary>

</summary>
</details>
To implement a file upload progress bar in React, you can use the onUploadProgress callback in Axios or Fetch to track the progress of the upload. You can then update the UI with the progress information and display a progress bar to the user.

How do you implement a file download progress bar in React using Axios or Fetch?
<details>
<summary>

</summary>
</details>
To implement a file download progress bar in React, you can use the onDownloadProgress callback in Axios or Fetch to track the progress of the download. You can then update the UI with the progress information and display a progress bar to the user.

How do you handle JSON Web Tokens (JWT) when fetching data using Axios or Fetch?
<details>
<summary>

</summary>
</details>
You can store the JWT in the browser's localStorage or sessionStorage and include it in the Authorization header of the request as Bearer

How do you implement retries in React when fetching data using Axios or Fetch?
<details>
<summary>

</summary>
</details>
You can implement retries using a combination of a loop and a timeout function. The loop will make the request multiple times until it succeeds, and the timeout function will introduce a delay between each attempt.

How do you implement exponential backoff in React when fetching data using Axios or Fetch?
<details>
<summary>

</summary>
</details>
Exponential backoff can be implemented by increasing the delay between each retry attempt based on a power of 2. For example, the delay for the first retry could be 1 second, the second retry could be 2 seconds, the third retry could be 4 seconds, and so on.

How do you handle timeouts when fetching data using Axios or Fetch?
<details>
<summary>

</summary>
</details>
You can set a timeout value in the options object passed to the Axios or Fetch request. If the request does not receive a response within the specified timeout duration, it will throw an error.


Speed Optimization
How do you handle data caching in React to improve performance and reduce network requests?

<details>
<summary>

</summary>
</details>To handle data caching in React, you can use a caching library like React-Cache or Redux-Persist. These libraries allow you to store the data in memory or in the browser's local storage and retrieve it later, instead of making a network request every time. You can also use a caching strategy like time-based or cache-control headers

##How do you implement optimistic updates in React when fetching data?
<details>
<summary>
Optimistic updates involve updating the UI before receiving the server response. To implement this in React, you can first update the UI with the new data and then send the request to the server. If the server responds with an error, you can revert the UI to its previous state.
</summary>

</details>

###Securing React Application
#Submit sast and dast scan
###Template Injection
#Trust Policy
###How to whitelist component
##Insecure Direct Object Reference
#CSRF - Cross Site Direct Forgery