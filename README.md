# Mimicking  Program Aided language using a large language model
- The following program is designed to mimick program aided language(PAL) using the gemini-pro large language model
- using prompt engineering, the following progrma will

  - use a boiler plate prompt to solve **mathimatical questions** and return the python code
  - execute the python code to reach to the result using the python interpreter

**Note**: The program is specifically made to solve mathimatical problems

# steps
1. The program installs and imports   the required libraries
```python
! pip install -q --upgrade google-generativeai
```
```python
import google.generativeai as genai
from google.colab import userdata
from IPython.display import Markdown
import textwrap
import os
GOOGLE_API_KEY=userdata.get('GOOGLE_API_KEY')
genai.configure(api_key=GOOGLE_API_KEY)
model = genai.GenerativeModel('gemini-1.5-pro') 
```

2. Prompt engineering is used to create a prompt that contains example questions and their corresponding python code.the prompt also makes sure only a python script is returned from the language model

3. the python code is executed using the python interpreter to get the result


