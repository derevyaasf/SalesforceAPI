pipeline {
  agent any
  stages {
    stage('Check installations') {
      steps {
        sh '''if which nodejs >/dev/null; then
    nodejs --version

else
sudo apt-get -y install nodejs
  #  node -version
  echo Stage 1-1
fi

if which npm >/dev/null; then
    npm --version
else
    sudo apt-get -y install npm
  
    echo Stage 2-1
fi

if which newman >/dev/null; then
    newman --version
else
   sudo npm install -g newman
    # newman -version
    echo Stage 2
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
