1. Define CRUD.
The four basic types of functionality that we want our APIs to have. We want them to be able to create, read, update, and delete resources.

2. Why do we use set method_override: true?
It allows us to use delete and put methods from our controller in the form in our erb files. Normally html forms only recognize get and post methods. Using a hidden input with name _method, we change the post method to a delete or put. 
 
3. Explain the difference between value and name in this line: `<input type='text' name='task[title]' value="<%= @task.title %>"/>.`
The name is what the submitted input will be assigned to. The value will be accessed by key :title contained in the hash returned by :task in the params hash returned when the form is submitted.
The value is what is going to appear in the text box when the page loads which in this case is the current value. 

4. What are params? Where do they come from?
When you submit a form, all of the input names are put into a hash called params as keys. The values of these keys are whatever was entered for that specific input. You can use the params hash in your controller to access the input key values. 

5. Check out your routes. Why do we need two routes each for creating a new Task and editing an existing Task?
For creating a new task you need a route where you put the input for creating the new task. You also need a route to send that new task information to. 
For editing a task you need to put in the new edit information on one path and then send the new edited information to another path. 
