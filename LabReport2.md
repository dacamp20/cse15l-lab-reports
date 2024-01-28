# Lab Report 2

---
My ChatServer code:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-01-28%20004714.jpg?raw=true)

---

For each of the two examples, describe:

1. Which methods in your code are called?
2. What are the relevant arguments to those methods, and the values of any relevant fields of the class?
3. How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

---

**Example #1**

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-01-27%20232209.jpg?raw=true)

- The methods called after entering `https://0-0-0-0-6789-u69i2euk7j5mqgu1eodj6pvbrc.us.edusercontent.com/add-message?s=HI&user=Dan` to the searchbar are `handleRequest(URI url)` and the `parseQueryParamters(String query)` methods. The `handleRequest(URI url)` method is called by the `Server.java` class and its purpose is to process an incoming HTTP request with the `/add-message` path , extract query parameters, and update the chat history. The `parseQueryParamters(String quesry)` method is called by the `handleRequest(URI url)` method and its purpose is to parse the query parameters from the URL query string. This method is used internally by `handleRequest` to extract and organize the parameters.
- The relevant arguments to those methods and the values of any revelant fields of the class are `https://0-0-0-0-6789-u69i2euk7j5mqgu1eodj6pvbrc.us.edusercontent.com/add-message` which is the full URL recieved as an HTTP request and the `s=HI&user=Dan` is the query part of the URL which contains key-value pairs seperated by "&". The `query = s=HI&user=Dan` contains the parameters along with their values `"s" = HI` and `"user" = Dan`.
- The values of the revelant fields of the class change by updating the `chatMessages` field with a new message `Dan: HI\n` because the parameters are `"s" = , HI` and `"user" = Dan`.

  ---

**Example #2**

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-01-28%20003600.jpg?raw=true)

- The methods called after entering `https://0-0-0-0-6789-62cva0863i62omk16i5h7tmq4s.us.edusercontent.com/add-message?s=Hello%20how%20are%20you&user=Rob` to the searchbar are `handleRequest(URI url)` and the `parseQueryParamters(String query)` methods. The `handleRequest(URI url)` method is called by the `Server.java` class and its purpose is to process an incoming HTTP request with the `/add-message` path , extract query parameters, and update the chat history. The `parseQueryParamters(String quesry)` method is called by the `handleRequest(URI url)` method and its purpose is to parse the query parameters from the URL query string. This method is used internally by `handleRequest` to extract and organize the parameters.
- The relevant arguments to those methods and the values of any revelant fields of the class are `https://0-0-0-0-6789-62cva0863i62omk16i5h7tmq4s.us.edusercontent.com/add-message` which is the full URL recieved as an HTTP request and the `s=Hello how are you&user=Rob` is the query part of the URL which contains key-value pairs seperated by "&". The `s=Hello how are you&user=Rob` contains the parameters along with their values `"s" = Hello how are you` and `"user" = Rob`.
- The values of the revelant fields of the class change by updating the `chatMessages` field with a new message `Rob: Hello how are you\n` because the parameters are `"s" = Hello how are you` and `"user" = Rob`.

---
