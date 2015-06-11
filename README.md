##This is the final project for NYU course Web Search Engine (CSCI-GA 2580-001 2014 Fall)
-------------------------------------------
By :  [Fei Guan](https://github.com/FeiGuan),   [Jingxin Zhu](https://github.com/jz1371),    [Wuping Lei](https://github.com/Ryanray13)

#Features: 
#####1.1 knowledge bar
![demo1](/img/demo1.gif?raw=true "demo1")




#####1.2 spelling checking based on Pseudo-Relevance-Feedback (PRF)
![demo2](/img/demo2.gif?raw=true "demo2")


*(**web seach** -> **web search**, instead of -> **web reach**, after adding (PRF))*



#####1.3 snippet and local cache
![snippet](/img/snippet.png?raw=true "demo3")


#Framework design:
![design](/img/design.png?raw=true "demo4")

#Usage
Part 1: Compile and run:
Change in the parent directory of src first and then, 
3.1 To compile,
  ```bash
  $ javac [-encoding utf8] -cp jsoup.jar src/edu/nyu/cs/cs2580/*.java
 ```
3.2.1 Run mining mode :
```bash
  $ java -cp jsoup.jar:src edu/nyu/cs/cs2580/SearchEngine --mode=mining --options=conf/engine.conf
```
3.2.2 Run index mode:
```bash
  $ java -cp jsoup.jar:src edu/nyu/cs/cs2580/SearchEngine --mode=index --options=conf/engine.conf
 ```
3.2.3 Run server mode:

```bash
  $ java -cp jsoup.jar:src edu/nyu/cs/cs2580/SearchEngine --mode=serve --port=25801 --options=conf/engine.conf
  ```
3.2.4 Run front-end server:

  install node.js first

#FrontEnd:
Repositories contain front end code which runs  on node.js, you need to install node.js and under directory of /frontend
```bash
  $ sudo npm install
  
  $ bower install
  ```
Once all library has been installed, go to frontend directory and run: 
```bash
  $ cd frontend/
  $ node app.js
  ```
Then go to browser enter localhost:3000.

For Your Infomation:
The project contains some file with utf-8 encoding character, you may need to add -encoding utf8 to compile.
Different system may require different delimiter between classpath you may need to change from ":" to ";"
The word being searched is stemmed, and stopwords will be filtered, if you want word to as it is, double
quote that single word.
     
Intro：
On one hand, when searching a question in computer programming, people are usually expecting to see
a highly recommended answer and save the time clicking each results search engine returns. 
On the other hand, platforms such as Stack Overflow have accumulated a huge amount of valuable answers
on a wide range of topics in computer programming[1]. So, our team will try to leverage those answers 
to provide a knowledge bar for programming questions.
In this project, our team also takes efforts to check users’ spelling mistake and 
provide suggestion query for possible mistake in the light of Pseduo-Relevance-Feedback.

