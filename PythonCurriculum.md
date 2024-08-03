# Detailed Full-Stack Python Curriculum

## I. Git and GitHub

### 1. Introduction to Version Control
- What is version control?
  - Definition and importance
  - History of version control systems
- Centralized vs. Distributed version control systems
  - Comparison and use cases
- Benefits of using version control in software development
  - Collaboration improvements
  - Code history and versioning
  - Branching and merging capabilities

### 2. Git Basics
- Installing Git
  - Installation on Windows, macOS, and Linux
  - Verifying installation
- Configuring Git
  - Setting up user name and email
  - Configuring default editor
- Initializing a repository
  - Understanding the .git directory
  - Creating a new repository (git init)
- The three states of Git
  - Working directory
  - Staging area (Index)
  - Git directory (Repository)

### 3. Basic Git Commands
- git init
  - Starting a new repository
- git add
  - Staging specific files
  - Staging all files (git add .)
  - Understanding the staging area
- git commit
  - Creating commits
  - Writing meaningful commit messages
  - Amending commits
- git status
  - Checking repository status
  - Understanding file states
- git log
  - Viewing commit history
  - Customizing log output
- git diff
  - Comparing working directory to staging area
  - Comparing staging area to last commit

### 4. Branching and Merging
- Creating branches
  - git branch command
  - Naming conventions for branches
- Switching branches
  - git checkout command
  - git switch command (Git 2.23+)
- Creating and switching branches
  - git checkout -b shortcut
- Merging branches
  - Fast-forward merges
  - Three-way merges
- Resolving merge conflicts
  - Understanding conflict markers
  - Manual conflict resolution
  - Using merge tools
- Practical Scenarios
  - Branching strategies (Gitflow, feature branching)
  - Common workflows (pull requests, code reviews)

### 5. Remote Repositories and GitHub
- Introduction to GitHub
  - What is GitHub?
  - GitHub features overview
- Creating a GitHub account and repository
  - Setting up SSH keys
  - Creating a new repository on GitHub
- Cloning repositories
  - git clone command
- Pushing changes to remote
  - git push command
  - Understanding remotes and branches
- Pulling changes from remote
  - git pull command
  - Fetch vs. Pull
- Fetching changes
  - git fetch command
  - Reviewing changes before merging

### 6. Collaboration with Git and GitHub
- Forking repositories
  - When and why to fork
  - Keeping a fork updated
- Creating pull requests
  - From a fork
  - From a branch in the same repository
- Reviewing and commenting on pull requests
  - Code review best practices
  - Using GitHub's review features
- Merging pull requests
  - Merge strategies (merge commit, squash, rebase)
- Issues and issue tracking on GitHub
  - Creating and assigning issues
  - Linking issues to pull requests
- Advanced Collaboration
  - Continuous integration (CI) with GitHub Actions

### 7. Advanced Git Concepts
- Rebasing
  - Basic rebasing concept
  - Interactive rebasing
  - When to use (and when not to use) rebasing
- Cherry-picking
  - Applying specific commits to branches
  - Use cases for cherry-picking
- Resetting
  - Soft reset
  - Mixed reset
  - Hard reset
  - Dangers of resetting public history
- Reverting changes
  - Creating revert commits
  - Reverting multiple commits

## II. Python

### 1. Python Basics
- Python installation and setup
  - Installing Python on different operating systems
  - Setting up virtual environments
- Python interpreter and running scripts
  - Interactive mode vs. script mode
  - Using IDEs and text editors (VS Code, PyCharm)
- Basic syntax and data types
  - Indentation and code blocks
  - Comments and docstrings
  - Integers, floats, strings, booleans
- Variables and operators
  - Variable naming conventions
  - Assignment operators
  - Arithmetic operators
  - Comparison operators
  - Logical operators

### 2. Control Structures
- Conditional statements
  - if statements
  - elif and else clauses
  - Nested conditionals
- Loops
  - for loops
    - Iterating over sequences
    - Using range()
  - while loops
    - Condition-controlled loops
    - Infinite loops and how to avoid them
- Control statements
  - break statement
  - continue statement
  - pass statement

### 3. Data Structures
- Lists
  - Creating and accessing lists
  - List methods (append, extend, insert, remove, etc.)
  - Slicing lists
- Tuples
  - Immutable sequences
  - Tuple packing and unpacking
- Sets
  - Creating sets
  - Set operations (union, intersection, difference)
