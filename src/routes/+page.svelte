<script lang="ts">
  type Priority = 'p1' | 'p2' | 'p3';

  type Task = {
    id: number;
    title: string;
    isCompleted: boolean;
    priority?: Priority;
  };

  const tasks: Task[] = [
    { id: 1, title: 'Learn Svelte', isCompleted: false },
    { id: 2, title: 'Learn TypeScript', isCompleted: false },
    { id: 3, title: 'Learn TDD', isCompleted: false },
  ];
</script>

<h1>Tasks</h1>

<ul>
  {#each tasks as task (task.id)}
    <li>{task.title}</li>
  {/each}
</ul>
