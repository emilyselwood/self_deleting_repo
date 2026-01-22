# The Self Deleting Repo

This repo will self destruct in ...


## WTF?

There are a lot of ways to get a repo of code to execute code on your local machine with out you realising its going to. When you open this repo in an editor or IDE it will endevor to delete its self.

## Ok, but this is safe right?

Yes, in theory. Assuming you've not cloned this somewhere weird... like your `c:\windows` directory.

## So how?

There are a lot of ways of running code you probably don't realise you need to trust when you open a repo for editing. What does that "Do you trust the authors of this repo?" pop up really mean?

### Rust

`build.rs` is evil and can do anything it likes, when cargo builds a project it runs all the code in there with the privs of your shell or editor. It'll cause an error because the code files will vanish under it but the repo will be gone.

## VS code tasks

`.vscode/tasks.json` can define any script it likes to execute when the folder is opened. It'll automatically run `delete_me.sh` in this case.


## Ok, but why?

I don't think most people realise the implications of that "Do you trust the authors of this code" message that pops up when you open a new code repo. What the heck do you actually need to check for in the repo before you can say "yeah I trust this" When you click that button code someone else wrote is going to run on your computer. We should probably be a little more careful with this stuff. 

Those editors that say "Trust anything in the parent directory" make things much worse if you check out everything into the same place `~/projects` or `~/git` etc.
