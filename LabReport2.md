# Lab Report 2

**Part #1:**

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

**Part 2:**

Using the command line, show with ls and take screenshots of:

- The absolute path to the private key for your SSH key for logging into ieng6:
  
  `ls /c/Users/danca/.ssh/id_rsa`
  
![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-01-29%20142605.jpg?raw=true)

- The absolute path to the public key for your SSH key for logging into ieng6:
  
    `ls /home/linux/ieng6/oce/80/dacampuzano/.ssh/authorized_keys`
  
![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-01-29%20142803.jpg?raw=true)

- A terminal interaction where you log into your ieng6 account without being asked for a password:
![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-01-29%20142859.jpg?raw=true)

---

**Part 3:**

In weeks 2 and 3 of the lab, I learned to create a Java file named SearchEngine.java to implement a web server capable of tracking a list of strings. This server supports paths for adding new strings to the list and querying the list to return all strings containing a given substring. Additionally, I gained knowledge in developing a web server named ChatServer.java that manages user input messages, keeping track of a single string updated by incoming requests along with the user who wrote each message. Furthermore, I acquired skills in setting up SSH keys for easy access and learned about two new commands `scp` and `mkdir` as well as their functionality.
