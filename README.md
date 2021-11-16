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
    // redefinie essa propriedade
    isComplete: !task.isComplete
    } : task // aqui retorna a task se id for diferente
)

setTasks(newTasks)
```

# Fazer deleção em state([]) 
* filter -> filtra e gera um novo array com dados filtrados
* Usando filter pra retornar todos outros items menos o do id atual
```jsx
const filteredTasks = tasks.filter(task => task.id !== id)

setTasks(filteredTasks)
```