- Dictionaries
  - Creating dictionaries
  - Accessing and modifying dictionary data
  - Dictionary methods
- List/Dictionary comprehensions
  - Basic syntax
  - Conditional comprehensions
  - Nested comprehensions

### 4. Functions
- Defining and calling functions
  - Function syntax
  - Return values
  - Default arguments
- Arguments and parameters
  - Positional arguments
  - Keyword arguments
  - Variable-length arguments (*args, **kwargs)
- Lambda functions
  - Syntax and use cases
  - Limitations of lambda functions
- Built-in functions
  - map(), filter(), reduce()
  - zip(), enumerate()

### 5. Modules and Packages
- Importing modules
  - import statement
  - from ... import syntax
  - Aliasing imports
- Creating custom modules
  - Writing reusable code
  - \_\_name__ == "\_\_main__" idiom
- Package structure
  - Creating packages
  - \_\_init__.py files
- Package management
  - pip and PyPI
  - Requirements files

### 6. File Handling
- Reading and writing text files
  - open() function and file modes
  - read(), readline(), and readlines() methods
  - write() and writelines() methods
- Working with CSV files
  - csv module
  - Reading and writing CSV data
- Working with JSON
  - json module
  - Serializing and deserializing JSON data

### 7. Object-Oriented Programming
- Classes and objects
  - Defining classes
  - Creating instances
  - Instance methods and attributes
- Inheritance
  - Single inheritance
  - Multiple inheritance
  - Method resolution order (MRO)
- Polymorphism
  - Method overriding
  - Duck typing
- Encapsulation
  - Private and protected attributes
  - Property decorators
- Abstraction
  - Abstract base classes
  - Interfaces in Python

### 8. Exception Handling
- Try-except blocks
  - Basic exception handling
  - Handling multiple exceptions
  - else and finally clauses
- Raising exceptions
  - raise statement
  - Creating custom exceptions
- Handling and logging errors
  - logging module
  - Best practices for error handling

### 9. Advanced Python Concepts
- Decorators
  - Function decorators
  - Class decorators
  - Decorators with arguments
- Generators
  - yield statement
  - Generator expressions
- Iterators
  - iter() and next() functions
  - Creating custom iterators
- Context managers
  - with statement
  - Creating custom context managers

### 10. Python Standard Library
- os module
  - File and directory operations
  - Environment variables
- sys module
  - System-specific parameters and functions
- datetime module
  - Working with dates and times
  - Time zones and timedeltas
- re module for regular expressions
  - Pattern matching
  - Substitution and splitting

### 11. External Libraries
- **requests for HTTP**
  - Making GET and POST requests
  - Handling responses and errors
- **Beautiful Soup for web scraping**
  - Parsing HTML
  - Extracting data from web pages
- **pandas for data manipulation**
  - Working with DataFrames
  - Data analysis and transformation
- **FastAPI for web development**
  - Setting up and creating web applications
  - Routing, dependency injection, and middleware
  - Asynchronous programming and performance benefits
  - Database integration and migrations using SQLAlchemy or Tortoise ORM
- **NumPy for numerical operations**
  - Arrays, mathematical functions, and statistical operations
- **Matplotlib for basic data visualization**
  - Creating plots, charts, and graphs

### 12. Testing in Python
- unittest framework
  - Writing test cases
  - Test fixtures and setup/teardown
- pytest
  - Writing and running tests with pytest
  - Fixtures and plugins
- Test-driven development (TDD) basics
  - Red-Green-Refactor cycle
  - Benefits and challenges of TDD

### 13. Real-world Applications
- Combine multiple libraries in projects
  - Web scraper that stores data in a database and visualizes it
  - API development with FastAPI/Django


  - Data analysis and visualization projects

## III. SQL

### 1. Introduction to Databases and SQL
- Why databases are important
- What is a database?
- What is SQL?
- How to install MySQL database

### 2. DDL Commands
- Creating tables with `CREATE`
- Modifying tables with `ALTER`
- Deleting tables with `DROP`
- Renaming tables with `RENAME`
- Removing data with `TRUNCATE`

### 3. DML Commands
- Inserting data with `INSERT`
- Updating data with `UPDATE`
- Deleting data with `DELETE`
- Retrieving data with `SELECT`

### 4. Constraints
- Primary key constraint
- Foreign key constraint
- Unique key constraint
- Not null constraint

### 5. SQL Clauses
- Ordering data with `ORDER BY`
- Filtering data with `WHERE`
- Grouping data with `HAVING`

