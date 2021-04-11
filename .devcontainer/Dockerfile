FROM python

RUN apt upgrade
RUN apt update
RUN pip install --upgrade pip

RUN apt-get install -y --no-install-recommends \
       apt-utils \
       build-essential \
       curl \
       xvfb \
       ffmpeg \
       xorg-dev \
       libsdl2-dev \
       swig \
       cmake \
       python-opengl

RUN apt-get install -y xvfb x11-utils
RUN pip install gym[box2d]==0.17.* pyvirtualdisplay==0.2.* PyOpenGL==3.1.* PyOpenGL-accelerate==3.1.*

ADD ./.devcontainer/pip-requirements.txt /tmp/
RUN pip install -r /tmp/pip-requirements.txt
RUN rm /tmp/pip-requirements.txt