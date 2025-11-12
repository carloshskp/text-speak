# Leitor de Texto 🎙️

Um aplicativo web moderno e responsivo que converte texto em fala, permitindo que os usuários ouçam qualquer texto em voz alta com controle total sobre velocidade de reprodução.

## ✨ Características

- **Leitura de Texto em Voz Alta**: Converte qualquer texto em áudio usando a API Web Speech nativa do navegador
- **Controle de Velocidade**: Ajuste a velocidade de reprodução de 0.5x a 2.0x para sua conveniência
- **Interface Moderna**: Design limpo e responsivo com gradiente visual atraente
- **Persistência de Dados**: Salve o texto no navegador para acessá-lo depois
- **Pausa e Reprodução**: Controle total sobre a reprodução com botões intuitivos
- **Suporte a Português Brasileiro**: Detecção automática e seleção de vozes pt-BR quando disponível
- **Design Responsivo**: Funciona perfeitamente em desktop, tablet e dispositivos móveis

## 🚀 Como Usar

1. Abra a aplicação no navegador
2. Digite ou cole o texto que deseja ouvir no campo de texto
3. Clique no botão **Reproduzir** (▶) para iniciar a leitura
4. Use o controle deslizante para ajustar a velocidade de reprodução (0.5x a 2.0x)
5. Clique no botão **Pausar** (⏸) para pausar a reprodução
6. Clique no botão **Salvar** (💾) para guardar o texto no navegador

## 📋 Requisitos

- Navegador moderno com suporte à Web Speech API
- JavaScript habilitado
- Node.js 18+ (para executar a etapa local de build do Tailwind)
- Conexão de internet (para carregar as dependências de CDN de ícones e análise)

## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Estilos com suporte a backdrop-filter e gradientes
- **JavaScript**: Lógica de aplicação
- **Tailwind CSS**: Framework de CSS utilitário
- **Lucide Icons**: Ícones SVG modernos
- **Web Speech API**: Síntese de fala nativa do navegador

## 📦 Dependências

- [Tailwind CSS](https://tailwindcss.com/) - construído localmente a partir de `src/tailwind.css`
- [Lucide Icons](https://lucide.dev/) - via CDN

## 🛠️ Desenvolvimento local e build

1. Instale as dependências: `npm install`
2. Gere o bundle de CSS: `npm run build:css`
   - Esse comando executa `tailwindcss -i src/tailwind.css -o assets/tailwind.min.css --minify`
   - O arquivo gerado é versionado no repositório e deve ser reconstruído sempre que houver mudanças de classes ou configuração do Tailwind
3. Sirva o site localmente (ex.: `npx http-server` ou `python -m http.server`) e acesse `http://localhost:8000`
4. Valide visualmente a interface em resoluções desktop e mobile
5. Antes de publicar, rode novamente o comando de build para garantir que o CSS está atualizado

## 🚢 Fluxo de publicação

1. Execute `npm run build:css` para garantir que `assets/tailwind.min.css` está sincronizado com o código
2. Faça commit do CSS gerado junto com as demais alterações
3. Publique os arquivos estáticos (incluindo o bundle de CSS) no provedor de hospedagem ou no GitHub Pages
4. Após o deploy, repita o teste do PageSpeed Insights apontando para a URL de produção para confirmar a remoção do script CDN bloqueante do Tailwind

## 💾 Armazenamento Local

O aplicativo salva o texto no `localStorage` do navegador, permitindo que você recupere facilmente seu conteúdo em futuras visitas.

## 🎯 Vozes Disponíveis

O aplicativo tenta selecionar automaticamente uma voz em português brasileiro (pt-BR) se disponível no seu sistema. Se nenhuma voz pt-BR for encontrada, o navegador usará a voz padrão do sistema.

## 🌐 Navegadores Suportados

- ✅ Chrome/Chromium (versão 25+)
- ✅ Firefox (versão 49+)
- ✅ Safari (versão 14.1+)
- ✅ Edge (versão 79+)
- ⚠️ Opera (com suporte parcial)

## 📝 Notas

- A qualidade da voz depende das vozes disponíveis no seu sistema operacional
- Alguns navegadores podem ter limitações no comprimento do texto para síntese de fala
- A velocidade de reprodução pode variar dependendo do navegador e do sistema operacional

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👤 Autor

Carlos Henrique Bernardes

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias e correções de bugs.

## 💡 Dicas de Uso

- Use velocidades mais lentas (0.5x - 1.0x) para melhor compreensão
- Use velocidades mais rápidas (1.5x - 2.0x) para revisão rápida
- Salve textos frequentemente usados para acesso rápido
- Teste diferentes vozes do seu sistema para encontrar a que melhor se adequa

## 🐛 Solução de Problemas

### A voz não está funcionando
- Verifique se o JavaScript está habilitado no navegador
- Tente recarregar a página
- Certifique-se de que o navegador tem permissão para usar síntese de fala

### O botão Salvar está desabilitado
- O botão Salvar só fica habilitado após iniciar uma reprodução
- Verifique se há espaço disponível no armazenamento local do navegador

### Texto não é lido completamente
- Alguns navegadores têm limite de comprimento para síntese de fala
- Tente dividir o texto em partes menores

---

**Aproveite o Leitor de Texto! 🎉**
