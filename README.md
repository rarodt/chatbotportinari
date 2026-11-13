# Chatbot Escola Portinari 2027

## Arquivos
- index.html — chatbot (abrir em qualquer navegador/hospedagem estática)
- Code.gs — script do Google Apps Script
- README.md — este arquivo

## Instalação

1. Crie uma planilha Google chamada "Leads Portinari 2027".
2. Extensões > Apps Script.
3. Apague o conteúdo padrão e cole o código de Code.gs.
4. Salve o projeto.
5. Implantar > Nova implantação > tipo "Aplicativo da Web".
   - Executar como: Eu (sua conta)
   - Quem pode acessar: Qualquer pessoa
6. Copie a URL que termina em /exec (já está configurada no index.html enviado).
7. Publique o index.html em uma hospedagem estática gratuita (ex.: GitHub Pages).

## Teste obrigatório antes de divulgar

1. Abra o index.html publicado.
2. Clique em "Solicitar uma visita".
3. Preencha todos os campos com dados de teste.
4. Envie.
5. Abra a planilha "Leads Portinari 2027" > aba "Leads 2027".
6. Confirme que uma nova linha apareceu com os dados enviados.
7. Repita o teste em um celular (Android e iPhone, se possível).

Se a linha não aparecer:
- Verifique se a implantação do Apps Script está como "Qualquer pessoa" tem acesso.
- Verifique se a URL em index.html corresponde exatamente à URL /exec gerada.
- Veja o log de execuções em Apps Script > Execuções, para identificar erros.

## Manutenção
- Para alterar textos do chatbot, edite as funções em index.html (school, grades, pedagogy, etc).
- Para alterar o WhatsApp, troque o valor WHATSAPP no objeto CONFIG.
- Nunca remova o campo "website" (honeypot) nem o checkbox de consentimento — protegem contra spam e atendem à LGPD.

## Limites conhecidos
- O envio usa modo "no-cors": o chatbot assume sucesso ao enviar, mas não recebe confirmação real do servidor. Por isso o teste manual na planilha é essencial.
- Sem custos recorrentes: toda a solução usa apenas Google Sheets, Apps Script e hospedagem estática gratuita.
