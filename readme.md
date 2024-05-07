# Tutorial 10

## 1.2: Understanding how it works.

![alt text](images/image.png)

- `Rafif's Computer: hey hey` is printed synchronously from the main thread immediately after the task is spawned.
- `Rafif's Computer: howdy!` is printed from the asynchronously spawned task.
- The program then waits for two seconds due to `TimerFuture::new(Duration::new(2, 0)).await;` inside the asynchronously spawned task.
- After the two-second wait, `Rafif's Computer: done!` is printed. This completes the execution of the asynchronously spawned task.