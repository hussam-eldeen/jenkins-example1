pipeline {
    tools {
    maven 'maven_3_5_0'
    }
    agent any

     stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven){
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh  'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh  'mvn deploy'
                }
            }
        }
      }

}
