# Example

This is for my own training purposes and is not intented to be read without instruction.

This guide/training thing reads top down.
If you completed sections out of order you will be missing steps.

## Terminology

We use terminology wrong

upstream = `remote`

A `project` as mentioned in here is a clone of the repository. It simulates having the set up across multiple people's computers.

## Set up

1. Clone repo
2. Clone repo again into a different folder
3. Open each folder in IDE
4. View git graph is the same (sourcetree if you want)
5. View git graph in Github/lab

## Learning about *distributed* git

Create a new branch, and check it out

```sh
git checkout -b feature1
```

Notice that the branch isn't available anywhere except where you created it.

To tell the remote about it, use `push`.

```sh
git push --set-upstream origin feature1
```

1. View the branch is visible in github/lab
2. Notice the branch is not visible in second clone

To make it available in the second project, we need to use `fetch`.

In second project:

```sh
git fetch
```

1. View git graph

### Same with a commit

```sh
git add .
git commit -m "2 Added abc line"
```

Is it there?

What do?

## Merge requests

Before you start this section, make a commit in the 'other' project.

```sh
git checkout -b feature2
echo "123.txt" > 123.txt
git add 123.txt
git commit -m "3 Add 123"
```

Back to first project.

Create an MR using ...
