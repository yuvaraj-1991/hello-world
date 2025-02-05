pipeline {
    agent {label 'node-slave'}
    stages {
        stage('Example') {            
            options {
                // Timeout counter starts BEFORE agent is allocated
                timeout(time: 1, unit: 'SECONDS')
            }
            steps {
                echo 'Hello World'
            }
        }
    }
}
