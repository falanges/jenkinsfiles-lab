pipeline {
  agent any

  environment {
    DEMO = '1'
  }

  stages {
    stage('stage1') {
      steps {
        echo "This is build $BUILD_NUMBER of demo $DEMO"
        sh '''
        echo "Using a multiline shell step"
        chmod +x ../test.sh
        cd .. && ./test.sh
        '''
      }
    }
  }
}