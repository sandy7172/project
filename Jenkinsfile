pipeline {
    agent any

    stages {
        stage('Validate) {
            steps {
                echo 'Code Validation..'
                sh 'mvn compile'
            }
        }
        stage('Unite Test') {
            steps {
                echo 'mvn Testing..'
                sh 'mvn testing'
            }
        }
        stage('Sonar Analysis') {
            steps {
                echo 'Sonar Analysis....'
                sh 'mvn sonar:sonar -Dsonar.host.url=http://3.0.146.79:9000 -Dsonar.login=ab1b71a448e066106050263c288a12b0e62ff80c'
            }
        }
    }
}
