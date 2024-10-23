    1  kubectl port-forward service/el-cd-listener  8090:8080
    2  git config --global user.email "jose.s.maciel@outlook.com" && git config --global user.name "maciel-j" && git config --list && git clone https://github.com/maciel-j/wtecc-CICD_PracticeCode.git && cd wtecc-CICD_PracticeCode
    3  cd labs/02_add_git_trigger/
    4  export PS1="[\[\033[01;32m\]\u\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
    5  kubectl apply -f tasks.yaml
    6  kubectl apply -f pipeline.yaml
    7  tkn task ls
    8  tkn pipeline ls
    9  ls -ahl
   10  ls -ahl /home/project/wtecc-CICD_PracticeCode
   11  kubectl apply -f eventlistener.yaml
   12  tkn eventlistener ls
   13  kubectl apply -f triggerbinding.yaml
   14  kubectl apply -f triggertemplate.yaml
   15  kubectl port-forward service/el-cd-listener  8090:8080
   16  curl -X POST http://localhost:8090   -H 'Content-Type: application/json'   -d '{"ref":"main","repository":{"url":"https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode"}}'
   17  tkn pipelinerun ls
   18  tkn pipelinerun logs --last
   19  history >> history.md && MSG="FEAT: add trigger 2024.10.23" && cd /home/project/wtecc-CICD_PracticeCode && git add . && git commit -m "${MSG}"
   20  git push
   21  git config --list
   22  cd wtecc-CICD_PracticeCode/labs/03_use_tekton_catalog/
   23  export PS1="[\[\033[01;32m\]\u\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
   24  kubectl apply -f tasks.yaml
   25  tkn hub install task git-clone --version 0.8
   26  kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/main/task/git-clone/0.9/git-clone.yaml
   27  kubectl apply -f pvc.yaml
   28  kubectl apply -f pipeline.yaml
   29  tkn pipeline start cd-pipeline     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch="main"     -w name=pipeline-workspace,claimName=pipelinerun-pvc     --showlog
   30  tkn pipelinerun ls
   31  tkn pipelinerun logs --last
   32  history >> history.md && MSG="FEAT: add workspace 2024.10.23" && cd /home/project/wtecc-CICD_PracticeCode && git add . && git commit -m "${MSG}"&& git push
   33  git push
   34  git config --list
   35  cd wtecc-CICD_PracticeCode/labs/04_unit_test_automation/
   36  export PS1="[\[\033[01;32m\]\u\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
   37  kubectl apply -f tasks.yaml
   38  tkn hub install task git-clone
   39  tkn hub reinstall task git-clone
   40  tkn task ls
   41  tkn hub install task flake8]
   42  tkn hub install task flake8
   43  kubectl apply -f pipeline.yaml
   44  tkn pipeline start cd-pipeline     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch="main"     -w name=pipeline-workspace,claimName=pipelinerun-pvc     --showlog
   45  kubectl apply -f tasks.yaml
   46  kubectl apply -f pipeline.yaml
   47  tkn pipeline start cd-pipeline     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch="main"     -w name=pipeline-workspace,claimName=pipelinerun-pvc     --showlog
   48  tkn pipelinerun ls
   49  tkn pipelinerun logs --last
   50  history >> history.md && MSG="FEAT: add test tasks 2024.10.23" && cd /home/project/wtecc-CICD_PracticeCode && git add . && git commit -m "${MSG}"&& git push
