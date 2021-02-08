
def SONAR_TOKEN = "c892c1b0655e1feacd1ccce04929f2d4f8cdba82"
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
            ${env.SONAR_SCANNER} -X -Dsonar.login=${SONAR_TOKEN}
           echo "enjoying my first build with shared library in github"
         """.trim()
    }


    stage("upload to nexus"){
    echo "upload artifact to nexus repo"
/*
    nexusPublisher nexusInstanceId: 'nexus_server_ctg', nexusRepositoryId: 'maven-releases', packages: [[$class: 'MavenPackage', mavenAssetList: [[classifier: '', extension: '', filePath: '']], mavenCoordinate: [artifactId: 'Helloword', groupId: 'org.ctg', packaging: 'maven-archetype', version: '1.0-SNAPSHOT']]], tagName: 'devop-2020-feb-7'
 */

}



}
// /home/akhigbe/Downloads/sonar-scanner-4.5.0.2216-linux/bin/sonar-scanner




