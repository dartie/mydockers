FROM alpine
WORKDIR /home/

# Install system requirements (# github-cli)
RUN apk add python3 py3-pip git  

# Install python requirements
RUN pip install mkdocs mkdocs-material pymdown-extensions

# configure mkdocs
RUN mkdocs new mkdocs-Notebook

RUN git clone https://github.com/dartie/knowledge-base

COPY ./mkdocs.yml /home/mkdocs-Notebook

WORKDIR /home/mkdocs-Notebook
EXPOSE 9001

# run the application
# Start development server by default
ENTRYPOINT ["mkdocs"]
CMD ["serve", "--dev-addr=0.0.0.0:9001"]

