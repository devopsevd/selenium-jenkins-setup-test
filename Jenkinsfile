node{

    checkout scm
    def mvnHome
	mvnHome = tool 'Maven'

        stage('Run Tests') {
            sh "'${mvnHome}/bin/mvn' -Dgrid.server.url=http://seleniumhub:4444/wd/hub clean test "
        }
        stage('Functional Test Results') {
            junit '**/target/surefire-reports/TEST-*.xml'
        }
 }
