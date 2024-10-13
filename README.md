# Fullstack Developer Take-Home Challenge

## Overview

Thank you for your interest in the Fullstack Developer position at Wink, Inc. This take-home challenge is designed to assess your proficiency in frontend development using Svelte and TypeScript, as well as your ability to handle form data submission and validation.

## Front-end Challenge

You are tasked with enhancing a provided SvelteKit application that includes a form for creating or adding a member to a company account. The application already includes basic components and structure. Your goal is to implement the specified challenges and bonus tasks to demonstrate your skills.

1. **BoxedRadio Component Interaction**
   - **Objective:** Ensure that the `BoxedRadio` component correctly reflects the selected state.
   - **Details:** When a user selects a radio button, the component should update its state accordingly and reflect the selected option is highlighted correctly.

2. **Render Existing Company Dropdown**
   - **Objective:** Dynamically adjust form fields based on the selected account type.
   - **Details:** 
     - **Agent Account Type:**
       - If "Agent" is selected as the account type, hide the "New Company" and "Existing Company" options.
       - The Company Information section becomes optional, and it won't matter if the user belongs to a new or existing company.
     - **Other Account Types (Corporate & Application Service):**
       - If the user selects "Existing Company" in the account creation type, a dropdown should appear in the Company Information section, allowing selection from a predefined list of existing companies.
       - When "Existing Company" is selected, hide the address fields and only display the dropdown.
       - Refer to the Figma design for visual guidance on this scenario.
   - **Implementation Hint:** Utilize the provided `data.json` file to simulate data from database.

3. **Form Submission and Data Handling**
   - **Objective:** Implement form submission functionality that collects all input data and displays the results on a different page or route.
   - **Details:** Upon clicking the submit button, validate and gather all form data into a JSON object, then navigate to a new route (e.g., `/member-account`) that presents the submitted information in a user-friendly format.

### Front-end Bonus Tasks

- **Form Validation**
  - **Member:**
    - First Name, Last Name, and Email is required.
    - Email must be a valid email address.
  - **Company Name:**
    - Required field if the account type is "Corporate" or "Application Service".
  - **Phone Number:**
    - Must be a valid phone number format.
  - **Zip Code:**
    - Must be a valid zip code format.
  - **UI Enhancements:**
    - Add an asterisk (*) next to all required fields to indicate their necessity.
    - Utilize Bootstrap's built-in error components to display validation messages as per the Figma design.

- **Subscription/Billing Section**
  - **Design Integration:**
    - Add a subscription and billing section based on the provided designs included in the '`/design` folder.
  - **Component Creation:**
    - Create reusable components for this section.
  - **Styling:**
    - Utilize theme colors for backgrounds and text using the existing CSS variables in the `scss` folder. Take advantage of any utility helper classes you can find. 
    - Ensure the section is responsive across different device sizes.
  - **Account Type Specific Subscriptions:**
    - For the "Agent" Account Type, only the "AnnuitySpecs" and "LifeSpecs" subscriptions are available.
    - Hide the other two subscription options from the form.
    - An example of this scenario can be found in the Figma design.

---

### Getting Started:

1. **Extract the Zip File:**
   - After downloading the provided zip file, extract it. Inside, you will find two main folders: 
     - `design/` — This contains the Figma design files and image assets.
     - `code/` — This contains the project repository.

2. **Figma Design Files:**
   - You can either:
     - **Import the .fig file into your Figma account:**
       1. Open your Figma Drafts file browser.
       2. Drag and drop the file into the file browser or editor. Once the file is uploaded, click “Done” on the file importer modal box.
     - **View the image assets:** If you prefer not to use Figma, you can simply refer to the image files in the `design/` folder.

3. **Upload the repository to your GitHub account**:
   - Create a new repository on your personal GitHub account.
   - Initialize the repository locally by running the following commands inside the project directory (replace `<repository-url>` with the URL of your GitHub repository):
     ```bash
     git init
     git remote add origin <repository-url>
     git add .
     git commit -m "Initial commit"
     git push -u origin main
     ```

4. **Create a feature branch**: After pushing the initial commit, create a feature branch where you will work on the challenge:
   ```bash
   git checkout -b feature/challenge-solution
   ```

5. **Install dependencies**: Navigate into the project directory and run the following command to install the necessary packages:
   ```bash
   npm install
   ```

6. **Development server**: Once dependencies are installed, start the development server with:
   ```bash
   npm run dev
   ```

   This will spin up a local server that you can access at `http://localhost:5173`.

### Libraries and Tools

You are free to install any libraries that can aid you in completing this challenge, especially for form validation and handling complex form logic. We recommend considering the following:

