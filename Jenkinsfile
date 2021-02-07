
node("CTG-LINUX-NODES"){
@Library('Personal-Jenkins-shared-library') _
    stage('git checkout'){
        scmcheckout{
            branch = 'master'
            url = 'https://github.com/akharaiyi/Sonar-Scann-proj.git'
        }
    }

    stage('check the dir for all file and build')


    stage('build'){
       echo "building the java project"
        sh """
            ls -ltra
           /home/akhigbe/Downloads/sonar-scanner-4.5.0.2216-linux/bin/sonar-scanner
           echo "enjoying my first build with shared library in github"
         """.trim()
    }



}



