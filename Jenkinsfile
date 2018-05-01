node {
  stage('Preparation') {
    git url: 'https://github.com/fspijkerman/refinedstorage.git', branch: 'jenkins'
  }
  stage('Build') {
     sh "./gradlew setupCIWorkspace"
     sh "./gradlew build"
  }
  stage('Archive artifacts') {
    archiveArtifacts 'build/libs/*.jar'
  }
}