### 6. Transactional Commands
- Rolling back transactions with `ROLLBACK`
- Committing transactions with `COMMIT`
- Setting savepoints with `SAVEPOINT`

### 7. Joins
- Inner join
- Outer join
- Cross join
- Full join

## IV. Web Development with React

### 1. JavaScript Fundamentals
- Variables and data types
  - var, let, and const
  - Primitive types and objects
- Operators and control structures
  - Arithmetic and comparison operators
  - if statements, switch statements, and loops
- Functions
  - Function declarations and expressions
  - Arrow functions
- ES6+ features
  - Destructuring
  - Spread and rest operators
  - Template literals
  - Modules (import/export)

### 2. React Basics
- Introduction to React
  - What is React?
  - Virtual DOM concept
- Setting up a React environment
  - Create React App
  - Project structure
- JSX syntax
  - Writing JSX
  - Expressions in JSX
  - JSX vs HTML differences

### 3. React Components
- Functional components
  - Creating functional components
  - Props in functional components
- Class components
  - Creating class components
  - State in class components
- Props and state
  - Passing props
  - Updating state
- Lifecycle methods
  - Mounting, updating, and unmounting phases
  - Common lifecycle methods (componentDidMount, componentDidUpdate, etc.)

### 4. Hooks in React
- useState
  - Managing state in functional components
  - Multiple state variables
- useEffect
  - Side effects in functional components
  - Dependency array
  - Cleanup functions
- Custom hooks
  - Creating reusable hooks
  - Rules of hooks
- Other built-in hooks
  - useContext for context API
  - useReducer for complex state logic
  - useRef for DOM references

### 5. Handling Events and Forms
- Event handling in React
  - Synthetic events
  - Passing arguments to event handlers
- Controlled components
  - Managing form inputs with state
  - Handling multiple inputs
- Form validation
  - Client-side validation techniques
  - Displaying error messages

### 6. React Router
- Setting up routes
  - BrowserRouter and Route components
  - Switch component for exclusive routing
- Navigation
  - Link and NavLink components
  - Programmatic navigation with history
- Route parameters
  - Dynamic routes
  - Accessing route parameters
- Nested routing
  - Creating subroutes
  - Outlet component in React Router v6

### 7. State Management
- Context API
  - Creating and providing context
  - Consuming context with useContext
- Advanced State Management
  - Redux principles and detailed coverage
  - Actions, reducers, and store
  - Connecting Redux to React components
  - useReducer for complex state management

### 8. Working with APIs
- Fetch API
  - Making GET, POST, PUT, DELETE requests
  - Handling responses and errors
- Axios
  - Setting up and using Axios
  - Interceptors and config
- Handling asynchronous operations
  - Promises and async/await
  - Loading states and error handling
- Error handling
  - Try-catch blocks
  - Error boundaries in React
- Integrations
  - Practical examples of integrating React with back-end APIs
  - Introduction to GraphQL and integration with React

### 9. Styling in React
- CSS modules
  - Creating and using CSS modules
  - Benefits of scoped styles
- Styled components
  - Writing CSS in JS
  - Dynamic styling with props
- CSS-in-JS solutions
  - Overview of popular libraries (e.g., Emotion, JSS)

### 10. Testing React Applications
- Jest for unit testing
  - Writing and running tests
  - Mocking modules and functions
- React Testing Library
  - Component testing
  - User event simulation
  - Best practices for testing React components

### 11. Performance Optimization
- React.memo
  - Memoizing functional components
  - When to use memoization
- useMemo and useCallback
  - Optimizing expensive calculations
  - Preventing unnecessary re-renders
- Code splitting
  - Dynamic imports
  - React.lazy and Suspense

### 12. Deployment
- Building for production
  - Optimizing the build process
  - Environment variables
- Deployment options
  - Netlify deployment
  - Other hosting platforms (GitHub Pages, AWS S3)

## V. Django

### 1. Introduction to Django
- What is Django?
- Features of Django

### 2. Getting Started
- How to create a project
- How to create an application
- Working with complete file structure in Django after creating Django project & application
- How to create more than one application
- How to create a `urls.py` file at application to improve performance

### 3. Core Concepts
- Working with MVT design pattern
- Working with templates folder for frontend development
- Working with Static folder for frontend design development
- Implementing JavaScript in Django
- Implementing Bootstrap in Django
- Working with model class in Django
- Working with Django forms

