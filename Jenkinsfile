pipeline {
    agent any
    tools {
        maven 'mvn'
//        jdk 'jdk8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Build') {
            steps {
                echo 'Cloning Project!!!'

                git 'https://github.com/parag007/game-of-life.git'

                sh 'mvn install'
                sh 'mvn compile'
                sh 'mvn test'

            }
        }

        stage ('UnitTest') {

            steps{

                dir ('/var/lib/jenkins/jobs/gamelife/workspace/gameoflife-acceptance-tests') {
            //     readFile '/var/lib/jenkins/jobs/gamelife/workspace/gameoflife-acceptance-tests'

               // sh 'mvn clean verify'

                   sh 'mvn -Dmaven.test.failure.ignore=true clean install'
                }

           }


        }
    }
}