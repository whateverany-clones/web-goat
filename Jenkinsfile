#!/usr/bin/env groovy
/*
 *****************************************************************************
 *
 *
 *
 *****************************************************************************
 */
@Library('JenkinsLibrary@master')

node() {
    stage('checkout') {
        checkout scm
    }


    // SonarQube plugin for Gradle requires Java 1.8
    stage('compile') {
            try {
                sh 'mvn compile'
            } catch (err) {
                println("#ci", "#C80000", "Fail compile")
                error()
            }
        }
/*
        checkmarx {
            script=this
        }

        sonar {
            script=this
        }

*/
}

