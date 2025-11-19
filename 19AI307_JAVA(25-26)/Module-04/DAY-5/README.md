# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento design pattern to save, view, and restore different versions of an article’s content.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create the Article class to store and modify content and generate mementos of its state.
4. Implement the ArticleMemento class to hold saved versions of the article content.
5. Create ArticleHistory to store and manage a list of mementos.
6. Each time new content is entered, save the article state as a memento in history.
7. Allow the user to choose a version index and restore that specific saved article content.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}
```



## OUTPUT:
<img width="724" height="200" alt="image" src="https://github.com/user-attachments/assets/060c03a0-6e76-4f82-b8a3-f6c2a5331811" />



## RESULT:
The program successfully saves multiple versions of an article and restores the selected version using the Memento design pattern.
