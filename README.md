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


