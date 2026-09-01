### Create first Python application

Put this in `app/main.py`:

```python
def main():
    print("Hello from Python!")
    print("Welcome to AI Engineering.")


if __name__ == "__main__":
    main()
```

Run it:

```bash
python app/main.py
```

You should get:

```text
Hello from Python!
Welcome to AI Engineering.
```

### Important Python concept

This:

```python
if __name__ == "__main__":
    main()
```

means:

> Run `main()` only when this file is executed directly.

This distinction becomes important when we start building larger applications with multiple modules.

---
