
def SONAR_TOKEN = "c892c1b0655e1feacd1ccce04929f2d4f8cdba82"
node("Test-machine-linux"){
@Library('Personal-Jenkins-shared-library') _
    stage('git checkout'){
        scmcheckout{
            branch = 'master'
            url = 'https://github.com/akharaiyi/Sonar-Scann-proj.git'
        }
    }

    stage('build'){
       echo "building the java project"
        sh """
            ls -ltra
           /home/akhigbe/Downloads/sonar-scanner-4.5.0.2216-linux/bin/sonar-scanner -X -Dsonar.login=${SONAR_TOKEN}
           echo "enjoying my first build with shared library in github"
         """.trim()
    }


    stage("upload to nexus"){
     echo "hello world"

}

    stage("SONAR_GATE"){
        // sonar analysis
        
    }



}
// /home/akhigbe/Downloads/sonar-scanner-4.5.0.2216-linux/bin/sonar-scanner




