pipeline {
    agent {label 'node-slave'} 
    stages {
        stage ('git checkout') {
           steps {
               sh 'git clone https://github.com/yuvaraj-1991/hello-world.git'
               sh 'pwd'
               }
        }
         stage ('build war file') {
             steps {
                sh 'cd hello-world'
                sh 'mvn clean package'
              }
          }  
        }
    }
}
