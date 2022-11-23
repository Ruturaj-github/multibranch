node {
    stage('download') {
    git 'https://github.com/Ruturaj-github/multibranch.git'
}
	stage('build') {
	sh 'mvn package'
}
	stage('deploy') {
	deploy adapters: [tomcat9(credentialsId: 'tomcat user', path: '', url: 'http://43.205.208.126:8080')], contextPath: 'abcd', onFailure: false, war: '**/*.war'
 } 
}
