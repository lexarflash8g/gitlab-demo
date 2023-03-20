#!/usr/bin/env groovy

pipeline {
    agent any
    tools {
        maven 'maven-3.6.0'
    }
    

    stages {

 
        // stage("init") {
        //     steps {
        //         script {
        //             gv = load "script.groovy"

        //         }
        //     }
        // }
        // stage('build') {
        //     steps {
        //         script {
        //             gv.buildApp()
        //         }
        //     }
        // }


        // stage('test') {
        //     when {
        //         expression {
        //             params.executeTests
        //         }
        //     }
            
        //     steps {
        //         script {
        //             gv.testApp()
        //         }
        //     }
        // }



        stage("build jar") {
            steps {
                script {
                    echo "building the application"
                    sh 'mvn package'
                }
            }
        }

            stage("build image") {
            steps {
                script {
                    echo "building the application"
                       { 
                        
                        sh 'docker build -t lexarflash8g/bootcampdevops:jma-2.0 .'
                        sh "docker login -u lexarflash8g -p Arminvan99{$}{$}"
                        sh 'docker push  lexarflash8g/bootcampdevops:jma-2.0'
                     }
            }
        }
                }
        
        
            stage('deploy') {
            
            steps {
                script {

                    echo "deploying the application...."

                   

                  
                }
            }
        }
    }
}

