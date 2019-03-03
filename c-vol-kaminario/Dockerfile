# Copyright 2019 Kaminario Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM registry.access.redhat.com/rhosp13/openstack-cinder-volume:latest

MAINTAINER Kaminario
LABEL name="rhosp13/openstack-cinder-volume-kaminario"
LABEL vendor="Kaminario"
LABEL version="3.1"
LABEL summary="cinder-volume image pre-installed with krest"
LABEL description="openstack cinder volume docker image with Kaminario's krest dependency pre-installed"
#LABEL release="latest"

# switch to root to install packages
USER root

# install packages
RUN curl "https://bootstrap.pypa.io/get-pip.py" -o "/tmp/get-pip.py"
RUN python /tmp/get-pip.py
RUN pip install krest

# switch the container back to the default user
USER cinder

