# Manage secrets

## What are secrets?

**Secrets** are objects that contain a short piece of sensitive data (like a password, key, or token). You don’t want this information to be visible to everyone who accesses your app, but it needs to be stored within your app. We use **secrets management** to make this possible. This way, our clients’ apps can authenticate to APIs and databases securely.

Secrets are managed entirely through your management console. Adding, deleting, or editing a secret takes just a few steps, which we’ve [outlined later in this doc](#how-do-i-edit-a-secret).

## Not sure why you’d need a secret?

If your app is using a database or an API, you’ll need to use secrets.

1. To talk to databases and APIs, you’ll need to authenticate.
2. Keys and passwords (secrets) are used to securely authenticate apps.
3. To keep secrets secure, they can’t be put anywhere that someone could stumble upon them.
4. Secret management makes your secrets available to your app **without compromising their security** -- your app’s users won’t be able to access your secrets.

## How do I manage secrets?

Secrets can be created, deleted, and edited within **your management console**.

## How do I create a secret?

### 1. Open your management console

Open your management console.

### 2. Navigate to your workload

#### Select continuous deployment in the lefthand menu

#### Select your associated cluster

#### Select your deployment

#### Select Secrets

If you have an existing secret, you’ll be able to see it there.

### 3. Add a secret

#### Select the purple Add secret button in the top right corner

#### Input your secret’s name and value

For example, you might name your secret secret1 and include the key (or password) itself in the value field.

Secrets names should **follow these guidelines:**
Consist **solely of** UPPERCASE LETTERS, digits (e.g. 1, 2, 3, 4, 5), and the underscore symbol (_)
Do **not** begin with a digit

Note that you **can’t change the name of a secret** after you create it, so make sure the name you choose will be relevant even if you make any updates.


#### Select save to save your new secret in the environment


## How do I edit a secret?

### 1. Open your management console

### 2. Navigate to your Workload

Select continuous deployment in the lefthand menu.

### 3. Select your associated cluster

### 4. Select your deployment

Select Secrets.

If you have an existing secret, you’ll be able to see and change it from this screen.

### 5. Select the gears icon beside your secret

You’ll have the option to change your secret’s value.

## How do I delete a secret?

### 1. Open your management console

### 2. Navigate to your Workload

Select **your deployment**.

Select **Secrets**.

### 3. Delete your secret

Select the **trash can button** next to your secret’s name.

Confirm that you want to **delete this secret**.


## How are secrets configured?

Your Workspace will configure each new secret as an individual environment variable in your application. For example, you might add a secret with the name `EXAMPLE_API_KEY`. You can access this secret using the following Python code:

```
import os

os.environ[“EXAMPLE_API_KEY”]
```
