FROM waleedka/modern-deep-learning
WORKDIR /Mask_RCNN
COPY assets assets
COPY mrcnn mrcnn
COPY requirements.txt requirements.txt
COPY samples samples
COPY setup.cfg setup.cfg
COPY setup.py setup.py
RUN python3 setup.py install
WORKDIR /
RUN git clone https://github.com/waleedka/coco.git
WORKDIR /coco/PythonAPI
RUN python3 -m pip install --upgrade cython
RUN python3 setup.py build_ext install