---
title: "Process what ?"
datePublished: Tue Jan 27 2026 16:50:57 GMT+0000 (Coordinated Universal Time)
cuid: cmkwu20qj000802jufnre7htf
slug: process-what

---

you've heard these terms processes, tasks, cores, threads, parallelism, concurrency, sync and async, often some of them with multi- prefix.  interrelated names and definition depending on the context. 

these are eluded me for a long time and still does, and might continue to do so,
I have actually started writing this to give meaning in detailed description, someday I will but till then I want you to explore this forest on your own. 

but hey wait, let me give you a torchlight before you begin this journey.

we find it difficult to look at these terms and make sense because we often look from one perspective. ~and that does not help.~

```python3
import os
from psutil import Process as p

me                 = p(os.getpid())          
me_mama            = p(me.ppid())            
me_grama           = p(me_mama.ppid())      
me_grama_mama      = p(me_grama.ppid())    
me_grama_mama_mama = p(me_grama_mama.ppid())

print(
me,                 
me_mama, 
me_grama,            
me_grama_mama, 
me_grama_mama_mama,

sep="\n"
)
```

```shell
psutil.Process(pid=308, name='python3', status='running')
psutil.Process(pid=12, name='zsh', status='sleeping')
psutil.Process(pid=11, name='Relay(12)', status='running')
psutil.Process(pid=10, name='SessionLeader', status='sleeping')
psutil.Process(pid=1, name='init(Ubuntu)', status='sleeping')
```


