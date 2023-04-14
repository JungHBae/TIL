
1. sending to child 
```jsx
function App() {
  const [tasks, setTasks] = useState([
    { id: 5271, name: "Record React Lectures", completed: true },
    { id: 7825, name: "Edit React Lectures", completed: false },
    { id: 8391, name: "Watch Lectures", completed: false },
  ]);
  return (
    <div className="App">
      <Header />
      <AddTask tasks={tasks} setTasks={setTasks} />
      <TaskList tasks={tasks} setTasks={setTasks} />
      <Footer />
    </div>
  );
}
```

2. shadow related, hover transitions

```jsx
.shadow {
  box-shadow: 0 2px 4px rgba(0,0,0,0.15),
              0 4px 8px rgba(0,0,0,0.15),
              0 8px 16px rgba(0,0,0,0.15),
              0 16px 32px rgba(0,0,0,0.15);
  transition: all 0.3s ease-in-out;
}

.shadow:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2),
              0 8px 16px rgba(0,0,0,0.2),
              0 16px 32px rgba(0,0,0,0.2),
              0 32px 64px rgba(0,0,0,0.2);
}
```
3. 
