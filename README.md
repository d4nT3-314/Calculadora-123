from zipfile import ZipFile

import os



# Criando estrutura básica de um site com HTML, CSS e JS (opcional)

index_html = """

<!DOCTYPE html>

<html lang="pt-BR">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Calculadora de Conceito</title>

    <style>

        body { font-family: Arial, sans-serif; padding: 2rem; background: #f2f2f2; }

        h1 { color: #333; }

        .resultado { margin-top: 1rem; padding: 1rem; background: #fff; border-radius: 8px; }

    </style>

</head>

<body>

    <h1>Calculadora de Conceito</h1>

    <p>Este é um exemplo de site simples com HTML para você hospedar no GitHub Pages.</p>

    <div class="resultado">

        <p><strong>Seu conceito:</strong> Excelente</p>

        <p><strong>Média:</strong> 9.0</p>

    </div>

</body>

</html>

"""



# Criar o arquivo index.html

os.makedirs("/mnt/data/site_exemplo", exist_ok=True)

with open("/mnt/data/site_exemplo/index.html", "w", encoding="utf-8") as f:

    f.write(index_html)



# Gerar o ZIP

zip_path = "/mnt/data/site_exemplo.zip"

with ZipFile(zip_path, "w") as zipf:

    zipf.write("/mnt/data/site_exemplo/index.html", arcname="index.html")



zip_path
