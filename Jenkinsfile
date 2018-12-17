node ('master') {
  stage ('initial') {
    echo "${HOSTNAME}"
    echo "${HOME}"
    echo "Hello World" > "${HOME}"/pipeline.tmp
    cat "${HOME}"/pipeline.tmp
    ls -l "${HOME}"/pipeline.tmp
  }
  stage ('cleanup') {
    rm -f "${HOME}"/pipeline.tmp
  }
}
