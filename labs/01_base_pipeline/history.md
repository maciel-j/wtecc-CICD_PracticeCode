    1  git config --global user.email "jose.s.maciel@outlook.com" && git config --global user.name "maciel-j" && git config --list && git clone https://github.com/maciel-j/wtecc-CICD_PracticeCode.git && cd wtecc-CICD_PracticeCode
    2  cd labs/01_base_pipeline/
    3  export PS1="[\[\033[01;32m\]\u\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
    4  kubectl apply -f tasks.yaml
    5  kubectl apply -f pipeline.yaml
    6  tkn pipeline start --showlog hello-pipeline
    7  kubectl apply -f tasks.yaml
    8  kubectl apply -f pipeline.yaml
    9  tkn pipeline start hello-pipeline     --showlog      -p message="Hello Tekton!"
   10  kubectl apply -f tasks.yaml
   11  kubectl apply -f pipeline.yaml
   12  tkn pipeline start cd-pipeline     --showlog     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch="main"
   13  kubectl apply -f pipeline.yaml
   14  tkn pipeline start cd-pipeline     --showlog     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch="main"
   15  history >> history.md
