FROM auroai/cyber:v5.0.0
# RUN apt update && \
#     apt-get install -y gedit  iputils-ping net-tools && \
#     apt install -y python-pip && \
#     pip install --upgrade pip
# RUN python -m pip install numpy \
#             opencv-python==4.2.0.32 \
#             protobuf \
#             pygame \
#             pyproj \
#             pyyaml \
#             scipy \
#     -i https://mirrors.aliyun.com/pypi/simple/

RUN echo "source /apollo/cyber/setup.bash" >> ~/.bashrc
RUN echo "CARLA_PYTHON_ROOT=~/carla_apollo_bridge_13/carla-python-0.9.13" >> ~/.bashrc
RUN echo "PYTHONPATH=$PYTHONPATH:/apollo/py_proto/" >> ~/.bashrc
RUN echo "PYTHONPATH=$PYTHONPATH:$CARLA_PYTHON_ROOT/carla:$CARLA_PYTHON_ROOT/carla/dist/carla-0.9.13-py2.7-linux-x86_64.egg" >> ~/.bashrc


ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES all
ENV SDL_VIDEO_GL_DRIVER = libGL.so.1.7.0  #libGL.so.1
ENV DISPLAY=$DISPLAY
ENV LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/usr/lib/nvidia"
ENV  __NV_PRIME_RENDER_OFFLOAD=1
ENV __GLX_VENDOR_LIBRARY_NAME=nvidia