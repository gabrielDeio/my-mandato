# Mandato

Jogo de gestão urbana e decisões políticas, em português. Uma cidade fictícia evolui conforme políticas econômicas, sociais e ambientais e as construções escolhidas pelo jogador.

## Executar

Sem dependências ou etapa de compilação. Sirva a pasta `dist` com um servidor HTTP:

```sh
python3 -m http.server 4173 --directory dist
```

Abra http://localhost:4173. O progresso fica no localStorage deste navegador. Fontes externas são opcionais; a interface usa fontes locais como alternativa.

## Jogabilidade

- 16 pautas por mandato, cada uma com três políticas e efeitos persistentes.
- 48 meses por mandato; eleição com 50% de aprovação, reeleição e continuidade da cidade.
- Dois eixos de orientação dinâmica: economia solidária/de mercado e expansão/preservação.
- 10 construções com custos, manutenção, empregos e capacidade habitacional. Desbloqueios dependem de população, políticas ou orientação econômica.
- Até três obras por mês, colocação direta no mapa ou construção automática acessível por teclado.
- Orçamento, migração, emprego, pressão sobre serviços, desigualdade, grupos de apoio e eventos condicionados à cidade.
- Políticas podem gerar déficit; obras exigem saldo. Caixa inferior a −R$ 160 mil ao fechar um mês provoca intervenção.
- Mapa isométrico desenhado em Canvas, filtros, zoom, histórico, ajuda, salvamento e avanço automático pausado nas decisões.

Os efeitos são simplificações ficcionais para o jogo e não previsões de políticas públicas reais.

## Testes

Node.js 22 ou superior:

```sh
npm test
```

`dist/engine.mjs` contém a simulação independente da interface; `dist/city.mjs`, o desenho do mapa; `dist/app.mjs`, a interação e o salvamento. O artefato servido é a pasta `dist`.
