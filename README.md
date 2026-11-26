# ЭлектроАтлас MCP

![ЭлектроАтлас MCP](assets/cover.png)

Сравните электромобили и гибриды в России. Проверьте цены в рублях, паспортный и зимний запас хода, продажи, дилеров и сборы при ввозе. Ответы на русском со ссылками на источники и страницы каталога.

- **MCP** `https://electroatlas.ru/mcp` (Streamable HTTP). Без входа и ключа. Только чтение.
- **MCP Registry** `ru.electroatlas/catalog` · `1.5.0`
- **Навыки** [`electroatlas`](skills/electroatlas/SKILL.md)

## Инструменты

| Инструмент | Назначение |
| --- | --- |
| `search` | Поиск по сайту |
| `fetch` | Страница сайта целиком |
| `search_models` | Поиск электромобилей |
| `get_model` | Карточка модели |
| `compare_models` | Сравнение двух моделей |
| `get_sales` | Продажи по моделям |
| `find_dealers` | Где купить: дилеры по городам |
| `list_regulations` | Регуляторика РФ |
| `get_regulation` | Регуляция целиком |
| `calc_import_fees` | Утильсбор и растаможка |
| `get_ranking` | Рейтинг и части балла |
| `get_changes` | Изменения цен, моделей и законов |
| `pick_car` | Подбор машины под поездки |
| `calc_ownership` | Годовые расходы и цена зарядки |

## Установка в одно нажатие

[Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=%D0%AD%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%90%D1%82%D0%BB%D0%B0%D1%81&connectorUrl=https%3A%2F%2Felectroatlas.ru%2Fmcp) · [Cursor](https://cursor.com/install-mcp?name=electroatlas&config=eyJ1cmwiOiJodHRwczovL2VsZWN0cm9hdGxhcy5ydS9tY3AifQ%3D%3D) · [VS Code](https://vscode.dev/redirect?url=vscode%3Amcp%2Finstall%3F%257B%2522name%2522%253A%2522electroatlas%2522%252C%2522type%2522%253A%2522http%2522%252C%2522url%2522%253A%2522https%253A%252F%252Felectroatlas.ru%252Fmcp%2522%257D) · [Kiro](https://kiro.dev/launch/mcp/add?name=electroatlas&config=%7B%22url%22%3A%22https%3A%2F%2Felectroatlas.ru%2Fmcp%22%7D) · [Goose](goose://extension?url=https%3A%2F%2Felectroatlas.ru%2Fmcp&type=streamable_http&timeout=300&id=electroatlas&name=%D0%AD%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%90%D1%82%D0%BB%D0%B0%D1%81&description=Compare%20EVs%20in%20Russia%20by%20rouble%20price%20and%20winter%20range.%20Look%20up%20dealers%2C%20sales%20and%20import%20rules.) · [Qoder](qoder://aicoding.aicoding-deeplink/mcp/add?name=electroatlas&config=JTdCJTIydXJsJTIyJTNBJTIyaHR0cHMlM0ElMkYlMkZlbGVjdHJvYXRsYXMucnUlMkZtY3AlMjIlN0Q%3D) · [Replit](https://replit.com/integrations?mcp=eyJkaXNwbGF5TmFtZSI6ItCt0LvQtdC60YLRgNC%2B0JDRgtC70LDRgSIsImJhc2VVcmwiOiJodHRwczovL2VsZWN0cm9hdGxhcy5ydS9tY3AifQ%3D%3D) · [LM Studio](lmstudio://add_mcp?name=electroatlas&config=eyJ1cmwiOiJodHRwczovL2VsZWN0cm9hdGxhcy5ydS9tY3AifQ%3D%3D)

GitHub скрывает ссылки на приложения. Скопируйте ссылку в адресную строку браузера:

- Goose - `goose://extension?url=https%3A%2F%2Felectroatlas.ru%2Fmcp&type=streamable_http&timeout=300&id=electroatlas&name=%D0%AD%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%90%D1%82%D0%BB%D0%B0%D1%81&description=Compare%20EVs%20in%20Russia%20by%20rouble%20price%20and%20winter%20range.%20Look%20up%20dealers%2C%20sales%20and%20import%20rules.`
- Qoder - `qoder://aicoding.aicoding-deeplink/mcp/add?name=electroatlas&config=JTdCJTIydXJsJTIyJTNBJTIyaHR0cHMlM0ElMkYlMkZlbGVjdHJvYXRsYXMucnUlMkZtY3AlMjIlN0Q%3D`
- LM Studio - `lmstudio://add_mcp?name=electroatlas&config=eyJ1cmwiOiJodHRwczovL2VsZWN0cm9hdGxhcy5ydS9tY3AifQ%3D%3D`

[Ссылки для сайтов](install-links.json)

```sh
claude mcp add --transport http electroatlas https://electroatlas.ru/mcp
claude plugin install electroatlas --marketplace electroatlas/mcp
codex mcp add electroatlas --url https://electroatlas.ru/mcp
agy plugin install https://github.com/electroatlas/mcp/tree/main/antigravity/electroatlas
gemini extensions install https://github.com/electroatlas/mcp
```

## Форматы пакета

| Клиент | Файл |
| --- | --- |
| Claude | [marketplace.json](.claude-plugin/marketplace.json) |
| ChatGPT / Codex | [plugin.json](openai/electroatlas/plugin.json) · [marketplace.json](.agents/plugins/marketplace.json) |
| Antigravity | [plugin.json](antigravity/electroatlas/plugin.json) |
| Gemini CLI | [gemini-extension.json](gemini-extension.json) · [Навыки](skills/) |
| Cursor | [plugin.json](.cursor-plugin/plugin.json) |
| Kiro | [POWER.md](kiro/electroatlas/POWER.md) |
| Kilo | [MCP.yaml](MCP.yaml) |
| Cline | [entry.json](entry.json) · [llms-install.md](llms-install.md) |
| Devin | [plugin.json](devin/electroatlas/.devin-plugin/plugin.json) |
| Agent Plugins | [plugin.json](plugin.json) |
| MCP Registry | [server.json](server.json) |

## Примеры вопросов

- Сколько проезжает зимой Москвич 3е и откуда эта цифра?
- Сравни Zeekr 001 и Li Auto L7 по цене и запасу хода.
- Где купить Voyah Free в Казани?

## Условия

- [Условия](https://electroatlas.ru/legal/terms)
- [Конфиденциальность](https://electroatlas.ru/legal/privacy)
- Поддержка: info@electroatlas.ru
- [MIT](LICENSE) · [Changelog](CHANGELOG.md)
