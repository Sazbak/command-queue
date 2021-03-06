# Change log

-Command Queue 0.1.3 (2018-12-10)
--------------------------------
- Remove: `CommandQueue(boolean distinctOnly)`.

- Add `CommandQueue.Builder<T>` to configure the created command queue.

- Add `CommandQueue.Builder.distinctOnly()`, which instructs the command queue not to send the event if the new event is content-equal to the previous event.

- Add `CommandQueue.Builder.limit(int)`, which instructs the command queue to drop new events if the queue is already "full".

-Command Queue 0.1.1 (2018-10-03)
--------------------------------
- Fix: Calling `setReceiver(Receiver)` inside a `receiveCommand` block will no longer "freeze" the queue.

-Command Queue 0.1.0 (2018-10-03)
--------------------------------
- Add `setPaused(boolean)` to temporarily freeze the queue even if receiver is available.

-Command Queue 0.0.3 (2018-09-16)
--------------------------------
- Fix possible edge case of a receiver setting a different receiver in the `receiveCommand` block.

- Add sample code.

-Command Queue 0.0.2 (2018-09-16)
--------------------------------
- Add `hasReceiver()`.

- Fix that emitting an event inside the receiver block could be executed in the wrong order.

-Command Queue 0.0.1 (2018-09-13)
--------------------------------
- Initial Release.