FROM tensorflow/tensorflow:latest-py3-jupyter

COPY requirements.txt /ml-powered-applications/requirements.txt
WORKDIR /ml-powered-applications

RUN pip install -r requirements.txt

RUN \
  python -m spacy download en_core_web_sm && \
  python -m spacy download en_core_web_lg

RUN python -c "import nltk; nltk.download('punkt')"

