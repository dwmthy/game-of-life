node('node-02') {
  stage('SCM Checkout') {
    git 'https://github.com/dwmthy/game-of-life.git'
  }

  stage('Compile - Package') {
    def mvnTool = tool name: 'maven-3.9.6', type: 'Maven'    
    withEnv(["MAVEN_HOME=${mvnTool}", "PATH+MAVEN=${mvnTool}/bin"]) {
      sh 'echo $MAVEN_HOME' // Debug: Check if MAVEN_HOME is correctly set
      sh 'echo $PATH'       // Debug: Check if the Maven bin directory is in PATH
      sh 'mvn package'      // Run Maven build
    }
  }
}
