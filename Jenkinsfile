node {
    stage('SCM Checkout'){
        git url: 'https://github.com/khadeermohammed/jvm.git',
            credentialID: 
            branch: 'master'
    }
    stage('Compile-Package') {
        def mvnHome = tool name: 'MAVEN3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy JDK') {
        sh 'sudo ansible-playbook /var/lib/jenkins/workspace/jvm_build/oracle_jdk.yml'
  
    }      
}
