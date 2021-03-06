This module allows National Instruments TDM/TDX files to be accessed like
NumPy structured arrays.

It can be installed in the standard way::

    python setup.py install

Sample usage::

    import tdm_loader
    data_file = tdm_loader.OpenFile('filename.tdm' [, encoding='utf-8'])

Access a channel by number or name for the first channel_group::

    data_file[channel]

Access a channel in a channel_group by name or number::

    data_file[channel_group, channel]

Access a column by number or name::

    data_file.col(column_num)

Access a channel by channel group and channel index or name combination::

    data_file.channel(channel_group, channel)

Get a whole channel group as dict:

    data_file.channel_dict(channel_group)

Search for a column name.  A list of all column names that contain
``search_term`` and their indices will be returned::

    data_file.channel_search(search_term)