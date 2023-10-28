## Guidy
This tool is designed to help you manage roles, permissions, flows, and operations as code. The primary goal is to store Directus settings in human-readable JSON files so that they can be version-controlled and easily redeployed. Below, I'll provide a more detailed explanation of how to use these tools:

## 1. Features

### 1.1. Save Roles and Permissions
- You can save roles and permissions into JSON files, making it easy to version control and manage access control settings in Directus.

### 1.2. Load Roles and Permissions
- These tools allow you to load roles and permissions from JSON files into a Directus instance, ensuring that your access control configurations can be easily restored.

### 1.3. Save Flows and Operations
- Flows and operations are also stored in JSON format, allowing you to save them as code in your projects.

### 1.4. Load Flows and Operations
- You can load flows and operations from JSON files into your Directus instance, enabling you to manage and maintain your workflows as code.

## 2. How to Use

### 2.1. Setup Dev Environment

#### Set up Directus
For testing purposes, you can start a local Directus instance using Docker. Here are the steps:

1. Navigate to the "test" directory.
2. Run the following Docker Compose command to start Directus locally:
   ```
   docker-compose up
   ```

3. Open your web browser and visit http://localhost:8055/.
4. Log in using the provided credentials: username - `admin@example.com`, password - `d1r3ctu5`.
5. Set a static token for the admin user. In this case, the token is `GNuG2xodzTMY19AaYh0r7yYNWSqWF-AE`.

#### Create Collections
You should create collections within Directus as needed for your project.

### 2.2. Load Roles

Change your current directory to the "src" directory and run the following command to load roles and permissions:

```
python load_roles.py
```

### 2.3. Save Roles

To save roles and permissions, change your current directory to the "src" directory and run:

```
python save_roles.py
```

### 2.4. Save Flows

To save flows and operations, change your current directory to the "src" directory and run:

```
python save_flows.py
```

The script will attempt to save all the flows into a directory configured in the `config.ini` file. Make sure to set the correct URL and token for Directus in the `config.ini` file. You can use `config.ini.sample` as a reference.

### 2.5. Load Flows

To load flows and operations, change your current directory to the "src" directory and run:

```
python load_flows.py
```
![image](https://github.com/kinnovent/directools/assets/311397/87f14b3f-6d69-4b8f-a10d-ef4f844eadb0)

The script will try to load all the flows from a directory configured in the `config.ini` file.

Please ensure that you document your project and these steps in a more detailed manner for easy reference by other team members or users. This documentation should include information on the purpose and usage of these tools and provide examples of configuration files and commands.
