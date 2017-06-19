# Bropy
A lightweight bro log reader for python.

## Installation
Installation using pip:
```
pip install bropy
```
Clone repository:
```
git clone https://github.com/Thijsvanede/bropy.git
```

## Usage
Use bropy as an iterator:
```
from bropy.bro_log_reader import BroLogReader

reader = BroLogReader()
for row in reader.read_logs('<path_to_file>'):
    # Do your stuff per row
```

It is also possible to load a bro log into a pandas dataframe:
```
import pandas as pd
from bropy.bro_log_reader import BroLogReader

reader = BroLogReader()
df = pd.DataFrame(reader.read_logs('<path_to_file>'))
```