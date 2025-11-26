node('node-02') {
    stage('Compile - Package') {
        def mvnTool = tool name: 'maven-3.9.6', type: 'Maven'    
        withEnv(["MAVEN_HOME=${mvnTool}", "PATH+MAVEN=${mvnTool}/bin"]) {
            sh "mvn --version"
        }
    }
}
