# todoListnew
1- Entidades (relacionadas/associadas) ao problema
->task ->user
2- Identificar RELACIONAMENTOS das propriedades relacionadas as entidades
task |PROPRIEDADE| 
ID   DESCRIÇÃO    USER    COMPLETED    DATE
1      x            -       false      07-11-23
2      y            -      true        07-11-23

USER |PROPRIEDADE|
ID  NAME        AGE 
1   Ricardo     velho
2    Leo        novo

USERTASK |TABELA DE RELAÇÃO|
ID  USER  TASKS
1     1     1 
2     2     1

Temos a relação de:
1x1, que basicamente é 1 para 1, onde user so tem 1 task
1xN, que 1 user pode ter varias tasks
NxN, onde N users pode estar associado a N tasks ou N tasks associado a N users

3- Classes managers para gerir o que fizemos 
->userManager
->taskManager
->todoManager
onde consigo associar cada tipo (user/task)
E temos algo como se fosse nosso database 
->List<User>
->List<Task>
->List<UserTask>.... que vai gerir todas as outras classes, tem que acessar o user e as tasks

4- Metodos -> os tipos de parametros e o que vai retornar
EX:
taskManager
->createTask(name = String, description = String) = task;
->deleteTask(ID = int) = void;
->update(task=Task) = Task;
->update(description = String, task_ID = int) = task;
->getList() = List<task>;


userManager
->createUser(name = String, ID = int, password = String) = user;
->deleteUser(ID = int) = void;
->getList() = List<User>;


5- Main
-> instanciar dependencias (new)
.-> menu (switch)
.-> pegar input do user (escolha/opção)
.-> chamar metodos de uma dependencia (classes)
.-> tratar retornos (try/catch - sucess/fail)
.estão em um loop (while)
