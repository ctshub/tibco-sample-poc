pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /host_mnt/C/Users/brock/.m2":/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                dir('tibco.sample.ems.poc.application.parent'){
                    sh 'mvn -U -DskipTests clean package' 
                }
                
            }
        }
    }
}
