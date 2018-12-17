node ('master') {
  stage ('initial') {
    echo "${HOSTNAME}"
    echo "${HOME}"
    echo "Hello World" > ~/pipeline.tmp
    cat ~/pipeline.tmp
    ls -l ~/pipeline.tmp
  }
  stage ('cleanup') {
    rm -f ~/pipeline.tmp
  }
}
