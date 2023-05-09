FROM jupyter/datascience-notebook:latest

LABEL maintainer="@paolograniero"

# Copy requirements file
COPY requirements.txt /tmp/requirements.txt

# Install requirements
RUN pip install -r /tmp/requirements.txt

# Set user and working directory
USER jovyan
WORKDIR /home/jovyan/work

# Enable JupyterLab
ENV JUPYTER_ENABLE_LAB=yes

# Expose port
EXPOSE 8888

# Start JupyterLab
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
