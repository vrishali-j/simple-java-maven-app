pipeline {
    agent any
    node {
      withEnv(['PATH=$PATH:/opt/maven/bin']) {
    }
    }
    
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
