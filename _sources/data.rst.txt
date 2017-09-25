Data
=====

The data is stored in the *data* directory supplied with this module, 
but pooled from various sources. For consistent results, use the 
functions provided in the data module to access and manipulate the data.

Update functions
................

The function of the data module are called when the data module is used as
a standalone module to update the database.

.. autofunction:: flexibility.data.data_update.WD_update

.. autofunction:: flexibility.data.data_update.WD_data_check

Examples:
    >>> data.data.WD_update()
        

Data class
..........

The data class is added to the analysis to load the data.
The data is retrieved from the in the data folder and if 
available a pre-determined data base is loaded for the analysis.
NOT IMPLIMETED YET!
        
.. autoclass:: flexibility.data.data.Data
   :members:

