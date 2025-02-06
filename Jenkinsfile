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
         stage {'deploy to Tomcat'} {
              steps {
                  sh 'echo "Deploying to tomcat"'
                  sh 'sudo cp -R sudo cp -R target/hello-world-war-null.war /opt/tomcat/apache-tomcat-10.1.34/webapps'
                  sh 'sudo bash /opt/tomcat/apache-tomcat-10.1.34/bin/.stop.sh'
                  sh 'sudo bash /opt/tomcat/apache-tomcat-10.1.34/bin/.start.sh'
              }
          }
        }
    }

