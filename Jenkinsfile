node {
  stage('Build') {
     sh "./gradlew setupCIWorkspace"
     sh "./gradlew build"
  }
  stage('Archive artifacts') {
    archiveArtifacts 'build/libs/*.jar'
  }
}
