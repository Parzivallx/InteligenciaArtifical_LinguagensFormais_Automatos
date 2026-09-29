# 🧪 10. Atividade prática no Regex Learn — 0,5 ponto

> 🔎 **Objetivo:** verificar, na prática, se a expressão regular desenvolvida para o desafio final atende corretamente a todas as regras da especificação.

---

## 🔤 Expressão utilizada

A expressão utilizada para o desafio final foi:

```text
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$
```

A expressão foi testada no **Regex Learn Playground** utilizando os exemplos válidos, inválidos e quatro novos casos de teste.

---

## 🧪 Registro dos testes

| **Entrada** | **Esperado** | **Obtido** | **Regra verificada** |
|:---|:---:|:---:|:---|
| `CCO-2024-0001-M` | ✅ aceita | ✅ aceita | Curso, limite inferior e formato |
| `ESW-2026-1042-N` | ✅ aceita | ✅ aceita | Formato geral |
| `SIS-2029-9999-T` | ✅ aceita | ✅ aceita | Curso, limite superior e formato |
| `CCO-2027-0100-N` | ✅ aceita | ✅ aceita | Formato geral |
| `ESW-2025-4321-M` | ✅ aceita | ✅ aceita | Formato geral |
| `SIS-2028-5678-M` | ✅ aceita | ✅ aceita | Formato geral |
| `CCO-2025-0042-T` | ✅ aceita | ✅ aceita | Formato geral |
| `ADS-2026-0001-N` | ❌ rejeita | ❌ rejeita | Curso |
| `CCO-2030-0001-M` | ❌ rejeita | ❌ rejeita | Ano |
| `SIS-2027-123-N` | ❌ rejeita | ❌ rejeita | Número com três algarismos |
| `esw-2026-1042-N` | ❌ rejeita | ❌ rejeita | Curso em minúsculas |
| `CCO/2026/0001/M` | ❌ rejeita | ❌ rejeita | Separador incorreto |
| `CCO-2026-0001-X` | ❌ rejeita | ❌ rejeita | Turno inexistente |
| `CCO-2026-0001-M-EXTRA` | ❌ rejeita | ❌ rejeita | Caracteres extras |
| `SIS-2024-5678-M` | ✅ aceita | ✅ aceita | 🆕 Limite inferior 2024 |
| `CCO-2029-0001-T` | ✅ aceita | ✅ aceita | 🆕 Limite superior 2029 |
| `ESW-2026-123-N` | ❌ rejeita | ❌ rejeita | 🆕 Caso quase correto |
| `SIS-2028-5678-M-EXTRA` | ❌ rejeita | ❌ rejeita | 🆕 Caracteres extras |

---

## 🧩 Justificativa por blocos

A expressão pode ser dividida em partes para facilitar a compreensão:

```text
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$
```

| **Bloco** | **Função** |
|:---|:---|
| `(CCO\|ESW\|SIS)` | 🎓 Permite os cursos CCO, ESW e SIS |
| `202[4-9]` | 📅 Permite os anos de 2024 a 2029 |
| `[0-9]{4}` | 🔢 Exige exatamente quatro algarismos |
| `(M\|T\|N)` | 🌙 Permite os turnos M, T ou N |
| `-` | ➖ Separa os blocos da matrícula |
| `^` | 🔰 Indica o início da cadeia |
| `$` | 🛑 Indica o fim da cadeia |

### 🔍 Entendendo a estrutura

```text
^(CCO|ESW|SIS) - 202[4-9] - [0-9]{4} - (M|T|N)$
       ↓              ↓          ↓           ↓
     Curso            Ano      Número       Turno
```

Dessa forma, cada parte da Regex corresponde diretamente a uma regra definida para o código de matrícula.

---

## 📊 Resultado da validação

Os testes realizados apresentaram os resultados esperados:

- ✅ Os exemplos válidos foram aceitos.
- ❌ Os exemplos inválidos foram rejeitados.
- 📅 Os limites de ano `2024` e `2029` foram validados.
- 🔢 O número foi limitado a exatamente quatro algarismos.
- 🎓 Apenas os cursos `CCO`, `ESW` e `SIS` foram aceitos.
- 🌙 Apenas os turnos `M`, `T` e `N` foram aceitos.
- 🚫 Caracteres extras foram rejeitados.
- ⚠️ Casos quase corretos também foram rejeitados corretamente.

---

## 📝 Conclusão

Depois de realizar os testes, foi possível verificar que a Regex funciona de acordo com as regras definidas para o código de matrícula.

Os exemplos válidos foram aceitos e os inválidos foram rejeitados, incluindo os testes com os anos de **2024** e **2029**, um caso quase correto e outro com **caracteres extras**.

Assim, a expressão:

```text
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$
```

representa corretamente o formato:

**CURSO - ANO - NÚMERO - TURNO**
