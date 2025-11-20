# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use ScheduledExecutorService to delay execution of tasks and print their message.

## AIM:
To schedule user-defined tasks with delays using ScheduledExecutorService and print their messages after the specified time.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read number of tasks and their (message, delay) from the user.
4. Create a ScheduledExecutorService with a thread pool.
5. For each task, schedule it with the given delay using schedule().
6. Store all futures and wait for completion using f.get().
7. Shutdown the scheduler after all tasks finish.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.*;
import java.util.concurrent.*;

public class ScheduledExecutorUserInput {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        ScheduledExecutorService scheduler = Executors.newScheduledThreadPool(n);

        // Store futures to wait for all to finish
        List<ScheduledFuture<?>> futures = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            String line = sc.nextLine().trim();
            String[] parts = line.split(" ");
            String message = parts[0];
            int delay = Integer.parseInt(parts[1]);

            Runnable task = () -> System.out.println(message);

            // schedule tasks based on user delays
            futures.add(scheduler.schedule(task, delay, TimeUnit.SECONDS));
        }

        // Wait for all tasks to complete
        for (ScheduledFuture<?> f : futures) {
            try {
                f.get();  // ensures print order based on actual scheduling
            } catch (Exception e) {
                System.out.println(e.getMessage());
            }
        }

        scheduler.shutdown();
        sc.close();
    }
}
```


## OUTPUT:

<img width="354" height="159" alt="image" src="https://github.com/user-attachments/assets/758355f7-6419-4d87-a7ca-331d4566a884" />



## RESULT:
Messages are printed after their respective delays as scheduled by the executor service.
