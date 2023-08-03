<template>
  <div class="tasks-container">
    <form>
      <input type="text" class="text-container" />
      <button class="create-button">Criar</button>
    </form>
    <section>
      <div class="task-count">
        <h3>Tarefas criadas<span>0</span></h3>

        <h3>Concluídas<span>0 de 0</span></h3>
      </div>
      <div>
        <!-- UTILIZAR O CÓDIGO ABAIXO QUANDO NÃO TIVER NENHUMA TAREFA CRIADA -->
        <!-- <div class="empty-container"> 
          <p>
            <span>Você ainda não tem tarefas cadastradas</span>
            Crie tarefas e organize seus itens a fazer
          </p>
        </div> -->
        <TaskView />
        <TaskView />
        <TaskView />
        <TaskView />
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import TaskView from '../components/TaskView.vue'

export default {
  name: 'CreateTaskView',
  components: { TaskView }
}
</script>

<style scoped>
.tasks-container form {
  display: flex;
  align-items: center;
  gap: 8px;
}

.tasks-container .text-container {
  width: 90%;
  height: 5.4rem;

  padding: 1.6rem;

  background-color: var(--gray-500);
  border: 1px solid var(--gray-700);
  border-radius: 8px;

  color: var(--gray-200);
  font-size: 1.6rem;
}

.tasks-container .create-button {
  width: 9rem;
  height: 5.2rem;

  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;

  padding: 1.6rem;

  background: var(--blue-dark);
  border: none;
  border-radius: 8px;

  font-weight: 700;
  font-size: 1.4rem;

  color: var(--gray-100);

  cursor: pointer;
  transition: background 0.1s;
}

.tasks-container .create-button:not(:disabled):hover {
  background: var(--blue);
}

.tasks-container .create-button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.tasks-container section {
  width: 100%;

  margin-top: 6.4rem;
}

.tasks-container section .task-count {
  display: flex;
  align-items: center;
  justify-content: space-between;

  margin-bottom: 2.4rem;
}

.tasks-container section .task-count h3 {
  font-weight: 700;
  font-size: 1.4rem;
}

.tasks-container section .task-count h3:first-child {
  color: var(--blue);
}

.tasks-container section .task-count h3:last-child {
  color: var(--purple);
}

.tasks-container section .task-count h3 span {
  margin-left: 0.8rem;
  padding: 0.2rem 0.8rem;

  background: var(--gray-400);

  font-size: 1.4rem;
  color: var(--gray-200);

  border-radius: 999px;
}

.tasks-container section .empty-container {
  display: flex;
  align-items: center;
  flex-direction: column;

  padding-block: 6.4rem;

  border-top: 1px solid var(--gray-400);
  border-radius: 8px;
}

.tasks-container section .empty-container p {
  color: var(--gray-300);
  margin-top: 1.6rem;

  text-align: center;
}

.tasks-container section .empty-container p span {
  display: block;
  font-weight: 700;
}
</style>
