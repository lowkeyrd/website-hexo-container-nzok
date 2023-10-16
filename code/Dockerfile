FROM registry.ap-southeast-1.aliyuncs.com/fc-demo/test:fengchongV1 AS gpu-1

WORKDIR /app

# ARG CI_COMMIT_SHA
# ARG DATETIME
# ARG PIPELINE_ID
# ARG BUILD_NUMBER
# ARG MODEL_URL
# ENV code_version=$CI_COMMIT_SHA
# ENV build_datetime=$DATETIME
# ENV build_pipeline_id=$PIPELINE_ID
# ENV build_id=$BUILD_NUMBER
# ENV model_url=$MODEL_URL

# ENV GPU_MEMORY_FRACTION=0.25
# ENV PYTHONPATH="${PYTHONPATH}:."
# ENV CUDA_VERSION=11
# ENV PROTOCOL_BUFFERS_PYTHON_IMPLEMENTATION='python'

COPY . .
CMD ["python","src/image_analysis_cuda11/recognition_category_model/recognition_server.py","--model_path","/app/models/model_data/category_recognition/category_recognition_v3.pth"]