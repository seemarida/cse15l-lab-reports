# Lab Report 2  
---

## Part 1  
**My implementation of StringServer.java**
```
import java.io.IOException;
import java.net.URI;
import java.net.URLDecoder;
import java.io.UnsupportedEncodingException;

class Handler implements URLHandler {
    int num = 1;
    String currentStr = "";

    public String handleRequest(URI url) {
        if (url.getPath().contains("/add-message")) {
            String query = url.getQuery();
            if (query != null) {
                String[] param = query.split("=");
                if (param[0].equals("s")) {
                    try{
                        String decoded = URLDecoder.decode(param[1], "UTF-8");
                        decoded = decoded.replace("+", " ");
                        currentStr += num + ". " + decoded + "\n";
                        num++;
                        return currentStr;
                    }
                    catch (UnsupportedEncodingException e) {
                        return "Error decoding the parameter: " + e.getMessage();
                    }
                    
                }
            }
        }
        return "404 Not Found!";
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
**Using /add-message..**  
