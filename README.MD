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

        This segment is the most costly and will take the longest. Acceptance criteria for a first "ALPHA" build will be as follows:
        NOTE: These milestones will be completed in order for safety concerns
            1. Manual/Automatic switch - Manual control of the craft via radio must be able to be flipped to at all times, this will be a radio based switch
            2. On loss of connection to control server the following behaviors will happen:
                1. Fixed wing: Circle over current position until manual control is enabled and first maneuver initiated
                2. Quadcopter: Hover
                3. Helicopter: Hover
                4. Ground/water vehicle: Stop completely
            3. If GPS is lost same behaviors as above, fixed wing will not hav gps guidance and will fall back to preprogrammed routine
            4. Automated Takeoff-Plane gets airborne then circles specified location on map
        BETA Acceptance Criteria:
            1. Automated Landing
            2. Ability to set paths
            3. Full automated flights are completed, short and extended
            4. adjustments for turbulence s


Tech Stack: Will be updated as decisions are made

Database: Non-Relational database
    1. Unsure of end goal with schema
    2. Data that is in database will be changing often
    3. fairly portable and easy to install
    4. Scalable

Webapp:
    - Angular
    
API:
    - Python backend
    - Queue/pipeline between backend and device (Rabbit?)
    
