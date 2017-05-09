# LT_ET
epoll对文件描述操作有两种默认方式：LT (lever trigger) and ET(edge trigger) . LT模式是epoll_wait检测到socket上有事件发生时，应用程序并不立即处理此事，epoll_wait还会下西再次通知应用程序，直到时间被处理．ET模式下epoll_wait检测到有事件发生时，通知应用程序，应用程序必须立即处理此事，因为后续的epoll_wait条用将不再响应此事，可见，ET模式减少了同一事件被触发的次数，
