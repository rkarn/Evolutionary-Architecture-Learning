Option-2 for Mongodb

    Get the mongodb container from here: https://www.thachmai.info/2015/04/30/running-mongodb-container/
    Run these commands: 
    mkdir ~/data
    sudo docker run -d -p 27017:27017 -v ~/data:/data/db mongo
    docker exec -it <mongo-db container id>

    Install the MongoDB client
    sudo apt-get install mongodb-clients

    Change mydb to the name of your DB
    mongo localhost/mydb

    Install Java by running these commands: 
    apt-get install default-jre
    apt-get install default-jdk

    performance test:   https://github.com/idealo/mongodb-performance-test
