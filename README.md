# Origem — Gestão de Cafés Especiais

Protótipo navegável para uma torrefação de cafés especiais. Interface em português brasileiro, adaptada a computador e celular.

## Executar

Não há dependências npm, compilação ou servidor de aplicação. Com Python 3 instalado, execute na raiz do repositório:

```sh
python -m http.server 8000 --directory dist
```

Abra http://localhost:8000 no navegador. No Windows, pode usar `py` no lugar de `python`. Um servidor estático equivalente também funciona.

## Arquivos

- `dist/index.html`: estrutura da interface e metadados.
- `dist/style.css`: estilos, responsividade e impressão.
- `dist/app.js`: telas, dados de exemplo e regras da demonstração.

A pasta `dist` contém o código-fonte editável, não arquivos gerados ou minificados. Para hospedagem estática, publique seu conteúdo. As fontes DM Sans e Manrope são carregadas do Google Fonts, com fontes alternativas quando indisponíveis.

## Funcionalidades

- Painel com vendas, estoque e pedidos.
- Cadastro de cafés, lotes, características sensoriais e qualidade.
- Estoque verde, torrado a granel e embalado, reservas e histórico.
- Torra com pesos reais, perda, rendimento e custo por kg.
- Embalagem em 250 g, 500 g e 1 kg.
- Pedidos, reserva, separação, expedição e cancelamento antes da saída.
- Clientes, histórico e abertura manual de conversa no WhatsApp.
- Compras recebidas, fornecedores e contas a pagar.
- Recebimentos parciais, despesas, fluxo de caixa e resultado gerencial simplificado.
- Impressão de pedidos e separação, exportação CSV e cópia JSON dos dados.

## Dados e limites

Esta é uma demonstração, não um SaaS pronto para uso financeiro em produção. Os exemplos são fictícios e as alterações ficam no `localStorage` do navegador, na chave `origem-demo-v1`. Não há sincronização entre dispositivos, banco de dados compartilhado, autenticação própria, isolamento entre empresas ou controle de concorrência entre usuários. O controle de acesso do site original não está incluído neste código estático.

Em Configurações, é possível baixar uma cópia JSON ou restaurar os exemplos. A restauração apaga as alterações locais. Não há importação de backup implementada. As vendas demonstrativas começam em setembro de 2026; selecione esse mês nos filtros para visualizá-las.

O resultado gerencial é simplificado e usa custos demonstrativos. Não substitui apuração contábil. Não há emissão fiscal, boletos, integração bancária, disparo automático de WhatsApp, devoluções, agendamento de torra ou suporte completo a parcelas e múltiplas contas.

## Fluxo para testar

1. Registre uma torra consumindo 10 kg verdes e obtendo 8 kg torrados.
2. Embale o lote em 32 pacotes de 250 g.
3. Confirme um pedido para reservar unidades.
4. Registre um recebimento parcial e confira o saldo pendente.
5. Expeça o pedido: a reserva se transforma em saída física sem baixa duplicada.

## Evolução para produção

Adicionar autenticação, banco de dados, transações de estoque no servidor, permissões, auditoria, backups e testes de concorrência antes de utilizar com operações reais.

Este repositório contém o código da aplicação. Credenciais, histórico Git do ambiente de criação e identificadores da hospedagem original não são necessários para executá-lo e não estão incluídos.
