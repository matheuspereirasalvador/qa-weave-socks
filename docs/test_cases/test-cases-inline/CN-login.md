# Cenário: Login

* CT-009: Login com dados válidos (positivo)

* CT-010: Login com dados que não pertencem a nenhuma conta (negativo)
* CT-011: Buscar dados pela API em busca de informações confidenciais (negativo)
* CT-012: Realizar login pela API e verificar se o retorno é válido (positivo)
* CT-013: Tentar logar 5 vezes errando somente a senha e na 6º vez logar dados corretos (negativo)
* CT-014: Tentar logar com a conta em status de confirmação de e-mail (negativo)
* CT-015: Verificar se o código de confirmação de e-mail foi recebido com sucesso (positivo)
* CT-016: Esperar 16 minutos e tentar confirmar o e-mail pelo código recebido (negativo)
* CT-017: Clicar no botão "Reenviar código" mais de uma vez em um intervalo de 60 segundos (negativo)
* CT-018: Tentar enviar o código incorreto 3 vezes e na 4º vez enviar o correto (negativo)
