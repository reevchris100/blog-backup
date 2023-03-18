---
title: "How to Generate and Analyse Java Heap Dump"
seoTitle: "How to generate Heap dump in Java and fix out of memory exception"
seoDescription: "How to generate Heap dump in Java and fix out of memory exception without installation"
datePublished: Sat Mar 18 2023 08:41:34 GMT+0000 (Coordinated Universal Time)
cuid: clfdpzmlv00140alab19y0hbp
slug: how-to-generate-and-analyse-java-heap-dump
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679127283701/af2b8f1d-2729-49ec-b342-13272450f589.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679128831388/e638d299-d3cb-46c1-af30-ca6595993023.jpeg
tags: java, memory, exception, heap, outofmemory

---

### Prerequisites

Install and Setup Java - [How do I install Java?](https://www.java.com/en/download/help/download_options.html)

### Steps

1. Write and execute a simple Java program.
    
    ```java
    
     public class SimpleJavaProgram {
        public static void main(String[] args) {
               List<String> list = null;
               while(true) {
                      list = new ArrayList(); //Memory leak
                      System.out.println(list);
               }
               System.out.println("Done");
        }
    }
    ```
    
2. Go to cmd and execute "jps" to find the JVM ID(vmid) of the running application. JPS stands for **Java Virtual Machine Process Status Tool** and this tool is used to list the JVMs runningn on the system.
    
    ```bash
    jps
    ```
    
3. Now run the "jmap" command to generate the heap dump using the above vmid.JMap stands for Java Memory Map and returns the heap memory details.
    
    ```bash
    jmap -dump:file=heapDump.jmap <vmid>
    ```
    
4. Run "jhat" on the heap dump generated to analyze the heap dump. Jhat stands for Java Heap Analysis Tool. It is used to analyze and monitor the heap dump.
    
    ```bash
    jhat heapDump.jmap
    ```
    
5. Analyze the heap dump from the below links:
    
    [http://localhost:7000/](http://localhost:7000/)
    
    You can also view the objects and instance counts in the histogram.
    
    [http://localhost:7000/histo/](http://localhost:7000/histo/)