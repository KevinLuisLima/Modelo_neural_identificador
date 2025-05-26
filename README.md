# Modelo_neural_identificador

## O que é
  Este é um repositório feito para comportar um modelo neural simples que recebe imagens e as categoriza baseado em padrões que ele identifica das imagens de seu dataset. O modelo vem pré-pronto com comentários e exemplificado com um código para identificar se uma imagem de sala de aula contém pessoas nela ou não.
  
## Como fazer funcionar
- Basta adicionar a sua pasta com imagens para a variável "data_dir" que você queira treinar (de preferência imagens PNG e não corrompidas, o código não tem tratamento de imagens corrompidas no momento);
- As imagens devem ser separadas em pastas, que serão tratadas como "classes". Todas as pastas devem compartilhar da mesma pasta root, e o "path" adicionado deve ser desta pasta root que contenha todas as classes para análise;
- Por fim, salve o modelo adicionando o path onde você queira salvá-lo para ser gerado o seu modelo neural .keras para que seja utilizado posteriormente em suas aplicações;
- Caso o modelo fique muito pesado para ser rodado ou você queira otimizar o resultado aumentando a resolução das imagens por exemplo, considere modificar os parâmetros que serão listados a seguir.

## Variáveis modificáveis do código
- batch_size: Seta o número de exemplos de treinamento usados em uma única iteração do algoritmo de treinamento;
- img_height: Altura em pixels que as imagens serão reescaladas;
- img_width: Largura em pixels que as imagens serão reescaladas;
- seed: Controla a aleatoriedade da escolha das imagens na separação entre treino e teste;
- validation_split: Dita a porcentagem de imagens que serão usadas para testar o modelo e quantas serão para validação. Aceita valores entre 0.99 e 0, e quanto maior, mais imagens serão usadas para validação e menos para teste. O código usa como base 80% para testes, 20% para validação (é importante pontuar que existem 2 validation_split: um para train_ds e outro para val_ds);
- model: Nele você pode modificar a estrutura da CNN, para aplicações mais avançadas. Não recomendo modificar seus parâmetros sem saber o que está acontecendo;
- epochs: Determina quantas vezes o modelo irá treinar para tentar melhorar seu resultado. A cada época, o próprio modelo altera os próprios parâmetros para testar uma acurácia maior;
