




---

Chalo, ek simple Flask project banate hain aur isme debug breakpoints lagate hain taaki samajh sakein kaise step-by-step debugging kiya ja sakta hai.

### Simple Project: Todo List API

Yeh project ek simple todo list API banata hai jisme CRUD (Create, Read, Update, Delete) operations honge. Fir is project me hum debugger lagaenge taaki dekhein kis tarah se debugging kaam karti hai.

---

### Step 1: Project Setup

1. Ek folder banao `todo_project`.
2. `todo_project` folder ke andar `app.py` naam ka file banao.
3. Ek virtual environment banao aur Flask install karo:

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Windows me: venv\Scripts\activate
   pip install flask
   ```

---

### Step 2: Write the Code (app.py)

```python
from flask import Flask, jsonify, request

app = Flask(__name__)

# Simple in-memory "database"
todos = []

@app.route('/todos', methods=['GET'])
def get_todos():
    return jsonify(todos)

@app.route('/todos', methods=['POST'])
def add_todo():
    data = request.get_json()
    todo = {"id": len(todos) + 1, "task": data["task"]}
    todos.append(todo)
    return jsonify(todo), 201

@app.route('/todos/<int:todo_id>', methods=['PUT'])
def update_todo(todo_id):
    data = request.get_json()
    for todo in todos:
        if todo["id"] == todo_id:
            todo["task"] = data["task"]
            return jsonify(todo)
    return jsonify({"error": "Todo not found"}), 404

@app.route('/todos/<int:todo_id>', methods=['DELETE'])
def delete_todo(todo_id):
    global todos
    todos = [todo for todo in todos if todo["id"] != todo_id]
    return jsonify({"message": "Todo deleted"}), 204

if __name__ == '__main__':
    app.run(debug=True)
```

---

### Step 3: Run the Flask Application

```bash
flask run
```

---

### Step 4: Set Up Debugger

Agar aap Visual Studio Code ya kisi IDE ka use kar rahe hain, to aap waha pe debugging configure kar sakte hain. Agar aap terminal se debugging karna chahte hain, to Python ka `pdb` module use kar sakte hain.

#### Example: `pdb` Debugging

`pdb.set_trace()` ka use karke hum code ke specific points pe execution ko pause kar sakte hain aur variables aur values ko check kar sakte hain.

Example: `app.py` me debugging lagao:

```python
import pdb
from flask import Flask, jsonify, request

app = Flask(__name__)

todos = []

@app.route('/todos', methods=['GET'])
def get_todos():
    pdb.set_trace()  # Debugger yahan pe start hoga
    return jsonify(todos)

@app.route('/todos', methods=['POST'])
def add_todo():
    data = request.get_json()
    todo = {"id": len(todos) + 1, "task": data["task"]}
    todos.append(todo)
    return jsonify(todo), 201

# ... (rest of the code remains the same)
```

---

### Step 5: Run the Debugger

1. `flask run` command se application ko dobara se start karein.
2. Browser ya API client (e.g., Postman ya curl) ka use karke `/todos` endpoint pe `GET` request bhejein.

    ```bash
    curl http://127.0.0.1:5000/todos
    ```

3. Jab `/todos` endpoint pe request jayegi, to execution `pdb.set_trace()` pe ruk jayegi.

4. Ab aap terminal pe commands use karke variables aur state ko check kar sakte hain. Kuch common commands ye hain:

   - `l`: Current line ke aas-paas ka code dikhata hai.
   - `n`: Next line pe execution ko le jata hai.
   - `p variable_name`: Kisi specific variable ka value print karta hai.
   - `c`: Execution ko continue karta hai till next breakpoint or end of program.

Example:
```bash
> /path/to/app.py(10)get_todos()
-> return jsonify(todos)
(Pdb) p todos
[]
(Pdb) n
(Pdb) c
```

### Step 6: Clean up Debugging Code

Debugger se kaam ho jane ke baad `pdb.set_trace()` ko hata de ya comment kar dein, taki production code clean aur performant rahe.

---

### Debugging Summary

- **pdb.set_trace()** ka use debugging start karne ke liye hota hai.
- Breakpoints pe ruk ke aap variables ka value aur code ka flow dekh sakte hain.
- `p` command se variable values inspect kar sakte hain, aur `c` command se execution continue kar sakte hain.


---
![image](https://github.com/user-attachments/assets/f45c2eec-ffa5-4eb6-a41c-d496a5a28ba2)


![image](https://github.com/user-attachments/assets/384d0251-5bf7-48f8-8235-c1b143b11552)

---
