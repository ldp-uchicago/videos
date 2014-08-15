# RCC

You can access the RCC systems via `ssh`:

    ssh <CNetID>@midway.rcc.uchicago.edu

See the [user guide](http://docs.rcc.uchicago.edu/user-guide.html#ssh) for more info. 

See [this section](http://docs.rcc.uchicago.edu/user-guide.html#storage) of the guide for an overview of storage allocations ... or [this gist](https://gist.github.com/joyrexus/7453f4e0ba9a0dc2f1f5) for a summary.

RCC accounts are obtained under the aegis of a particular project with a designated PI.  In our case, the project's account name is `pi-sgsg` and the PI is Susan Goldin-Meadow.  The principal storage area for the project can be found at `/project/sgsg`.

To check our overall allocation we can use `accounts balance`:

    [jvoigt@midway-login1 ~]$ accounts balance
    Account Balance: Wed Jan 29 13:29:31 2014
    Accounts:   pi-sgsg

    +---------+------------+----------+----------+
    | Account | Allocation | Usage    | Balance  |
    +---------+------------+----------+----------+
    | pi-sgsg |       5000 |     0.00 |  5000.00 |
    +---------+------------+----------+----------+

To check our storage quotas we can use `quota`:

    [jvoigt@midway-login1 ~]$ quota
    Disk quotas for user jvoigt:
    Filesystem       type          used     quota     limit      files
    ----------       -------- --------- --------- --------- ----------
    home             USR       384.00 K   25.00 G   30.00 G         13
    midway-scratch   USR        32.00 K    1.00 T    5.00 T          1
    project-sgsg     FILESET    42.98 G    5.49 T    6.04 T         67

