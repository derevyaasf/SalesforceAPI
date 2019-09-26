pipeline {
  agent any
  stages {
    stage('Check installations') {
      steps {
        sh '''if which node >/dev/null; then
    node -version
else
apt-get --yes --force-yes install nodejs
    node -version
fi

if which newman >/dev/null; then
    newman -version
else
    npm install -g newman
    newman -version
fi
'''
      }
    }
    stage('Test') {
      steps {
        sh '''pwd
'''
      }
    }
  }
}
