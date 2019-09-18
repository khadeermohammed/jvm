pipeline {
    agent any
    stage('SCM Checkout'){
        git 'https://github.com/demise712/jdk'
    }
    stage('Compile-Package') {
        def mvnHome = tool name: '', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
}
