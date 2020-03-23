node {
   
    def customImage
    
    environment {
        DOCKER_CERT_PATH = '/certs/client/xxx'
        DOCKER_TLS_VERIFY = 1
    }
    
    stage ('Checkout'){
        checkout scm
    }/*
    stage ('Build'){
        
        sh 'echo Starting build of odoo'
        customImage = docker.build("jhg_odoo:${env.BUILD_ID}","./Odoo")
    }*/
    stage ('Deploy') {
        
        sh 'echo Deploying Env'
        sh 'docker-compose up -d --build'    
    }
    
    stage ('Configure') {
      
    }
}
