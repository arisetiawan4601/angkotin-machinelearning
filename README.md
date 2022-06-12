<br />
<div align="center">
  <h2 align="center">Angkotin Time arrival Estimation</h2>

  <p align="center">
    <a href="https://drive.google.com/file/d/1g99cnfBJQnD2_XSEWJUq70BUp7hcvrwL/view?usp=sharing">Dataset</a>
    ·
    <a href="https://drive.google.com/file/d/1FPtPXhlvmRRt_rytghnd22Qe_5_jR3FU/view?usp=sharing">Google Colab</a>
    ·
    <a href="https://hub.docker.com/repository/docker/arisetiawan4601/angkotin_container">Docker Hub</a>
  </p>
</div>

## Usage
Endpoint
```url
http://34.66.224.150:8501/v1/models/angkotin_model:predict
```


Body
```json
{"instances": 
[{"jalur":"AG","awal":120,"akhir":1110,"kecepatan":10,"cuaca":"HUJAN","jam":"16.00 - 18.00"}]
}
```

Example 
```sh
curl -d '{"instances": [{"jalur":"AG","awal":120,"akhir":1120,"kecepatan":10,"cuaca":"HUJAN","jam":"16.00 - 18.00"}]}' -X POST https://34.66.224.150:8501/v1/models/angkotin_model:predict
```

Return
```json
{
    "predictions": [[17.6728287]
    ]
}
```