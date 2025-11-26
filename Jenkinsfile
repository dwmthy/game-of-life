node ('node-01'){
  stage('SCM Checkout'){
    git 'https://github.com/dwmthy/game-of-life'
  }

  stage('Compile - Package'){
    sh 'mvn package'
  }
}
