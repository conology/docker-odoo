node {
   
    def customImage
    
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
    /*
    stage ('Configure') {
      
    }*/
}
