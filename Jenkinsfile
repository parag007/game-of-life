#!/usr/bin/env groovy

/**
 * @ Maintainer Parag Dhere<paragchintoo007@gmail.com>
 * Plugins Needed in Jenkins: Ant, Maven, Ansible, Artifactory, SonarQube,
 * PMD, JUnit, Jacoco, HTML Publisher,
 */



 try {

    node{

           // def mvnHome = 'mvn'

            stage('Tool Setup') {
                    // ** NOTE: These tools must be configured in the jenkins global configuration.

                           maven 'mvn'
                            //  mvnHome = tool 'mvn'
                }


             stage('Build') {

                   echo '------------Cloning Repo----------------'
                    dir('game-of-life') {
                                 git url: 'https://github.com/parag007/game-of-life.git',
                                         branch: 'master'
                            }

                            sh 'mvn compile'






                }



             stage('Test') {
                         //steps {
              //sh './jenkins_build.sh'
                 //junit '*/build/test-results/*.xml'
                 //step([$class: 'JacocoPublisher',
                 //execPattern: 'target/*.exec',
                 //classPattern: 'target/classes',
                 //sourcePattern: 'src/main/java',
                 //exclusionPattern: 'src/test*'
        //         ])
          //      }
         }

    }




 }catch (exc) {
      error "Caught: ${exc}" }