# Permissions

All LDP members for which an account was created should be able to log into midway with their cnet credentials.

All users (except for those noted below) are members of the `pi-sgsg` group and have read/execute permissions on all project subdirectories. 

In addition to the `pi-sgsg` group, Robin Weiss of the RCC created an `sgsg-editors` group for us with the following users:

* Jason Voigt (jvoigt)
* Kristi Schonwald (kschoend)
* Reihonna Frost (reihonna)
* Dana Glenn (glennd)
* Katherine Lawlor (katielawlor)
* Theodora Koumoutsakis (tkoumou1)

We can use this to enable read/write/execute privs for group members on all project subdirs by making `sgsg-editors` the group owner (`chgrp -R sgsg-editors *`).

---

Robin writes ...

The easiest way to accomplish the access level you indicated (sgsg-editors has read/write and everyone else has read only) would be to first ensure /project/sgsg has permissions 770 with pi-sgsg as the group owner (which it does, we we're all good there).  All the members of your group are in the group pi-sgsg so they will all have the ability to get into this top level directory.  Then, what we can do is set all of the sub-folders within /project/sgsg to permissions 775 and set the group ownership to sgsg-editors.  This way, all members of sgsg-editors will get the r/w/x permissions, and everyone else will only get r/x as they will get the "others" permission level (r+x) since they are not members of sgsg-editors, but they are able to get into /project/sgsg since they are members of pi-sgsg.

`/project/sgsg` is already set up correctly, so to do the rest of the configuration, you will want to cd into `/project/sgsg` and do the following commands:

    chgrp -R sgsg-editors *
    chmod -R 775 *

The first command is going to set the group ownership of all files and directories to sgsg-editors. The second command is going to set the permissions to 775 on all of the files and directories.

You should probably run these commands whenever you copy files into the project space to just make sure everything is consistent across the files and directories you create.

Once we have our data migrated over and a directory structure settled upon, we can create additional groups for more fine-gained control.
