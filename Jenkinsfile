pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin900529!'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.1.85' //private IP
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin' //jenkins global 
    }
    
    stages {
        stage('Build'){
            steps {
                sh 'mvn -s setting.xml -DskipTests install'
            }
        }
    }
}