# Ansible-config-mgt

iam editing this repository
let me see if it will work

am doing project 12 right now


##### Jenkinsfile for quick access

######################
# pipeline {
  agent any


  stages{
      stage("Initial cleanup") {
          steps {
            dir("${WORKSPACE}") {
              deleteDir()
            }
          }
        }

      stage('Build') {
         steps{
            script {
              sh 'echo "building stage"'  
            }
         }
       }

      stage('Test') {
        steps {
          script {
              sh 'echo "Testing stage"'
          } 
        }
     }

      stage('Package') {
        steps {
          script {
              sh 'echo "packaging app"'
          } 
         }
      }

      stage('Deploy'){
        steps{
            script {
                sh 'echo "deploying to dev"'
            }
        }
      }

      stage('clean up'){
        steps {
            cleanWs()
        }
        }
      }
   }
   ''''''''''''''''''''''''''''''