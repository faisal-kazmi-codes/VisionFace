```shell
$ pip install deepface
```

Alternatively, you can also install deepface from its source code. Source code may have new features not published in pip release yet.

```shell

$ pip install -e .
```

Once you installed the library, then you will be able to import it and use its functionalities.

```python
from deepface import DeepFace
```


```python
models = [
  "VGG-Face", 
  "Facenet", 
  "Facenet512", 
  "OpenFace", 
  "DeepFace", 
  "DeepID", 
  "ArcFace", 
  "Dlib", 
  "SFace",
  "GhostFaceNet",
]

#face verification
result = DeepFace.verify(
  img1_path = "img1.jpg",
  img2_path = "img2.jpg",
  model_name = models[0],
)

#face recognition
dfs = DeepFace.find(
  img_path = "img1.jpg",
  db_path = "C:/workspace/my_db", 
  model_name = models[1],
)

#embeddings
embedding_objs = DeepFace.represent(
  img_path = "img.jpg",
  model_name = models[2],
)
```

| Model          | Measured Score | Declared Score     |
| -------------- | -------------- | ------------------ |
| Facenet512     | 98.4%          | 99.6%              |
| Human-beings   | 97.5%          | 97.5%              |
| Facenet        | 97.4%          | 99.2%              |
| Dlib           | 96.8%          | 99.3 %             |
| VGG-Face       | 96.7%          | 98.9%              |
| ArcFace        | 96.7%          | 99.5%              |
| GhostFaceNet   | 93.3%          | 99.7%              |
| SFace          | 93.0%          | 99.5%              |
| OpenFace       | 78.7%          | 92.9%              |
| DeepFace       | 69.0%          | 97.3%              |
| DeepID         | 66.5%          | 97.4%              |