### 4. Model Relationships
- Working with Django model relationships
  - One To One Relationship
  - Many To One Relationship
  - Many To Many Relationship

### 5. Exception Handling
- Django Exceptions
  - Working with predefined exceptions
  - Working with custom exceptions

### 6. Django ORM
- Django ORM
- Django Cookies & Sessions implementations
- Django Custom Routing
- Django Image uploading
- Django file uploading

### 7. Django Rest Framework (DRF)
- Why Django rest framework is required
- What is API
- What is Web API
- What is Rest-Ful API
- How to create restful APIs using Django rest framework
- Working with Postman tool to test our restful APIs

## VI. AWS (Amazon Web Services)

### 1. Introduction to Cloud Computing
- Cloud computing concepts
  - IaaS, PaaS, SaaS models
  - Benefits of cloud computing
- AWS global infrastructure
  - Regions and Availability Zones
  - Edge locations and CDN

### 2. Compute Services
- EC2 (Elastic Compute Cloud)
  - Launching EC2 instances
  - Instance types and sizing
  - Security groups and key pairs
- Lambda for serverless computing
  - Creating Lambda functions
  - Event triggers
  - Cold starts and performance considerations

### 3. Storage Services
- S3 (Simple Storage Service)
  - Buckets and objects
  - S3 storage classes
  - Bucket policies and access control
- EBS (Elastic Block Store)
  - Creating and attaching EBS volumes
  - EBS volume types
  - Snapshots and backups

### 4. Database Services
- RDS (Relational Database Service)
  - Supported database engines
  - Creating and managing RDS instances
  - Multi-AZ deployments and read replicas
- DynamoDB for NoSQL
  - Tables, items, and attributes
  - Partition keys and sort keys
  - Read and write capacity units

### 5. Application Integration
- SQS (Simple Queue Service)
  - Creating and managing queues
  - Message processing and visibility timeout
  - Dead letter queues
- SNS (Simple Notification Service)
  - Topics and subscriptions
  - Publishing messages
  - Integration with other AWS services

### 6. Monitoring and Management
- CloudWatch for monitoring
  - Metrics and dashboards
  - Alarms and notifications
  - Log management
- CloudFormation for infrastructure as code
  - Writing CloudFormation templates
  - Stacks and stack sets
  - Change sets and stack updates

### 7. Deployment and Management
- Elastic Beanstalk
  - Deploying applications
  - Environment configuration
  - Updating and monitoring applications
- CloudFront for content delivery
  - Creating distributions
  - Origin and behavior settings
  - Caching strategies

### 8. AWS SDK for Python (Boto3)
- Installing and configuring Boto3
  - Setting up credentials
  - Creating service clients and resource objects
- Interacting with AWS services using Python
  - S3 operations (upload, download, list)
  - EC2 management
  - Working with DynamoDB

### 9. Serverless Applications
- Building serverless applications
  - AWS Lambda functions
  - API Gateway for RESTful APIs
  - Step Functions for workflows
- Serverless Framework (optional)
  - Defining serverless applications
  - Deploy

---

## VII. Capstone Project: Interview App with Google Speech-to-Text and Text-to-Speech

### Full-stack application leveraging Python, React, Django, and AWS

### 1. Defining Project Requirements
- **Identifying project goals and objectives**
  - Create an application to facilitate mock interviews.
  - Integrate Google Cloud's Speech-to-Text for converting spoken questions to text.
  - Use Google Cloud's Text-to-Speech to convert text-based interview questions to speech.
- **Creating user stories and acceptance criteria**
  - As a user, I can speak my answers, and they will be transcribed automatically.
  - As a user, I can listen to the questions asked by the system.
  - As an admin, I can manage interview questions and review transcriptions.
- **Determining MVP (Minimum Viable Product) features**
  - Basic interview interface with speech-to-text and text-to-speech functionality.
  - User authentication and session management.
  - Dashboard for admins to view and manage questions and answers.

### 2. Designing System Architecture
- **Creating high-level system design**
  - Frontend: React-based user interface.
  - Backend: Django-powered API.
  - Speech services: Google Cloud APIs for Speech-to-Text and Text-to-Speech.
  - Storage: AWS S3 for storing audio files.
  - Database: AWS RDS or DynamoDB.
- **Designing database schema**
  - Users table (with roles for users and admins).
  - Questions and answers tables.
  - Transcriptions and audio storage paths.
