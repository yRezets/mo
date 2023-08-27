# mo
<!DOCTYPE html>
<html>
<head>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 50px;
  }

  .question {
    font-size: 24px;
    margin-bottom: 20px;
  }

  .options {
    display: flex;
    justify-content: center;
    gap: 20px;
  }

  .option {
    font-size: 20px;
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 10px;
  }

  .no {
    background-color: #ff7f7f;
  }

  .yes {
    background-color: #9aff9a;
  }
</style>
</head>
<body>
  <div class="question">
    <p>Amorzao,</p>
    <p>uma semana nao da...</p>
    <p>Vamos no ver todos os dias</p>
  </div>

  <div class="options">
    <span class="option no" onclick="changePosition()">Não</span>
    <span class="option yes" onclick="showResponse()">Sim</span>
  </div>

  <div id="responseMessage" style="display: none;">
    <p>Estou muito feliz que você disse "Sim"! Te amo muito.</p>
  </div>

  <script>
    function changePosition() {
      var noButton = document.querySelector('.no');
      var yesButton = document.querySelector('.yes');
      var optionsDiv = document.querySelector('.options');

      optionsDiv.insertBefore(noButton, yesButton.nextSibling);
    }

    function showResponse() {
      var responseMessage = document.getElementById("responseMessage");
      var optionsDiv = document.querySelector('.options');

      responseMessage.style.display = 'block';
      optionsDiv.style.display = 'none';
    }
  </script>
</body>
</html>
