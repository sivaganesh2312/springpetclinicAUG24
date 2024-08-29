pipeline {
  agent { label 'spc' }
  stages {
	stage('git') {
		  steps {
			git url: 'https://github.com/sivaganesh2312/springpetclinicAUG24.git', branch: 'main'
		  }
	}
	stage('build') {
	  steps {
		sh 'mvn clean package'
		junit testResults: '**/surefire-reports/*.xml'
		archive '**/target/spring-petclinic-*.jar'
	  } 
	}

  }

}