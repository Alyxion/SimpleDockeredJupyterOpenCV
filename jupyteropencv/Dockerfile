FROM jjanzic/docker-python3-opencv@sha256:4d62a19be279775d9b8938cd097530e1b7102ce50445df0b26d19590a9fea90b as baseimage
COPY requirements.txt requirements.txt
RUN apt-get update -y
RUN apt install libgl1-mesa-glx -y
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

FROM baseimage as jupyteropencv
EXPOSE 5005:5005
WORKDIR /projects
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=5005", "--allow-root"]
# If you prefer Jupyter Notebook feel free to comment the line above and uncomment the one below:
# CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=5005", "--allow-root"]