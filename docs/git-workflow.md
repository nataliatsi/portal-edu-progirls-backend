## **Fluxo recomendado (Fork + Upstream — ProGirls Backend)**

Repositório oficial:
👉 [https://github.com/Programmer-Girls/portal-edu-progirls-backend](https://github.com/Programmer-Girls/portal-edu-progirls-backend)

---

## 🔄 **Sempre manter seu projeto atualizado**

Antes de começar qualquer tarefa, sincronize seu repositório com o projeto original:

```bash
git checkout main
git pull upstream main
git push origin main
```

> 💡 Isso garante que você esteja trabalhando com a versão mais recente do projeto, evitando conflitos e problemas no Pull Request.

Depois, atualize sua branch de trabalho:

```bash
git checkout sua-branch 
git merge main
git push origin sua-branch
```

---

## **1. Criar / acessar sua branch**

```bash
git checkout -b nome-da-branch
```

Ou, se já existir:

```bash
git checkout nome-da-branch
```

---

## **2. Fazer alterações + commit**

```bash
git add .
git commit -m "[FEAT] descrição clara do que foi feito"
```

---

## **3. Subir para o seu fork**

```bash
git push origin nome-da-branch
```

---

## **4. Abrir Pull Request (PR)**

No GitHub, MUITO IMPORTANTE 👇

### ✅ Configuração correta:

```
base repository:   Programmer-Girls/portal-edu-progirls-backend
base branch:       developer

head repository:   SEU-FORK/portal-edu-progirls-backend
compare branch:    sua-branch
```

---

### ✅ Exemplo correto

```
base:     Programmer-Girls/portal-edu-progirls-backend ← developer
compare:  nataliafork/portal-edu-progirls-backend      ← natalia
```

Isso significa:

* PR indo para o projeto oficial ✅
* Na branch correta (`developer`) ✅

---

### ❌ Erro comum

```
base:     nataliafork/portal-edu-progirls-backend ← main
```

Isso cria PR no fork (errado)

---

### ⚠️ Se estiver errado

Clicar em:

**"compare across forks"**

E ajustar manualmente:

* base → `Programmer-Girls/...`
* branch → `developer`

---

## **5. Após abrir o PR**

### ✔️ Se pedirem ajustes:

```bash
git add .
git commit -m "[FIX] ajustes do PR"
git push origin sua-branch
```

O PR atualiza automaticamente

---

### ✔️ Se o PR for aprovado e mergeado:

Atualize tudo de novo:

```bash
git checkout main
git pull upstream main
git push origin main
```

Depois:

```bash
git checkout sua-branch
git merge main
```

---

## 🧠 **Resumo do fluxo**

1. Atualiza `main` com `upstream`
2. Atualiza sua branch
3. Desenvolve
4. Commit + push
5. Abre PR para `developer`
6. Após merge → atualiza tudo novamente

---

## 🪙 **Regra de ouro**

> PR sempre vai para o repositório original (upstream)
> **e para a branch `developer`, nunca `main`**