- **[Zod](https://github.com/colinhacks/zod):** A TypeScript-first schema declaration and validation library.
- **[SuperForms](https://github.com/ghosh/ui):** A form library for Svelte that simplifies form handling and validation.

## SQL Skills Challenge

This challenge is designed to assess your SQL skills. You will be working with a sample database schema defined in the `mysql-schema.sql` file. The challenge consists of three steps: easy, moderate, and difficult. Each step requires you to create a SQL statement based on the example database schema.

1. **Easy:**
   - **Objective:** Retrieve a list of all employees along with their department names.
   - **Instructions:**
     - Write a SQL query to fetch the first name, last name, and department name of all employees.
     - If an employee does not belong to any department, the department name should be `NULL`.

2. **Moderate:**
   - **Objective:** Calculate the total budget for all projects managed by each department.
   - **Instructions:**
     - Write a SQL query to fetch the department name and the total budget of all projects managed by that department.
     - The result should include departments even if they do not manage any projects, with the total budget being `0` in such cases.

3. **Difficult**
   - **Objective:** Find the top 3 highest-paid employees who are working on at least one project.
   - **Instructions:**
     - Write a SQL query to fetch the first name, last name, and salary of the top 3 highest-paid employees who are assigned to at least one project.
      - The result should be ordered by salary in descending order.

---

### Setting Up MySQL Locally

To complete the SQL Skills Challenge, you need to set up a local MySQL server. Follow these steps to install MySQL using Homebrew, apply the schema, and execute the insert statements.

1. **Install Homebrew**
   - If you don't have Homebrew installed, you can install it by running the following command in your terminal:

      ```sh
      /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
      ```
    - Once Homebrew is installed, make sure it's up to date:
  
      ```sh
      brew update
      ```

2. **Install MySQL:** Once Homebrew is installed and updated, you can install MySQL by running:

      ```sh
      brew install mysql
      ```

3. **Start MySQL Server:** After installing MySQL, start the MySQL server with:

      ```sh
      brew services start mysql
      ```

4. **Secure MySQL Installation:**
    - Run the following command to secure your MySQL installation:

      ```sh
      mysql_secure_installation
      ```
    - Follow the prompts to set up your root password and secure your MySQL installation. This command will guide you through securing your MySQL installation by setting a root password, removing anonymous users, disallowing remote root login, and removing test databases.

5. **Connect to MySQL:**

   - Log in to your MySQL server using the root user:

      ```sh
      mysql -u root -p
      ```
   - Enter the root password you set during the secure installation process.

6. **Create and Use the `company_db` Database:** Once connected to MySQL, create and use the `company_db`:

    ```sh
    CREATE DATABASE company_db;
    USE company_db;
    ```

7. **Apply the Schema:** 
    - To apply the schema from your SQL file, save the schema (which includes the table creation and data insertion statements) into a file, for example mysql-schema.sql. Then, from the terminal (outside of MySQL), run:

      ```sh
      mysql -u root -p company_db < /path/to/mysql-schema.sql
      ```
    - Make sure to replace /path/to/mysql-schema.sql with the actual file path where you saved the schema.

8. **Verify the Setup:**

    - You can verify that the schema and data have been applied correctly by logging into MySQL and running some basic queries:

      ```sh
      USE company_db;
      SHOW TABLES;
      ```
    - You should see the `employees`, `departments`, `projects`, and `employee_projects` tables listed.

9. **Execute the SQL Challenge:**
    - Now that your MySQL server is set up and the schema and data are in place, you can proceed with the SQL Skills Challenge. Refer to the challenge instructions in the previous section to complete the tasks.

    - For each challenge, create a SQL file with your solution and place it in the `src/lib/server/db` folder. Name the files as follows:

      - `easy-challenge.sql` for the easy challenge
      - `moderate-challenge.sql` for the moderate challenge
      - `difficult-challenge.sql` for the difficult challenge

## Submission Guidelines:

1. **Complete your work on a feature branch**: Make sure all your work is done on the `feature/challenge-solution` branch, which you created in the **Getting Started** section.

2. **Open a pull request**: After pushing your changes, create a pull request (PR) on your own repository from the `feature/challenge-solution` branch into the `main` branch.

3. **Submit the PR link**: Send us the link to the pull request. We will review the code diff and your implementation directly from the PR.

4. **Optional improvements**: Feel free to implement any additional features or enhancements that you think would improve the project. Anything extra you add will help showcase your skills and creativity.

## Time Expectations

You should aim to complete this challenge within **1-2 weeks**. If you require more time, please reach out, and we can provide an extension if needed. If you are not familiar with Svelte, you may attempt the challenge using a JavaScript framework of your choice while following the Figma design guidelines.

## Resources

- **Svelte Documentation:** [https://svelte.dev/docs](https://svelte.dev/docs)
- **SvelteKit Documentation:** [https://kit.svelte.dev/docs](https://kit.svelte.dev/docs)
- **TypeScript Documentation:** [https://www.typescriptlang.org/docs/](https://www.typescriptlang.org/docs/)
- **SvelteStrap Documentation:** [https://sveltestrap.js.org/](https://sveltestrap.js.org/)
- **Bootstrap Documentation:** [https://getbootstrap.com/docs/5.3/getting-started/introduction/](https://getbootstrap.com/docs/5.3/getting-started/introduction/)
- **Figma Learn:** [https://help.figma.com/](https://help.figma.com/hc/en-us/articles/360041003114-Import-files-to-the-file-browser)
- **Homebrew Documentation:** [https://brew.sh](https://brew.sh)
- **MySQL Secure Installation Guide:** [https://dev.mysql.com/doc/refman/8.0/en/mysql-secure-installation.html](https://dev.mysql.com/doc/refman/8.0/en/mysql-secure-installation.html)
- **MySQL Documentation:** [https://dev.mysql.com/doc/](https://dev.mysql.com/doc/)
- **Homebrew Services:** [https://github.com/Homebrew/homebrew-services](https://github.com/Homebrew/homebrew-services)

## Questions?

If you have any questions or need further clarification, feel free to reach out to [vince@winkintel.com](vince@winkintel.com) and [daniele@winkintel.com](daniele@winkintel.com).
#   w i n k e - e h  
 