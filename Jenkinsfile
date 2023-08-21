pipeline{
    agent any
    stages{
        stage('Source'){
            steps{
                //get sourcec code from git repository
                git 'https://github.com/Siddharth0337/estore_.git'
                //run npm install to install the node modules
                sh "npm install"
                sh "npm audit fix --force"
                echo 'Source Stage Finished'
            }
            
        }
        stage('build'){
            steps{
                //run build command to create dist directory
                sh "npm run build"
                echo 'Build Stage Finished'
            }
        }
    }
}