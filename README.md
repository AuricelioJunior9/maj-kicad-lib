# Biblioteca KiCad — MAJ Circuits

Símbolos e footprints dos componentes vendidos pela **MAJ Circuits**, prontos para
usar no KiCad. Cada componente traz o **SKU da loja** embutido, então a lista de
materiais (BOM) do seu projeto já sai com o código de compra.

🛒 Loja: https://www.majcircuits.com.br

---

## Conteúdo

| Arquivo | O que é |
|---|---|
| `maj-kicad-lib.kicad_sym` | Biblioteca de **símbolos** (esquemático) |
| `MAJ.pretty/` | Biblioteca de **footprints** (placa) |
| `MAJ.3dshapes/` | **Modelos 3D** (.step — abre em qualquer CAD) |

### Componentes disponíveis

| Símbolo | Footprint | Modelo 3D | Descrição | SKU |
|---|---|---|---|---|
| `BC547` | `TO-92_Inline` | `TO-92_Inline.step` | Transistor NPN, 0.1 A Ic, 45 V Vce, TO-92 | `BC547` |

> Esta lista cresce conforme novos componentes são cadastrados na loja.

---

## Como instalar

### Símbolos

1. No KiCad, abra o **Editor de Símbolos**
2. **Preferências → Gerenciar bibliotecas de símbolos...**
3. Aba **Bibliotecas globais** → botão **+** (ou o ícone de pasta)
4. Aponte para o arquivo `maj-kicad-lib.kicad_sym`
5. Defina o **Apelido** como `MAJ` → **OK**

### Footprints

1. Abra o **Editor de Footprints**
2. **Preferências → Gerenciar bibliotecas de footprint...**
3. Aba **Bibliotecas globais** → ícone de **pasta** (adicionar biblioteca existente)
4. Aponte para a pasta `MAJ.pretty`
5. Defina o **Apelido** como `MAJ` → **OK**

Pronto: os componentes aparecem como `MAJ:BC547` e `MAJ:TO-92_Inline`.

### Modelos 3D

Os arquivos `.step` da pasta `MAJ.3dshapes/` são **universais** — abrem em qualquer
CAD (KiCad, Altium, Fusion 360, SolidWorks, FreeCAD). Use-os para verificar
encaixe mecânico, projetar caixas e gerar renders do seu produto.

No KiCad, o modelo já vem associado ao footprint: basta abrir o visualizador 3D
(**Alt+3**) que o componente aparece montado na placa.

---

## Convenções da biblioteca

- **Símbolos** são nomeados pelo **componente** (`BC547`).
- **Footprints** são nomeados pelo **encapsulamento** (`TO-92_Inline`), porque o
  mesmo encapsulamento serve a vários componentes (BC547, BC548, 2N2222...).
- Todos os símbolos são **achatados** (sem herança), então funcionam de forma
  independente, sem exigir as bibliotecas oficiais do KiCad instaladas.
- Campos extras presentes em cada símbolo:
  - `SKU` — código do produto na MAJ Circuits
  - `Fornecedor` — `MAJ Circuits`
  - `Loja` — link direto para a página do produto

---

## Licença

**CC-BY-SA 4.0.** Uso livre em projetos comerciais e fechados — veja
[LICENSE.md](LICENSE.md) para os detalhes e a atribuição às bibliotecas oficiais
do KiCad.

Datasheets são propriedade dos fabricantes e apenas referenciados por link.
