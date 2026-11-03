pipeline {
    agent any

    stages {
        stage('Dependencies') {
            steps {
                build job: 'account', wait: true
            }
        }
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean install'
            }
        }
    }
}
