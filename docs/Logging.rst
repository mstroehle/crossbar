:orphan:

Logging
=======

Crossbar.io has configurable logging systems, to make it's log output
easier to consume or nicer to look at.

    Crossbar's structured logging system is present in versions 0.11 and
    above, and a lot of these options will only work in these versions.

Formats
-------

Crossbar.io has three log formats, specified by the ``--logformat``
switch.

-  ``color``: This is the default, and outputs colored logging messages.
   `Example <https://asciinema.org/a/73tuxhtzl8yokk0pqstomyu1j>`__
-  ``nocolor``: This reduces the color output by Crossbar, and is
   suitable for redirecting to files.
   `Example <https://asciinema.org/a/eqx5dt291xuwjap2b3g6g8gql>`__
-  ``syslogd``: This removes timestamps, and reduces the color.
   `Example <https://asciinema.org/a/9ropoyi6k9hpr7l5sbesqutox>`__

Levels
------

Crossbar.io supports restricting the output to certain levels, specified
by the ``--loglevel`` switch. These levels are:

-  ``none``: No output.
-  ``critical``: Critical or above.
-  ``error``: Error or above.
-  ``warn``: Warning or above.
-  ``info``: The default -- Info or above.
-  ``debug``: Debug or above, and turn on the source location of the log
   events (what class/function generated them).
   `Example <https://asciinema.org/a/bdt8linu408ihiq0fkqazx930>`__
-  ``trace``: Trace or above. Some internal Crossbar.io components
   support trace logging, this is not yet extended to user components.

Logging to a file
-----------------

By passing ``--logtofile`` to Crossbar.io, you can log to the location
specified by ``--logdir``. You may combine the ``--loglevel`` switches
with ``--logtofile``, but not ``--logformat`` (it is always in
``nocolor``).

Adding logging to your components
---------------------------------

If you want to integrate with Crossbar.io's logging system, see :doc:`Logging in Crossbar.io <Logging-in-Crossbar.io>` .
