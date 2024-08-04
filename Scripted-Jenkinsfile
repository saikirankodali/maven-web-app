node {
    def mvnPath

     environment {
        JAVA_HOME = '/opt/java/openjdk'
    }
    
    stage('git clone') {
        git 'https://github.com/ashokitschool/maven-web-app.git'
    }
    
  stage('Maven build'){
    def mvnHome = tool name:'maven', type:"maven";
    def mvnPath = "${mvnHome}/bin/mvn";
    sh "${mvnPath} --version"
    sh "${mvnPath} clean package"
 }
}
