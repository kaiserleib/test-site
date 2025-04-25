# Todo List

This is a very basic todo list app implemented with pure HTML and JS, directly embedded in markdown.

<div>
  <input id="new-todo" type="text" placeholder="Add a new todo...">
  <button onclick="addTodo()">Add</button>
  <ul id="todo-list"></ul>
</div>

<script>
function addTodo() {
  var input = document.getElementById('new-todo');
  var text = input.value.trim();
  if (!text) return;
  var li = document.createElement('li');
  li.textContent = text;
  li.onclick = function() { this.remove(); };
  document.getElementById('todo-list').appendChild(li);
  input.value = '';
}
</script>

[Back to Home](index.md)
