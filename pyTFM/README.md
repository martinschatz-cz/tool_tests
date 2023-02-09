# pyTFM test
 * package [https://github.com/fabrylab/pyTFM](https://github.com/fabrylab/pyTFM)
 * documentation [https://pytfm.readthedocs.io/en/latest/installation.html](https://pytfm.readthedocs.io/en/latest/installation.html)

## env creation
```
conda create --name pyTFM python=3.8.5
conda activate pyTFM
```

package install
```
pip install git+https://github.com/fabrylab/pyTFM.git
conda install jupyterlab jupyterlab_code_formatter black isort -c conda-forge
#conda install numpy==1.19.5
```

clickpoint activation
```
clickpoints register
```

## Error - create issue
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
Cell In[1], line 1
----> 1 from pyTFM.TFM_functions import calculate_deformation
      2 from pyTFM.plotting import show_quiver

File ~\Anaconda3\envs\pyTFM\lib\site-packages\pyTFM\TFM_functions.py:4
      2 import matplotlib.pyplot as plt
      3 import numpy as np
----> 4 import openpiv.filters
      5 import scipy.fft
      7 from openpiv.pyprocess import extended_search_area_piv

File ~\Anaconda3\envs\pyTFM\lib\site-packages\openpiv\filters.py:20
      1 """The openpiv.filters module contains some filtering/smoothing routines."""
      3 __licence_ = """
      4 Copyright (C) 2011  www.openpiv.net
      5 
   (...)
     17 along with this program.  If not, see <http://www.gnu.org/licenses/>.
     18 """
---> 20 from openpiv.lib import replace_nans
     21 import numpy as np
     22 from scipy.signal import convolve

File ~\Anaconda3\envs\pyTFM\lib\site-packages\openpiv\lib.pyx:7, in init openpiv.lib()

File ~\Anaconda3\envs\pyTFM\lib\site-packages\numpy\__init__.py:305, in __getattr__(attr)
    300     warnings.warn(
    301         f"In the future `np.{attr}` will be defined as the "
    302         "corresponding NumPy scalar.", FutureWarning, stacklevel=2)
    304 if attr in __former_attrs__:
--> 305     raise AttributeError(__former_attrs__[attr])
    307 # Importing Tester requires importing all of UnitTest which is not a
    308 # cheap import Since it is mainly used in test suits, we lazy import it
    309 # here to save on the order of 10 ms of import time for most users
    310 #
    311 # The previous way Tester was imported also had a side effect of adding
    312 # the full `numpy.testing` namespace
    313 if attr == 'testing':

AttributeError: module 'numpy' has no attribute 'float'.
`np.float` was a deprecated alias for the builtin `float`. To avoid this error in existing code, use `float` by itself. Doing this will not modify any behavior and is safe. If you specifically wanted the numpy scalar type, use `np.float64` here.
The aliases was originally deprecated in NumPy 1.20; for more details and guidance see the original release note at:
    https://numpy.org/devdocs/release/1.20.0-notes.html#deprecations
