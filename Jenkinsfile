
node("Test-machine-linux"){
@Library('Personal-Jenkins-shared-library') _
        stage('git checkout'){
            scmcheckout{
                branch = 'master'
                url = 'https://github.com/akharaiyi/Sonar-Scann-proj.git'
            }
        }

        stage('check the dir for all file and build'){
            echo "ls -R"
        }


        stage('build'){
           echo "building the java project"
            sh """
                ls -ltra
                ${env.SONAR_SCANNER} -X
               echo "enjoying my first build with shared library in github"
             """.trim()
        }


        stage("upload to nexus"){
            echo "happy code and enage in devops lol...."

      }



}




