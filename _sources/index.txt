.. SpikeSort Homepage documentation master file, created by
   sphinx-quickstart on Fri Jan 20 17:56:12 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome
=======

*SpikeSort is a flexible spike sorting framework implemented completely
in Python. It features manual and automatic clustering, many data
formats and it is memory-efficient. Truely Open Source, BSD-licensed.*

Eavesdropping on neurons in action
----------------------------------

Spike sorting is a common pre-processing step for the analysis of
neuroscientific data.  The goal of the procedure is to detect the times
at which neurons generated action potential, also called spikes.

The times at which spikes arrive encode information about sensory stimuli and
their perception. Therefore, correct identification of occurrences of
spikes elicited by different neurons is necessary to understand
the function and disfunction of nervous system.

Spike sorting done right
------------------------

Spike sorting is based on
extracellular recordings of small electric potential associated with
spikes by microelectrodes placed very close to the cell. In practice, such
electrodes pick up activity of multiple neurons active simultaneously.
The goal of spike sorting is  to discriminate the responses of
indvidual cells from others. 

Each cell has its own characteristic spike waveshape, so that cells
can be easily differentiated just by comparing their spikes.  Spikes
of similar shapes and amplitudes are grouped together using automatic or manual
clustering procedure.

If you want to know more read an in-depth article on spike sorting in
`Scholarpedia`_ or simply go directly to the :ref:`tutorials
<docs:tutorials-section>` in the documentation of SpikeSort and start
sorting.

Start sorting in matter of minutes
----------------------------------

Run included Python script:

.. code-block:: bash

   $ export DATAPATH='where/your/data/is/located'
   $ python -i cluster_beans.py

and you can start sorting:

.. code-block:: pycon
   
   >>> browser.show()                         # sort and show results
   >>> cluster = base.features['LabelSource'] 
   >>> cluster.recluster(1, 'gmm',2 )         # split cell 1 into 2 clusters
   >>> cluster.delete_cells(2, 3)             # delete unwanted cells

Features
--------

* user-friendly and customisable,

* interactive command-line interface in Python,

* graphical-user interface and visualization widgets,

* k-means and gaussian mixture models clustering algorithms and manual
  cluster cutting,

* support for multi-channel data (for example, from tetrodes),

* support for binary datasets and HDF5 files (support for other formats can be
  easily implemented),

* based on established scientific libraries: `NumPy`_, `PyTables`_,
  `matplotlib`_, `scikit-learn`_

License
-------

SpikeSort is free and `Open Source`_. Its liberal `license`_ (BSD) allows for
non-commercial and commercial use.


Contribute
----------

Found a bug? Have a good idea for improving SpikeSort?  Need help to
analyse your data? Head over to github page and create a new ticket or
fork. If you just want to chat with developers, send us an e-mail.

.. _Open Source: http://www.opensource.org/docs/osd

.. _license: https://github.com/btel/SpikeSort/blob/master/LICENSE

.. _Scholarpedia: http://www.scholarpedia.org/article/Spike_sorting

.. _NumPy: http://numpy.scipy.org/

.. _PyTables: http://www.pytables.org/moin

.. _matplotlib: http://matplotlib.sourceforge.net/

.. _scikit-learn: http://scikit-learn.org/stable/
