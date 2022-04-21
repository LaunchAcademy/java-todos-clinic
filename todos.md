## Create a Todo Application

### Create a Task

- There's a menu item to create a task
- Every task must have a name and a priority
- Name must be between 5 and 255 characters
- Priority must be a number between 1 and 10
- Include appropriate schema constraints and JPA validations

### Add a category name

- We forgot to add a column for the category of each task!
- Create a new migration to add a `category_name` column to the existing `tasks` table.
- This should be a required field and can contain 1 to 255 characters.
- Make sure to update the validations and test it out!

### List Tasks

- List all tasks in the system, ordered by priority in descending order

### Bonus

- Lets normalize the category name!
- Right now we can have duplication in the `category_name` column. Let's instead create a `categories` table that must have a unique name.
- In our migration we will also need to change the `category_name` column to `category_id` as this will be holding a foreign key.
