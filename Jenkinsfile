node {
    stage('SCM Checkout'){
        git 'https://github.com/demise712/jdk'
    }
    stage('Compile-Package') {
        def mvnHome = tool name: 'MAVEN3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
}
