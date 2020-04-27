# py-nonblocking-input
Simple, cross-platform, pure Python way of reading stdin without blocking

---

#### Pros
- Single file
- Single class
- Single thread
- Documented
- Simple to use
- Typed - as it brings more light to dynamic typed returns
- Cross-platform (anything platform that can run a 2nd thread)
- Pure Python

#### Cons
- Requires setup at start of program (simple)
```python
u = NonBlockingStdIn()
```
- Requires teardown at end of program (simple)
```python
u.kill()
```
- Does not enforce the fact that only a single instance should ever exist
```python
a = NonBlockingStdIn()
b = NonBlockingStdIn()
# This is a journey of pain that leads to multiple threads fighting over stdin using input()
```