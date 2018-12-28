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
    withEnv(['JAVA_HOME=/usr/java/jdk1.8.0_92/', "VERSION=${buildVersion}", "PATH=/app/maven/apache-maven-3.6.0/bin:"+env.PATH]) {
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
}

