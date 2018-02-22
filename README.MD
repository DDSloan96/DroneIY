This is the repository for the yet to be started Drone It Yourself project.  

This project will contain a frontend, backend and arduino component that will be able to control a "Drone" of your choosing. 

Initially only planes will be included in this but over time support will be added for helicopters, cars, quadcopters and whatever other drones are requested.  

The goal of this project is to cover multiple tech stacks as well as give me a pet project to do.  

This project will move in 3 stages before it will be considered a BETA:
   1. Web front end that has Basic UI elements and navigation.  This will just produce dummy messages in the console correlating to the values that will eventually be passed to the backend
   2. Python based backend.  This backend will consist of multiple microservices and act as a basis for learning CI/CD, docker and kubernetes.  The backend will consist of the following parts: 
      1. Login API
      2. Location API
      3. Control API
      This will connect the front end to a database and command queuing system (Rabbit?) and spit out the instructions into log files as a standin for the arduino
    3. Ardiuno will act as the standard microcntroller at the start, this will consist of the following steps
        1. Connection testing
        2. Passing outputs from queue to console
        3. Logging back to server with results
        4. GPS location sent back to server
        5. Basic control testing on bench
        6. putting controls onto a model
        7. ground tests
        8. test flights