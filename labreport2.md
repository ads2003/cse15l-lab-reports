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


