node {
    stage('SCM Checkout'){
        git 'https://github.com/demise712/jdk'
    }
    stage('Compile-Package') {
        sh 'mvn package'
    }
}
