# Lab Report 2 - Servers and SSH Keys (Week 3)


## Part 1

~~~
import java.io.IOException;
import java.net.URI;

// Interface to handle URL requests
interface URLHandler {
    String handleRequest(URI url);
}

// Implementation of URLHandler for handling chat-related requests
class ChatHandler implements URLHandler {
    private StringBuilder chatHistory = new StringBuilder();

    @Override
    public String handleRequest(URI url) {
        String path = url.getPath();
        if ("/add-message".equals(path)) {
            String query = url.getQuery();
            if (query != null && !query.isEmpty()) {
                String[] parameters = query.split("&");
                if (parameters.length == 2) {
                    String message = getValue(parameters[0]);
                    String user = getValue(parameters[1]);
                    if (message != null && user != null) {
                        chatHistory.append(user).append(": ").append(message).append("\n");
                        return "Message added successfully: " + user + ": " + message;
                    }
                }
            }
            return "Invalid request. Both 'message' and 'user' parameters are required.";
        } else {
            return chatHistory.toString();
        }
    }

    private String getValue(String parameter) {
        String[] parts = parameter.split("=");
        return parts.length == 2 ? parts[1] : null;
    }
}

// Main class to start the chat server
class ChatServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151:");
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port, new ChatHandler());
    }
}

// Server class to simulate server functionality
class Server {
    public static void start(int port, URLHandler handler) {
        // Simulate server startup
        System.out.println("Server started on port " + port);
        // Simulate server running
        System.out.println("Server is running...");
        // Simulate server shutdown
        System.out.println("Server stopped.");
    }
}
~~~

<img width="285" alt="Screenshot 2024-04-24 at 9 34 40 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/50ae3660-30b6-42c7-af45-f3791f789c08">


<img width="265" alt="Screenshot 2024-04-24 at 9 34 33 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/e6ddd576-3773-434e-834b-a2c54b753e1f">


*The first screenshot depicts the invocation of the main function and handleRequest. The URL serves as the parameter for invoking the handleRequest method, whereas port 5001 is used as the argument for invoking the main function. Each time a new message is contributed via the website or after the survey is concluded, the value of s is appended and a new line is added. Furthermore, each time the program moves to the next line, the new message is added to the original empty String s. The new message is placed at index 1 of the path array.
One pertinent area of study is chat history, where the add message request is initially an empty string. Upon sending the add message request, the chat history field undergoes a transformation from an empty string to "avani.. namaste/n". When I make the second add message request, the chat history box is modified from "avani.. namaste/n" to "avani.. namaste/n".Aditya: Whats up/n?*

# Part 2


<img width="559" alt="Screenshot 2024-04-24 at 9 47 26 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/df041bab-bdbc-4cc5-9161-5c28cded082c">




<img width="191" alt="Screenshot 2024-04-24 at 9 47 40 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/30ce4d57-aaca-4dde-9267-76fd38524426">




<img width="536" alt="Screenshot 2024-05-08 at 2 52 16 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/840f185b-0949-499a-9f05-5a3668fbb055">



# Part 3 (what I Learnt)

*Building your initial webpage from the ground up. what symptoms and bugs are in software. The most important thing I learned was about junit testing, which is quite helpful for CSE programming assignments.*

