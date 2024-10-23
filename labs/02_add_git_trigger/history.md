    1  git config --global user.email "jose.s.maciel@outlook.com" && git config --global user.name "maciel-j" && git config --list && git clone https://github.com/maciel-j/wtecc-CICD_PracticeCode.git && cd wtecc-CICD_PracticeCode
    2  cd labs/02_add_git_trigger/
    3  export PS1="[\[\033[01;32m\]\u\[\033[00m\]: \[\033[01;34m\]\W\[\033[00m\]]\$ "
    4  kubectl apply -f tasks.yaml
    5  kubectl apply -f pipeline.yaml
    6  tkn task ls
    7  tkn pipeline ls
    8  ls -ahl
    9  ls -ahl /home/project/wtecc-CICD_PracticeCode
   10  kubectl apply -f eventlistener.yaml
   11  tkn eventlistener ls
   12  kubectl apply -f triggerbinding.yaml
   13  kubectl apply -f triggertemplate.yaml
   14  kubectl port-forward service/el-cd-listener  8090:8080
   15  curl -X POST http://localhost:8090   -H 'Content-Type: application/json'   -d '{"ref":"main","repository":{"url":"https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode"}}'
   16  tkn pipelinerun ls
   17  tkn pipelinerun logs --last
   18  history >> history.md && MSG="FEAT: add trigger 2024.10.23" && cd /home/project/wtecc-CICD_PracticeCode && git add . && git commit -m "${MSG}"
