.. flexibility documentation master file, created by
   sphinx-quickstart on Wed Jul 26 13:11:33 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: .static/Dong-Energy.png
	:scale: 10%
	:align: right


flexibility
===========

:Author:
   Ruben Menke
   *rmenk@dongenergy.dk*
:Release: |release|
:Date: |today|

*flexibility* is a module containing a collection of scripts and data sources to
analyse flexibility in the power market. For a look through the documentation
have a look here:

.. toctree::
   :maxdepth: 1

   introduction
   asset
   analysis
   scheduling
   data
   contract
   contrib_guide


Aims
----
The aim of the module is to provide a framework to collect the different types
of analyses that are regularly performed when assessing the performance of
flexibility assets. This means that the focus is on providing an easy access to
parsed and correct data for the various input sources and shortcuts to invoke
often needed calculations.

Quick start
-----------
In a jupyter notebook do this: ::

    import pandas as pd
    import numpy as np
    import flexibility

    #load a predefined asset:
    amp = flexibility.asset.Asset('amp')

    # Pass the asset definition to the analysis
    analysis = flexibility.analysis.Analysis(asset = amp)

    # run day ahead schedule
    analysis.schedules.set_da_schedule('amp')

    # Let's not bother trading on the intraday market
    analysis.schedules.set_wd_schedule('lazy')

    # Let's use the realistic simulation of operation in the imbalance
    analysis.schedules.set_imba_schedule('realistic')

    # Let's have a look at the results so far
    analysis.data.data['schedule'].head()

This should give you a pandas dataframe with an overview of the schedule. The
schedule is the list of power settings sent to the asset.
The `da` is the day ahead schedule, so the schedule after we sold power on the
day ahead market.
`wd` is the withinday or intraday market, which we skipped so it should be the
same as the day ahead. The final schedule is the one that actually ran, and
includes our actions from the imbalance market. Have a look at the introduction
for more information and examples.


.. py:module:: flexibility

Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
