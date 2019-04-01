* Dispatch
  * [raywenderlich, Part 1/2](https://www.raywenderlich.com/5370-grand-central-dispatch-tutorial-for-swift-4-part-1-2)
  * [raywenderlich, Part 2/2](https://www.raywenderlich.com/5370-grand-central-dispatch-tutorial-for-swift-4-part-1-2)
  * [DispatchQueue](https://developer.apple.com/documentation/dispatch/dispatchqueue)
    * Dispatch queues are FIFO queues to which your application can submit tasks in the form of block objects. Dispatch queues execute tasks either serially or concurrently. Work submitted to dispatch queues executes on a pool of threads managed by the system.
    * You schedule work items synchronously or asynchronously. When you schedule a work item synchronously, your code waits until that item finishes execution. When you schedule a work item asynchronously, your code continues executing while the work item runs elsewhere.
  * [DispatchWorkItem](https://developer.apple.com/documentation/dispatch/dispatchworkitem)
    * cancel()
  * [DispatchGroup](https://developer.apple.com/documentation/dispatch/dispatchgroup)
    * enter(), leave()
    * wait(), wait(timeout: DispatchTime)
    * notify(queue:work:)
  * GCD: Grand Central Dispatch
  * QoSClass
    * userInteractive
    * userInitiated
    * `default`
    * utility
    * background
    * unspecified
  * Thread-Safe Arrays, w/ utilizing DispatchQueue
    * https://basememara.com/creating-thread-safe-arrays-in-swift/
    * async: write
    * sync: read

* Dispatch, ObjC
  * [dispatch_async](https://developer.apple.com/documentation/dispatch/1453057-dispatch_async?language=objc), async, returns immediately
  * dispatch_sync, do not call on the same queue
  * [dispatch_get_main_queue](https://developer.apple.com/documentation/dispatch/1452921-dispatch_get_main_queue?language=objc)
  * [dispatch_get_global_queue](https://developer.apple.com/documentation/dispatch/1452927-dispatch_get_global_queue?language=objc), high, default, low, background

```objective-c
    dispatch_async(dispatch_get_main_queue(), ^{
    });
    dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
    });
```

* Dispatch, Swift

```swift
DispatchQueue.global(qos: .userInitiated).async { [weak self] in
  // ..

  DispatchQueue.main.async { [weak self] in
  }
}

DispatchQueue.main.asyncAfter(deadline: .now() + 5.0) { [weak self] in
}

```

* NSOperationQueue
  * [NSOperationQueue]()
    * addOperation
    * maxConcurrentOperationCount
  * [NSBlockOperation](https://developer.apple.com/documentation/foundation/nsblockoperation?language=objc) / NSOperation
    * cancel
    * addDependency, removeDependency

* @synchronized() {}

* dispatch_semaphore_t
  * dispatch_semaphore_create(..)
  * dispatch_semaphore_wait(.. , ..)
  * dispatch_semaphore_signal(..)

* retain cycles

```objective-c
// cycle
    [obj theMethod:^{
        [obj doSomething];
    }];
// using __weak
    __weak typeof(self) weakSelf = self;
    [self theMethod:^{
        __strong typeof(self) strongSelf = weakSelf;
        if (strongSelf) {
            [strongSelf doSomething];
        } else {
            // ..
        }
    }];
```
