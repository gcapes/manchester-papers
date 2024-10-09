For questions you thought about after Gerard has left your life. 

Perhaps it will be helpful to his next batch of students while they desperately try to think of something witty to write in one of those other files...

# Questions
## If I create a private repository, is this enough to ensure no one can see it without my ssh key and password?
- Yes. If you have a private repo, no one else can see or use it unless they have been given collaborator access to your repo.
- If the repo is within a GitHub organisation, it may also be visible to the organisation administrators.


## How safe is my data on Github? Is it an ok place to keep code that might end up being confidential?
- You can start off confidential (private) and then go public but you can't really go the other way
  (you can change the visibility to private but if your code is already out there ...)
- It can be considered confidential in terms of code used for a paper not yet published


## Non-text files
I often write code/scripts that go read some raw data, process it and produce secondary data,
which may or may not be in plain text format. 
Then this secondary data can be used to make graphs, tables, which in turn can be included in reports or manuscripts. 
Are there recommended ways to organise this type of workflow around git/github?

Do I want to push the secondary data, and if so, 
are there best practices around keeping track of which version of the script was used to produce a given secondary data file? 
What about graphs that will be either editable or png/jpg, etc. 
Do I push those or keep them on some other online-accessible place and only keep links to them in the respoitory? 

- Generally speaking you shouldn't be committing non-text files to a git repo, nor files that can be recreated automatically
  (such as secondary data files or 
- To keep track of which commit was used to generate any given output, one approach could be to embed the commit ID into
  the filename of the secondary data file/graph image file. You can get the SHA using `git rev-parse --short HEAD`
- For storing large files you could consider git LFS, or storage outside of version control e.g. OneDrive, RDS
 
