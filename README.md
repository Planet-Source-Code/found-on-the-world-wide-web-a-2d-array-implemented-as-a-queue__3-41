<div align="center">

## A 2D Array Implemented as a Queue


</div>

### Description

2D Array Implemented as a Queue. http://users.neca.com/jboxall/ja05007.htm
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Found on the World Wide Web](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/found-on-the-world-wide-web.md)
**Level**          |Unknown
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Data Structures](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/data-structures__3-8.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/found-on-the-world-wide-web-a-2d-array-implemented-as-a-queue__3-41/archive/master.zip)





### Source Code

```
/* Jason Boxall 1/21/96 CSC 131 Lab #9           */
/* This program uses a 2D array and implements it as a queue */
#include <stdio.h>
#include <string.h>
void enqueue(char [][15],int);
void dequeue(char [][15],int);
void display(char [][15],int);
void main()
{
 char names[10][15]={"Ed Brown","Ann Smith","Sue Jones"};
 int count=3;
 puts("The original queue is as follows:");
 display(names,count);
 puts("After dequeuing, the queue is as follows:");
 dequeue(names,--count);
 display(names,count);
 enqueue(names,++count);
 puts("After enqueuing, the queue is as follows:");
 display(names,count);
}
void display(char n[][15],int count)
{
  int i;
  for(i=0;i<count;++i)
   printf("%s\n",(n+i));
  puts("");
}
void enqueue(char n[][15],int count)
{
 puts("Enter a name:");
 gets(n[count-1]);
 puts("");
}
void dequeue(char m[][15],int count)
{
 int i;
 for(i=0;i<=count;++i)
  strcpy(m[i],m[i+1]);
}
```

