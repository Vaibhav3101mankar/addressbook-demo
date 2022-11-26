node{
    stage('code checkout'){
        git 'https://github.com/Vaibhav3101mankar/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }
    stage('test'){
       junit skipMarkingBuildUnstable: true, skipOldReports: true, testResults: '**/*.xml' 
   }
    
    stage('deploy to tomcat'){
        deploy adapters: [tomcat9(credentialsId: '7fca875c-7593-40c6-9d61-9e23711af097', path: '', url: 'http://18.208.183.122:8085/')], contextPath: 'AddressebookPipline', war: '**/*.war'
   }
}
