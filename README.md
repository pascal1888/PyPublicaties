# PyPublicaties

`PyPublicaties` is a Python library that facilitates easy access to the 'officielepublicaties' collection through the [SRU 2.0 interface provided by the Dutch government](https://data.overheid.nl/sites/default/files/dataset/d0cca537-44ea-48cf-9880-fa21e1a7058f/resources/Handleiding%2BSRU%2B2.0.pdf). This library simplifies the process of querying, retrieving, and managing official publications with just a few lines of code.

## Features

- Easy construction of queries for searching within the 'officielepublicaties' collection.
- Retrieval of publications with options to limit the number of records.
- Direct access to publication details such as identifiers and titles in a Python-friendly way.

## Installation

Install `PyPublicaties` using pip:

```bash
pip install PyPublicaties
````

## Quick Start


Here's a simple example to get you started with PyPublicaties:
```python
from PyPublicaties import retrieve_publications

query_dict = {
    'w.subrubriek': 'Stemmingen'
}

publications = retrieve_publications(query_dict=query_dict, max_records=100, start_record=1)

for publication in publications:
    print(publication)
```

This code will search for publications under the 'Stemmingen' subcategory and print details for up to 100 of them. The function always returns a list of objects

This allows for easy interaction in an object oriented way. For example, this code will access the title of the first retrieved result:

````python
publications[0].title
````


## Documentation

For more detailed information on all the capabilities, documentation will be made available in a later stadium.

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and submit a pull request with your changes.

## Support

If you encounter any issues or have questions, please submit an issue on the GitHub issues page.

## License

PyPublicaties is released under the MIT License. See the LICENSE file for more details.