#!/usr/bin/env groovy

/**
 * @ Maintainer Parag Dhere<paragchintoo007@gmail.com>
 * Plugins Needed in Jenkins: Ant, Maven, Ansible, Artifactory, SonarQube,
 * PMD, JUnit, Jacoco, HTML Publisher,
 */



 try {

    node{

    def mvnHome


     stage('Tool Setup') {
                    // ** NOTE: These tools must be configured in the jenkins global configuration.

                   mvnHome = tool name: 'mvn', type: 'maven'
                }


     stage('Checkout') {

     dir('game-of-life') {
                             git url: 'https://github.com/parag007/game-of-life.git',
                                     branch: 'master'
     }

     }

    }




 }catch (exc) {
      error "Caught: ${exc}"
  }