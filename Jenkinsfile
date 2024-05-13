pipeline {
    agent any
    
    environment {
        PATH="/usr/local/bin:/usr/bin:/bin:/home/vrishalijavere/apache-maven-3.8.8/bin:/home/vrishalijavere/java/openjdk-21.0.3+1/bin"
    }

    stages {
        stage('Build') { 
            steps {
                echo "PATH is: $PATH"
                sh 'source ~/.profile'
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
