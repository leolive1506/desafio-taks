# 💻 Sobre o desafio

- Adicionar uma nova tarefa
- Remover uma tarefa
- Marcar e desmarcar uma tarefa como concluída

# Arquivo com Lógica app
    * TaskList.tsx

# Redefinir um valor a um state
```tsx
const [tasks, setTasks] = useState<Task[]>([]);


const newTasks = tasks.map(
    task => task.id === id ? {
    // herda as outras propriedades
    ...task,
    isComplete: !task.isComplete
    } : task
)

setTasks(newTasks)
```