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
                echo 'This is a minimal pipeline.'

                git 'https://github.com/parag007/game-of-life.git'

            }
        }
    }
}