pipeline {
    agent any

    stages {
        stage('git scm checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Durgesh-Dhore/maven-project-new.git'
            }
        }
        stage('build') {
            steps {
                withMaven(jdk: 'JAVA_HOME', maven: 'MVN_HOME', traceability: true) {
                sh 'mvn validate'
}
            }
        }
        stage('compile') {
            steps {
                withMaven(jdk: 'JAVA_HOME', maven: 'MVN_HOME', traceability: true) {
                sh 'mvn compile'
}
            }
        }
    }
}
