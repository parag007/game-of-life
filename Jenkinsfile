#!/usr/bin/env groovy

/**
 * @ Maintainer Parag Dhere<paragchintoo007@gmail.com>
 * Plugins Needed in Jenkins: Ant, Maven, Ansible, Artifactory, SonarQube,
 * PMD, JUnit, Jacoco, HTML Publisher,
 */



 try {

    node{

            def mvnHome
            def mvnAnalysisTargets = '-P metrics pmd:pmd test '
            def artifactoryPublishInfo
            def artifactoryServer
            def isArchivalEnabled = true
            def isDeploymentEnabled = true
            //params.IS_DEPLOYMENT_ENABLED // Enable if you want to deploy code on app server
            def isSeleniumTestingEnabled = true
            //params.IS_SELENIUM_TESTING_ENABLED // Enable if you want to generate reports
            def isReportsEnabled = true
            //params.IS_REPORTS_ENABLED // Enable if you want to generate reports

           // def artifactName = appName // name of the war/jar/ear in artifactory
            def artifactExtension = "jar"
            def artifactoryRepoName = 'DevOps' // repo name in artifactory
            //def artifactoryAppName = appName // application name as per artifactory
            def artifactoryTempFolder = 'downloadsFromArtifactory'
            // name of the local temp folder where file(s) from artifactory get downloaded



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