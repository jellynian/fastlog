# fastlog
Simple, easy and fast log library for Golang

只有一个文件，可简单引入项目，速度快轻量级.基于官方log库做的二次开发

# 与Golang log库完全兼容,可以直接替换

例子:
    package main

    import (
        log "fastlog"
        "os"
    )

    func main() {
        log.Println("ddddddddddddd")
        log.Printf("%d",22222)
        log.Panic("ddddddddddddddd")
    }


# 例子

    package main

    import (
        log "fastlog"
        "os"
    )

    func main() {
        logger := log.New(os.Stderr, "prefix", log.LstdFlags|log.Ldebug)
        logger.Debug("ddddddddd")
        logger.Debugln("dddddddddddddd")
        logger.Debugf("%d", 2233)
    }
