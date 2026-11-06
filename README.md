package Test.Test;

import java.io.FileReader;
import java.io.IOException;
import org.json.simple.JSONObject;
import org.json.simple.parser.JSONParser;

public class ReadJSON {

    public static void main(String[] args) throws Exception {

        JSONParser jsonparser = new JSONParser();

        FileReader reader = new FileReader(".\\JSON\\student.json");

        Object obj = jsonparser.parse(reader);

        JSONObject studentobj = (JSONObject) obj;

        String FirstName = (String) studentobj.get("FirstName");
        String LastName = (String) studentobj.get("LastName");

        System.out.println("FirstName: " + FirstName);
        System.out.println("LastName: " + LastName);

        reader.close();
    }
}





import java.io.FileReader;
import java.io.IOException;
import java.text.ParseException;
import org.json.simple.JSONObject;
import org.json.simple.parser.JSONParser;

public class ReadJSON {
    public static void main(String[] args)
            throws IOException, ParseException,
            org.json.simple.parser.ParseException {

        JSONParser jsonparser = new JSONParser();

        FileReader reader = new FileReader("JSON/student.json");

        Object obj = jsonparser.parse(reader);

        JSONObject studentobj = (JSONObject) obj;

        String fname = (String) studentobj.get("firstname");
        String lname = (String) studentobj.get("lastname");

        System.out.println("Firstname: " + fname);
        System.out.println("Lastname: " + lname);
    }
}


docker build -t sandya .

docker run -d --name contain12 -p 8091:80 sandya

docker tag sha256:6a4e8da48806a13ea346f650b1021695fbbc80ac7e634238efaeaafb84ee8cf3 usha8548/sandya

kubectl version

kubectl get nodes

kubectl apply -f deployment.yml

kubectl get deployments

kubectl get pods

kubectl apply -f service.yml

kubectl get services

kubectl get pods

kubectl scale deployment sandya --replicas=5

kubectl delete pod usha-88cb86775-g6xqg
