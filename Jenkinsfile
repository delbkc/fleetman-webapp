node {
   stage('Preparation') { 
      git 'https://github.com/delbkc/fleetman-webapp'
   }
   stage('Build') {
     sh "mvn package"
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
