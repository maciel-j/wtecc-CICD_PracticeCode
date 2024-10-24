    1  git config --list
    2  git config --global user.email "jose.s.maciel@outlook.com" && git config --global user.name "maciel-j" && git config --list && git clone https://github.com/maciel-j/wtecc-CICD_PracticeCode.git && cd wtecc-CICD_PracticeCode
    3  export PS1="[\[\033[01;32m\]\h\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
    4  tkn hub install task git-clone
    5  cd wtecc-CICD_PracticeCode/labs/05_build_an_image/
    6  cd 05_build_an_image/
    7  cd lab/05_build_an_image/
    8  cd labs/05_build_an_image/
    9  tkn hub install task flake8
   10  kubectl apply -f tasks.yaml
   11  tkn task ls
   12  tkn clustertask ls
   13  pwd
   14  kubectl apply -f pipeline.yaml
   15  kubectl apply -f pvc.yaml
   16  tkn pipeline start cd-pipeline     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch=main     -p build-image=image-registry.openshift-image-registry.svc:5000/$SN_ICR_NAMESPACE/tekton-lab:latest     -w name=pipeline-workspace,claimName=pipelinerun-pvc     --showlog
   17  tkn pipelinerun ls
   18  tkn pipelinerun logs --last
   19  history >> history.md && MSG="FEAT: add build tasks 2024.10.23" && cd /home/project/wtecc-CICD_PracticeCode && git add . && git commit -m "${MSG}"&& git push
