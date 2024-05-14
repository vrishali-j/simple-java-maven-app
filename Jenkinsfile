pipeline {
    agent any
    environment {
        PATH="$PATH:/opt/maven/bin"
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
