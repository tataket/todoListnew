# todoListnew
1- Entidades (relacionadas/associadas) ao problema <br>
->task ->user <br>
2- Identificar RELACIONAMENTOS das propriedades relacionadas as entidades <br>
task |PROPRIEDADE| <br>
ID   DESCRIÇÃO    USER    COMPLETED    DATE <br>
1      x            -       false      07-11-23 <br>
2      y            -      true        07-11-23 <br>

USER |PROPRIEDADE| <br>
| ID | NAME | AGE |
| --- | --- | --- |
| 1 | Ricardo | velho |
| 2 | Leo | novo |


USERTASK |TABELA DE RELAÇÃO| <br>
ID  USER  TASKS 
1     1     1 
2     2     1 

Temos a relação de: <br>
1x1, que basicamente é 1 para 1, onde user so tem 1 task <br>
1xN, que 1 user pode ter varias tasks <br>
NxN, onde N users pode estar associado a N tasks ou N tasks associado a N users <br>

3- Classes managers para gerir o que fizemos <br>
->userManager <br>
->taskManager <br>
->todoManager <br>
onde consigo associar cada tipo (user/task) <br>
E temos algo como se fosse nosso database <br>
->List<User> <br>
->List<Task> <br>
->List<UserTask>.... que vai gerir todas as outras classes, tem que acessar o user e as tasks <br>

4- Metodos -> os tipos de parametros e o que vai retornar <br>
EX: <br>
taskManager <br>
->createTask(name = String, description = String) = task; <br>
->deleteTask(ID = int) = void; <br>
->update(task=Task) = Task; <br>
->update(description = String, task_ID = int) = task; <br>
->getList() = List<task>; <br>


userManager <br>
->createUser(name = String, ID = int, password = String) = user; <br>
->deleteUser(ID = int) = void; <br>
->getList() = List<User>; <br>


5- Main <br>
-> instanciar dependencias (new) <br>
.-> menu (switch) <br>
.-> pegar input do user (escolha/opção) <br>
.-> chamar metodos de uma dependencia (classes) <br>
.-> tratar retornos (try/catch - sucess/fail) <br>
.estão em um loop (while) <br>
