    1  git config --list
    2  git config --global user.email "jose.s.maciel@outlook.com" && git config --global user.name "maciel-j" && git config --list && git clone https://github.com/maciel-j/wtecc-CICD_PracticeCode.git && cd wtecc-CICD_PracticeCode
    3  cd wtecc-CICD_PracticeCode/labs/06_deploy_to_kubernetes/
    4  cd labs/06_deploy_to_kubernetes/
    5  export PS1="[\[\033[01;32m\]\u\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
    6  tkn hub install task git-clone
    7  tkn hub install task flake8
    8  kubectl apply -f tasks.yaml
    9  kubectl apply -f pvc.yaml
   10  tkn task ls
   11  tkn clustertask ls | grep openshift
   12  kubectl apply -f pipeline.yaml
   13  tkn pipeline start cd-pipeline     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch=main     -p app-name=hitcounter     -p build-image=image-registry.openshift-image-registry.svc:5000/$SN_ICR_NAMESPACE/tekton-lab:latest     -w name=pipeline-workspace,claimName=pipelinerun-pvc     --showlog
   14  tkn pipelinerun ls
   15  tkn pipelinerun logs --last
   16  kubectl get all -l app=hitcounter
   17  history >> history.md && MSG="FEAT: add deploy tasks 2024.10.23" && cd /home/project/wtecc-CICD_PracticeCode && git add . && git commit -m "${MSG}"&& git push
