node ('master') {
  stage ('initial') {
    echo "${HOSTNAME}"
    echo "${HOME}"
    echo "Hello World" > pipeline.tmp
    cat pipeline.tmp
  }
  stage ('cleanup') {
    rm -f pipeline.tmp
  }
}
