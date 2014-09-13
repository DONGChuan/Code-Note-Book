# sleep() and wait()

The code sleep(1000); puts thread aside for exactly one second.

The code wait(1000), causes a wait of up to one second. A thread could stop waiting earlier if it receives the notify() or notifyAll() call. The method wait() is defined in the class Object and the method sleep() is defined in the class Thread.
