pipeline {
  agent any
  stages {
    stage('git clone or git pull') {
      steps {
        git url: 'https://github.com/gwarang/test3.git', branch: 'master'
      }
    }


    stage('deployment, svc creation') {
      steps {
        sh '''
	kubectl apply -f blue.yaml
	'''
      }
    }
  }
}
