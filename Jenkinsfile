node {
    stage('SCM Checkout'){
        git url: 'https://github.com/demise712/jdk.git'
    }
    stage('Compile-Package') {
        def mvnHome = tool name: 'MAVEN3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    ansiColor('xterm') {
    ansiblePlaybook(
        playbook: '/var/lib/jenkins/workspace/jvm2/oracle_jdk.yml',
        colorized: true)
   }
}
