# getty #
---
 *a netty like asynchronous network I/O library*

## introdction ##
---
> DESC       : a asynchronous network I/O library in golang   
  LICENCE    : Apache License 2.0   

## develop history ##
---

- 2016/08/25
	> move close done to once clause in server.go:(Server)stop   
	>
	> rename reqQ to rQ which means read queue and its relative params   
	>
	> rename rspQ to wQ which means write queue and its relative params   
	>
	> version: 0.2.06   

- 2016/08/24
	> delete session.go:Session:wg(atomic.WaitGroup). Add session.go:Session:grNum instead to prevent from  (Session)Close() block on session.go:Session:wg.Wait()   
	>
	> add once for session.go:Session:done(chan struct{})   
	>
	> version: 0.2.05   

- 2016/08/23
	> do not consider empty package as a error in (Session)handlePackage   
	>
	> version: 0.2.04   

- 2016/08/22
	> rename (Session)OnIdle to (Session)OnCron   
	>
	> rewrite server.go: add Server{done, wg}   
	>
	> add utils.go   
	>
	> version: 0.2.03   

- 2016/08/21
	> add name for Session   
	>
	> add OnError for Codec   

- 2016/08/18
	> delete last clause of handleRead   
	>
	> add reqQ handle case in last clause of handleLoop   
	>
	> add conditon check in (*Session)RunEventLoop()   
	>
	> version: 0.2.02   

- 2016/08/16
	> rename all structs   
	> add getty connection   
	> rewrite (Session)handleRead & (Session)handleEventLoop   
	> version: 0.2.01   