- **Planning API endpoints**
  - Endpoints for user authentication.
  - Endpoints for managing questions and answers.
  - Endpoints for triggering speech-to-text and text-to-speech.

### 3. Implementing Backend with Django
- **Setting up project structure**
  - Create Django project and necessary applications.
- **Implementing models and database migrations**
  - Define models for users, questions, answers, and transcriptions.
  - Set up migrations for database schema.
- **Creating API views and serializers**
  - Build views for managing interview sessions.
  - Serialize data for frontend consumption.
- **Implementing authentication and authorization**
  - Use Django's authentication system.
  - Set up role-based access control for users and admins.
- **Writing unit and integration tests**
  - Test individual components of the backend.
  - Perform integration tests for API endpoints.

### 4. Containerizing the Application
- **Creating a Dockerfile**
  - Define the Dockerfile to containerize the Django application.
  - Include necessary dependencies and environment configurations.
- **Building and testing the Docker image**
  - Build the Docker image locally and test it.
  - Ensure that the application runs correctly in the container.

### 5. Deploying with AWS App Runner
- **Setting up AWS App Runner**
  - Deploy the containerized Django application using AWS App Runner.
  - Configure App Runner with the correct environment variables and settings.
- **Connecting to AWS RDS or DynamoDB**
  - Ensure that the deployed application can connect to the database.
  - Configure security groups and VPC settings as needed.

### 6. Creating Frontend with React
- **Setting up React project with Create React App**
  - Initialize the project and configure the environment.
- **Implementing component structure**
  - Develop components for interview interface, login, and admin dashboard.
- **Managing state and integrating with backend API**
  - Use React's state management and context API.
  - Fetch and display data from the Django backend.
- **Implementing routing and navigation**
  - Use React Router for navigation between different views.
- **Creating forms and handling user input**
  - Build forms for user registration, login, and interview responses.
- **Writing unit tests for React components**
  - Use Jest and React Testing Library to test components.

### 7. Integrating with AWS Services
- **Using S3 for file storage**
  - Store audio files and other assets in S3 buckets.
- **Implementing CloudFront for content delivery**
  - Distribute static assets using CloudFront.
- **Setting up Route 53 for domain management**
  - Manage domain and DNS settings.

### 8. Version Control and Collaboration
- **Using Git for version control**
  - Commit code regularly and use feature branches.
- **Creating and managing branches**
  - Follow GitFlow or another branching strategy.
- **Conducting code reviews via pull requests**
  - Use GitHub for code review and collaboration.
- **Using GitHub Projects for task management**
  - Track progress using GitHub Projects or another task management tool.

### 9. Testing and Quality Assurance
- **Conducting thorough testing (unit, integration, end-to-end)**
  - Ensure the application is thoroughly tested before deployment.
- **Performing security audits**
  - Check for security vulnerabilities in the codebase.
- **Optimizing performance**
  - Profile and optimize both frontend and backend components.

### 10. Documentation
- **Writing technical documentation**
  - Document the project architecture, APIs, and setup process.
- **Creating user guides or README files**
  - Provide detailed instructions for users and contributors.
- **Documenting API endpoints**
  - Use tools like Swagger or Postman to document and test APIs.

### 11. Deployment and DevOps
- **Setting up CI/CD pipeline with GitHub Actions**
  - Automate testing, building, and deployment processes.
- **Implementing monitoring and logging with CloudWatch**
  - Set up monitoring for the application and infrastructure.
- **Configuring error tracking and reporting**
  - Use tools like Sentry for error tracking and logging.

### 12. Presentation and Demo
- **Preparing project presentation**
  - Create a comprehensive presentation covering the project.
- **Creating a live demo**
  - Set up a live demo for stakeholders or potential employers.
- **Discussing challenges and lessons learned**
  - Reflect on the development process and outcomes.

---

## VIII. Course Conclusion and Next Steps

### 1. Review and Reflection
- Summarizing key learnings from each module
- Reflecting on personal growth and skill development
- Identifying areas for further improvement

### 2. Portfolio Development
- Refining capstone project for portfolio inclusion
- Creating a personal website or GitHub portfolio
- Highlighting key projects and skills

### 3. Continuous Learning Strategies
- Staying updated with technology trends
- Participating in coding challenges and hackathons
- Contributing to open-source projects

### 4. Career Preparation
- Resume building and LinkedIn profile optimization
- Preparing for technical interviews
- Networking strategies in the tech industry

