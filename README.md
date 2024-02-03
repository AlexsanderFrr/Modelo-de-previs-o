# Modelo-de-previs-o
Arquivo JSON de teste de um conjunto de dados históricos de aluguel de bicicletas para treinar um modelo. O modelo prevê o número de alugueres de bicicletas esperados num determinado dia, com base em características sazonais e meteorológicas .

Todo o conteudo presente neste repositório segue as diretrizes presente na documentação oficial da microsoft. 

Acesse pelo link
[Explore o Machine Learning Automatizado no Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)

Neste exercício, será usado o recurso de aprendizado de máquina automatizado no Azure Machine Learning para treinar e avaliar um modelo de aprendizado de máquina. Em seguida, você implantará e testará o modelo treinado.

### Primeiro
Após seguir todo o passo a passo pela documentação oficial aa aba métricas como indicado na imagem abaixo para visualização dos gráficos 
![alt text](image.png)

### Segundo

Na aba clique na aba Modelo → Implantar → Serviço Web
![alt text](image-1.png)

Em seguida aparecerá a aba de preenchimento e preencha com os eguintes dados da imagem abaixo
![alt text](image-2.png)

após finalizado a etapa anterior, vá na aba lateral em pontos de extremidade e clique no arquivo prever-alugueis
![alt text](image-3.png)

clique na aba Testar e aqui você verá um código JSON
![alt text](image-4.png)

Troque o código pelo fornecido abaixo e teste

```
 {
   "Inputs": { 
     "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]    
   },   
   "GlobalParameters": 1.0
 }
```
O resultado deve ser algo semelhante ao da imagem abaixo
![alt text](image-5.png)