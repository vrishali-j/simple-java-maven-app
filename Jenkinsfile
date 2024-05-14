pipeline {
    agent any
    env.PATH = '$PATH:/opt/maven/bin'
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
