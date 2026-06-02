<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inscrição para a Convenção de Tecnologia de Alagoas!</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <form action="https://httpbin.org/post" method="post" enctype="multipart/form-data">

        <input type="hidden" name="edicao" value="2026">

        <h1>Convenção de Tecnologia de Alagoas</h1>
        <p class="subtitulo">Formulário de Inscrição</p>

        <fieldset>
            <legend>Identificação do Participante</legend>

            <div class="campo-grupo">
                <label for="nome">Nome Completo</label>
                <input type="text" id="nome" name="nome" required>
            </div>

            <div class="campo-grupo">
                <label for="email">E-mail Profissional</label>
                <input type="email" id="email" name="email" required>
            </div>

            <div class="campo-grupo">
                <label for="cidade">Cidade de Origem</label>
                <input type="text" id="cidade" name="cidade" list="cidades-al">

                <datalist id="cidades-al">
                    <option value="Maceió">
                    <option value="Marechal Deodoro">
                    <option value="Rio Largo">
                    <option value="Arapiraca">
                    <option value="Palmeira dos Índios">
                    <option value="Penedo">
                    <option value="Coruripe">
                    <option value="Viçosa">
                </datalist>
            </div>

            <div class="campo-grupo">
                <label for="foto">Foto para crachá</label>
                <input type="file" id="foto" name="foto"
                    accept="image/jpeg,image/png"
                    aria-describedby="foto-help">

                <small id="foto-help">
                    Formatos aceitos: JPG e PNG. Tamanho máximo: 2 MB.
                </small>
            </div>
        </fieldset>

        <fieldset>
            <legend>Preferências para o Evento</legend>

            <div class="campo-grupo">
                <label for="chegada">Data e hora preferida para chegada</label>
                <input type="datetime-local" id="chegada" name="chegada">
            </div>

            <div class="campo-grupo">
                <label for="experiencia">
                    Nível de experiência em programação:
                    <span id="valor-experiencia">5</span>/10
                </label>

                <input type="range"
                    id="experiencia"
                    name="experiencia"
                    min="0"
                    max="10"
                    step="1"
                    value="5"
                    oninput="document.getElementById('valor-experiencia').textContent = this.value">
            </div>

            <div class="campo-grupo">
                <label for="cor_camiseta">Cor de preferência para a camiseta</label>
                <input type="color" id="cor_camiseta" name="cor_camiseta" value="#1a73e8">
            </div>

            <div class="campo-grupo">
                <label for="oficinas">Áreas de Especialidade</label>

                <select id="oficinas" name="oficinas[]" multiple size="4"
                    aria-describedby="oficinas-help">

                    <option value="web">Desenvolvimento Web com React</option>
                    <option value="python">Data Science com Python</option>
                    <option value="iot">Introdução a IoT e Arduino</option>
                    <option value="seg">Cibersegurança Prática</option>
                    <option value="ux">Design de Interface (UX/UI)</option>
                </select>

                <small id="oficinas-help">
                    Use Ctrl (ou Cmd no Mac) para selecionar mais de uma oficina.
                </small>
            </div>
        </fieldset>

        <button type="submit">Confirmar inscrição</button>

    </form>

    <div class="footer">
        <p><b>Feito por Murilo Marques & Emanuel Magno</b></p>
    </div>

</body>
</html>
