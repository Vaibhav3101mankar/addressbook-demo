node{
    stage('code checkout'){
        git 'https://github.com/Vaibhav3101mankar/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }
    stage('test'){
       junit allowEmptyResults: true, skipPublishingChecks: true, testResults: '**/*.xml'' 
   }
    
    stage('deploy to tomcat'){
        deploy adapters: [tomcat9(credentialsId: 'b5765fa9-28c4-45b9-80cf-2c038c8cf6ad', path: '', url: 'http://18.234.187.20:8085/')], contextPath: 'addressbookpipline', onFailure: false, war: '**/*.war'
    }
}
