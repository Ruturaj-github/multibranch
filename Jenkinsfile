node {
    stage('download') {
    git 'https://github.com/Ruturaj-github/multibranch.git'
}
	stage('build') {
	sh 'mvn package'
}
	stage('deploy') {
	deploy adapters: [tomcat9(credentialsId: 'tomcatuser', path: '', url: 'http://172.31.56.159:8080')], contextPath: 'sagar', onFailure: false, war: '**/*.war'
 } 
}
