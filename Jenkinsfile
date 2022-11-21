node {
    stage('download') {
    git 'https://github.com/Ruturaj-github/multibranch.git'
}
	stage('build') {
	sh 'mvn package'
}
	stage('deploy') {
	deploy adapters: [tomcat9(credentialsId: 'Tomcat user', path: '', url: 'http://172.31.38.189:8080')], contextPath: 'abc', onFailure: false, war: '**/*.war'
 } 
}
