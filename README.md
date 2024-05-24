/*Socket programming in Java*/

import java.net.*;

import java.io.*;

public class Server {

public static void main(String[] args) {

try {

ServerSocket serverSocket = new ServerSocket(5000);

Socket socket = serverSocket.accept();

DataInputStream in = new DataInputStream(socket.getInputStream());

System.out.println("Message from client: " + in.readUTF());

serverSocket.close();

} catch (IOException e) {

e.printStackTrace();

}

}

}
