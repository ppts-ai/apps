FROM jupyter/base-notebook:x86_64-python-3.11
RUN pip install spacy
RUN python -m spacy download en_core_web_sm
RUN pip install opencv-python