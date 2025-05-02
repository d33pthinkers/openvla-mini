ARG BASE_IMAGE=oawejkbnwroerjewovrimewjorajiebolrajieowihjewnoaltrrievt
FROM $BASE_IMAGE
ENV PYTHONPATH=$PYTHONPATH:/src
RUN apt-get update && apt-get install -y libgl1 libglib2.0-0

RUN pip install uv

#region TODO move to requirements file or poetry
RUN uv pip install --system \
"timm==0.9.10" \
"tokenizers==0.19.1"  \
"torch>=2.2.0" \
"torchvision>=0.16.0" \
"transformers==4.40.1" \
"pandas" \
"joblib" \
"accelerate>=0.25.0" \
"draccus==0.8.0" \
"einops" \
"huggingface_hub" \
"json-numpy" \
"jsonlines" \
"matplotlib" \
"peft==0.11.1" \
"protobuf" \
"rich" \
"sentencepiece==0.1.99" \
"timm==0.9.10" \
"tokenizers==0.19.1" \
"torch==2.2.0" \
"torchvision==0.17.0" \
"torchaudio==2.2.0" \
"transformers==4.40.1" \
"tensorflow==2.15.0" \
"tensorflow_datasets==4.9.3" \
"tensorflow_graphics==2021.12.3"
RUN python -m pip install jupyterlab==4.1.4 notebook

RUN pip install flash-attn --no-build-isolation
RUN pip install -U sageattention==1.0.6
RUN pip install -U triton

RUN apt-get  install -y git
RUN pip install  "dlimp@git+https://github.com/moojink/dlimp_openvla"
#endregion TODO move to requirements file
CMD python -m jupyter lab --ip=0.0.0.0 --no-browser --allow-root --port=${JUPYTERLAB_PORT:-8888}