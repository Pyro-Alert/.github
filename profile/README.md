<div align="center">

<img src="https://github.com/Pyro-Alert.png" width="120" alt="Logo do Pyro Alert">

# Pyro Alert

**🌱 Antecipando chamas para um futuro mais verde**

Monitoramento de focos de incêndio com sensores em campo, mapa em tempo real e alertas automáticos.

[Instagram](https://www.instagram.com/pyroalert) · [pyroalertpessoal@gmail.com](mailto:pyroalertpessoal@gmail.com)

![Status](https://img.shields.io/badge/status-em_desenvolvimento-ff6b35)
![Feito no Brasil](https://img.shields.io/badge/feito_no-Brasil-009c3b)

</div>

## 🔥 O problema

Um incêndio em área de vegetação começa pequeno. Com calor, ar seco e vento, ele se espalha
rápido, e quanto antes é percebido, mais fácil é controlar. Muitas vezes, porém, o aviso só chega
quando a fumaça já é visível de longe.

## 💡 A nossa ideia

Instalar **artefatos**, pequenos dispositivos com sensores, nas áreas de risco. Eles medem o
ambiente o tempo todo e enviam os dados para a plataforma Pyro Alert, que:

- mostra cada artefato num **mapa ao vivo**, com a cor do seu estado;
- **avalia o risco de incêndio** combinando as leituras: ar quente e seco ao mesmo tempo,
  fumaça aumentando, solo ressecado;
- **avisa a equipe** assim que o risco aparece;
- percebe quando um artefato **para de responder durante uma situação de risco**, sinal de que
  ele pode ter sido atingido pelo fogo;
- permite **pedir uma foto** do local pela câmera do artefato, para confirmar o que está acontecendo.

## 📡 O que os artefatos medem

| Sensor | Por que importa |
|---|---|
| 🌡️ Temperatura do ar | O calor favorece o início e a propagação do fogo |
| 💧 Umidade do ar | Ar seco deixa a vegetação mais inflamável |
| 🌱 Temperatura e umidade do solo | Solo quente e seco indica vegetação vulnerável |
| 💨 Fumaça | Sinal direto de queima |
| 🧪 Gases inflamáveis | Gases que aparecem com a queima ou que facilitam a combustão |
| 📷 Câmera | Foto do local sob demanda |

Cada artefato pode ter uma combinação diferente de sensores, de acordo com o local onde é instalado.

## ⚙️ Como funciona

```mermaid
flowchart LR
  A["📡 Artefatos em campo<br/>sensores + câmera"] -- "leituras a cada minuto" --> P["☁️ Plataforma Pyro Alert<br/>coleta e análise de risco"]
  P --> M["🗺️ Mapa ao vivo"]
  P --> L["🚨 Alertas para a equipe"]
  M -- "comandos, ex.: tirar foto" --> A
```

## 🛠️ Tecnologias

![ESP32](https://img.shields.io/badge/ESP32-E7352C?logo=espressif&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?logo=mqtt&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_+_PostGIS-4169E1?logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

## 📂 Como o projeto é organizado

| Repositório | O que faz |
|---|---|
| [pyro-firmware](https://github.com/Pyro-Alert/pyro-firmware) | Programa dos artefatos: lê os sensores, envia os dados, tira fotos e se atualiza pela internet |
| [pyro-contracts](https://github.com/Pyro-Alert/pyro-contracts) | O formato oficial das mensagens entre os artefatos e a plataforma |
| [pyro-ingest](https://github.com/Pyro-Alert/pyro-ingest) | Recebe as leituras, avalia o risco de incêndio e dispara os alertas |
| [pyro-api](https://github.com/Pyro-Alert/pyro-api) | Usuários e permissões, cadastro de artefatos, histórico e comandos |
| [pyro-web](https://github.com/Pyro-Alert/pyro-web) | O site: mapa ao vivo, gráficos dos sensores e painel do administrador |
| [pyro-infra](https://github.com/Pyro-Alert/pyro-infra) | Infraestrutura, ambiente de desenvolvimento e simulador de artefatos |
| [pyro-ci](https://github.com/Pyro-Alert/pyro-ci) | Padrões de qualidade e automações compartilhadas por todos os repositórios |

<sub>Os repositórios do produto são privados e visíveis só para a equipe.</sub>

## 👥 Equipe

<table>
  <tr>
    <td align="center" width="160">
      <a href="https://github.com/Rvjq">
        <img src="https://github.com/Rvjq.png?size=120" width="100" alt="Foto de Rafael"><br>
        <b>Rafael</b>
      </a>
    </td>
    <td align="center" width="160">
      <a href="https://github.com/RebecaLyra">
        <img src="https://github.com/RebecaLyra.png?size=120" width="100" alt="Foto de Rebeca Lyra"><br>
        <b>Rebeca Lyra</b>
      </a>
    </td>
    <td align="center" width="160">
      <a href="https://github.com/Vinicius-DAS">
        <img src="https://github.com/Vinicius-DAS.png?size=120" width="100" alt="Foto de Vinicius Diniz"><br>
        <b>Vinicius Diniz</b>
      </a>
    </td>
  </tr>
</table>

## 📬 Contato

- Instagram: [@pyroalert](https://www.instagram.com/pyroalert)
- E-mail: [pyroalertpessoal@gmail.com](mailto:pyroalertpessoal@gmail.com)
