---
layout: posts
title: asyncioのloopメモ 
---

* loop.run_forever() [\*](https://docs.python.org/3.5/library/asyncio-eventloop.html#asyncio.AbstractEventLoop.run_forever)  

* loop.run_until_complete(future) [\*](https://docs.python.org/3.5/library/asyncio-eventloop.html#asyncio.AbstractEventLoop.run_until_complete)  

* loop.close()  

* loop.call_soon(callback, *args) [\*](https://docs.python.org/3.5/library/asyncio-eventloop.html#asyncio.AbstractEventLoop.call_soon)  
指定した関数をイベントループ内で実行する  

* loop.call_later(delay, callback, *args) [\*](https://docs.python.org/3.5/library/asyncio-eventloop.html#asyncio.AbstractEventLoop.call_later)  

* loop.call_at(when, callback, *args) [\*](https://docs.python.org/3.5/library/asyncio-eventloop.html#asyncio.AbstractEventLoop.call_at)  
