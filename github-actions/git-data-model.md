# Context
While debugging, I realized that it was harder for me to make sense of the project history at work, when there were 'superfluous' merge commits that were automatically generated whenever someone needed to synchronize with the central repository with git pull. 

So I decided to learn more about the underlying data model of git. 

# Storage
Git object storage is just a directed acyclical graph, with a handful of different types of objects. Git maintains a set of objects and set of references. 

# Takeaway
HEAD and branches are references, so they are mutable; whereas, the nodes are immutable. 



