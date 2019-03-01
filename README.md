# TensorflowSamples
basic example of tensorflow


# Retrain based on parameters.

python -m scripts.retrain \
  --bottleneck_dir=tf_bevrage_files/bottlenecks \
  --how_many_training_steps=500 \
  --model_dir=tf_bevrage_files/models/ \
  --summaries_dir=tf_bevrage_files/training_summaries/"${ARCHITECTURE}" \
  --output_graph=tf_bevrage_files/retrained_graph.pb \
  --output_labels=tf_bevrage_files/retrained_labels.txt \
  --architecture="${ARCHITECTURE}" \
  --image_dir=tf_bevrage_files/bevrage_photos



# Classification

python -m scripts.label_classification \
    --graph=tf_bevrage_files/retrained_graph.pb  \
    --image=tf_bevrage_files/bevrage_photos/sprite/093187.jpg
