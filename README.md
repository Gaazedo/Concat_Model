# Reconhecimento e análise de doenças na pele com uso de machine learning

O melanoma é um câncer de pele agressivo e potencialmente fatal, cujo diagnóstico e tratamento precoces são essenciais. Contudo, a análise clínica das lesões cutâneas pode ser complexa, dificultando a detecção precoce. Nesse contexto, técnicas de processamento de imagens e redes neurais artificiais têm se mostrado promissoras no auxílio ao diagnóstico do melanoma. Este trabalho utiliza modelos de redes neurais para classificar imagens dermatológicas em sete categorias distintas de doenças de pele, demonstrando uma alta taxa de precisão.
Neste sentido, foi desenvolvida uma rede neural eficiente utilizando um modelo ResNet-50 pré-treinado para classificação de melanoma e empregando metadados através da concatenação de modelos para geração completa de imagens com descritores importantes para detecção precoce de câncer de pele, além da concatenação com um Rede Neural Convolucional, gerando assim um modelo com excelente desempenho e contribuindo para avanços na área médica.

##  Conjunto de Dados
Utilizamos os dados do conjunto de dados HAM10000, que consiste em 10.015 imagens dermatoscópicas que são lançadas como um conjunto de treinamento para fins de aprendizado de máquina acadêmico e estão disponíveis publicamente através do arquivo ISIC. Este conjunto de dados de referência pode ser usado para aprendizado de máquina e para comparações com especialistas humanos.

Composto por 7 classes diferentes de câncer de pele, listadas abaixo:  
**1. Nevos melanocíticos**   
**2. Melanoma**  
**3. Lesões benignas semelhantes à ceratose**  
**4. Carcinoma basocelular**  
**5. Queratoses actínicas**  
**6. Lesões vasculares**  
**7. Dermatofibroma**  

##  Arquitetura
Visando um melhor desempenho e acurácia, o modelo ResNet-50 se destaca pela sua capacidade de aprendizado, sua utilização como base demonstra vantagens em diversos pontos. Em primeiro lugar, a adição de camadas densas implementada no modelo demonstra uma maior capacidade de compartilhamento de dados entre os neurônios da rede e uma aptidão para resolução de problemas complexos, potencializando a detecção de doenças de pele de uma maneira mais precisa e revolucionando o diagnóstico de doenças de pele.
Na arquitetura CNN foram adicionadas camadas separadamente, sendo a primeira, uma divisão de filtros para a transformação de imagens, a segunda sendo voltada ao pooling para redução da resolução, a utilização de Dropout para redução de overfitting, uma camada Flatten para nivelamento e camadas densas.
Com a utilização destas duas arquiteturas há uma concatenação dos modelos através da biblioteca ‘fastai’ disponibilizada pelo PyTorch, realizando a junção da arquitetura CNN (modelo tabular) juntamente ao ResNet-50, tornando-se um modelo de avaliação de precisão na detecção e classificação das classes presentes.

![](https://github.com/Gaazedo/Reconhecimento-e-analise-de-doencas-na-pele-com-uso-de-machine-learning/blob/main/arquitetura_projeto.jpg?raw=true)
