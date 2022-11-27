node{
    stage('code checkout'){
        git 'https://github.com/Vaibhav3101mankar/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }       
    stage('deploy to tomcat'){
        deploy adapters: [tomcat9(credentialsId: '7fca875c-7593-40c6-9d61-9e23711af097', path: '', url: 'http://54.161.129.168:8085')], contextPath: 'http://54.161.129.168:8085', war: '**/*.war'
   }
}
