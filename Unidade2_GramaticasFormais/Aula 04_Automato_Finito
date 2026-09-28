# 🤖 Construção de Autômato Finito Determinístico (AFD)

## 🎯 1. Desafio

Construir um **AFD** sobre o alfabeto:

> **Σ = {0, 1}**

O autômato deve reconhecer todas as palavras que **terminam com `00`**.

---

## 🔵 2. Estados

### 🟢 q0 — Estado Inicial

A palavra ainda **não termina em `0`**.

### 🟡 q1

A palavra **termina em `0`**.

### 🔴 q2 — Estado Final

A palavra **termina em `00`**.

---

## 🔄 3. Transições

| Estado | Lê `0` | Lê `1` |
|:---:|:---:|:---:|
| 🟢 **q0** | q1 | q0 |
| 🟡 **q1** | q2 | q0 |
| 🔴 **q2** | q2 | q0 |

---

## 🧩 4. Grafo do AFD

```text
             0             0
        ┌─────────► q1 ─────────► q2 🔴
        │             │             │
        │             │ 1           │ 0
        │             ▼             │
     🟢 q0 ◄──────────┘             │
        ▲                            │
        └────────────── 1 ──────────┘
```

### 📌 Legenda

- 🟢 **q0** → Estado inicial
- 🟡 **q1** → A palavra termina em `0`
- 🔴 **q2** → Estado final
- `0` e `1` → Símbolos do alfabeto

---

## 🧠 5. Explicação Lógica

O autômato precisa verificar se os **dois últimos símbolos** são `00`.

- 🔹 Em **q0**, ao ler `0`, vamos para **q1**.
- 🔹 Em **q1**, ao ler outro `0`, chegamos em **q2**.
- 🔹 **q2** é o estado final porque a palavra termina em `00`.
- 🔹 Se lermos `1`, a sequência de zeros é interrompida e voltamos para **q0**.
- 🔹 Em **q2**, ao ler `0`, permanecemos em **q2**, pois a palavra continua terminando em `00`.

---

## 🧪 6. Testes

| Palavra | Resultado | Motivo |
|:---:|:---:|---|
| `100` | ✅ **Aceita** | Termina em `00` |
| `1100` | ✅ **Aceita** | Termina em `00` |
| `101` | ❌ **Rejeita** | Não termina em `00` |

### 📚 Outros exemplos

- `00` → ✅ Aceita
- `000` → ✅ Aceita
- `010` → ❌ Rejeita
- `1001` → ❌ Rejeita

---

## 🏁 7. Conclusão

O AFD possui **3 estados**:

- 🟢 **q0** → estado inicial
- 🟡 **q1** → a palavra termina em `0`
- 🔴 **q2** → estado final, pois a palavra termina em `00`

### ✅ Resultado

O autômato reconhece exatamente as palavras sobre **Σ = {0, 1}** que **terminam em `00`**.
