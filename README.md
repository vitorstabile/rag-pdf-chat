## Install dependencies

First, install the Ollama in Your Machine

- Go to https://ollama.com/download
- Choose your Operating System

After installed, make open your cmd and make pull of this two images
- ```ollama run mistral```
- ```ollama pull nomic-embed-text```

Now, install the requirements.

OBS:
- Do the following before installing the dependencies found in ```requirements.txt``` file because of current challenges installing ```onnxruntime``` through ```pip install onnxruntime```.
  - For MacOS users, a workaround is to first install ```onnxruntime``` dependency for ```chromadb``` using:

```
 conda install onnxruntime -c conda-forge
```

  - For Windows users, follow the guide [here](https://github.com/bycloudai/InstallVSBuildToolsWindows?tab=readme-ov-file) to install the Microsoft C++ Build Tools. Be sure to follow through to the last step to set the enviroment variable path.

- Now run this command to install dependenies in the ```requirements.txt``` file.

```
pip install -r requirements.txt
```

## Create Your Database

- Put your PDF inside of data/ folder
- Run the script ```python populate_database.py```

## Query the database

- Run the script ```python query_data.py "Act as a PDF extractor information for the product NOMOLT 150. Export in CSV format, separated by ; the table INSTRUCOES DE USO. Convert the table in flat format"```

## Test the output

Validate the RAG output in the script ```test_rag.py```

## References

https://github.com/pixegami/rag-tutorial-v2

https://medium.com/data-science/local-rag-from-scratch-3afc6d3dea08

https://www.youtube.com/watch?v=2TJxpyO3ei4

