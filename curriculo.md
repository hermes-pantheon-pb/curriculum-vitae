# CURRICULUM VITAE

**[SEU NOME COMPLETO]**  
Belo Horizonte, MG – Brasil  
E-mail: [seu-email@dominio.com] | Telefone: (31) 9XXXX-XXXX  
GitHub: [github.com/seu-usuario] | Portfólio de Infraestrutura: [link-do-repositorio]  
LinkedIn: [linkedin.com/in/seu-perfil]  

> **[Espaço para Foto 3x4]**: Adicione o arquivo `foto-perfil.jpg` nesta pasta para que sua foto seja renderizada automaticamente no cabeçalho do currículo.

---

## 🎯 RESUMO PROFISSIONAL
Estudante de **Engenharia de Computação na Universidade Federal de Minas Gerais (UFMG)** com sólida experiência prática na administração de sistemas Linux, virtualização de servidores (Proxmox VE), conteinerização com Docker e engenharia de redes segmentadas por VLANs (OPNsense e OpenWrt). Experiência comprovada no planejamento e sustentação de infraestrutura híbrida self-hosted de alta resiliência, integrando clusters locais a nós públicos em nuvem (Oracle Cloud Infrastructure - OCI). Vivência em governança de armazenamento centralizado (MergerFS, NFS/SMB), execução de rotinas de backup conteinerizadas efêmeras com criptografia ponta a ponta (rclone crypt) e observabilidade orientada a eventos e notificações por e-mail (S.M.A.R.T. e Uptime Kuma). Ciente dos fluxos de trabalho com Git e fundamentos conceituais de CI/CD, com forte motivação e preparo técnico para aprender e implementar esteiras de automação contínua dentro do laboratório.

---

## 🎓 FORMAÇÃO ACADÊMICA

**Bacharelado em Engenharia de Computação**  
Universidade Federal de Minas Gerais (UFMG) — Belo Horizonte, MG  
*Status: Em andamento (Previsão de Conclusão: [Ano])*

---

## 🛠️ COMPETÊNCIAS TÉCNICAS

- **Administração Linux**: Linux (Arch, Debian, Alpine), `systemd`, Shell Scripting, Gestão de Pacotes (`apt`, `pacman`, compilação via código-fonte).
- **Storage & Troubleshooting**: LVM, `fstab`, ext4/btrfs, Syncthing, Monitoramento (`htop`, `kill`), Análise de Logs (`journalctl`, `dmesg`).
- **Contêineres e Implantação**: Docker, Portainer, Arquitetura MicroVM, Oracle Cloud, Nginx (Reverse Proxy).
- **Redes, SSH e Segurança**: Pilha de Rede Linux (`iproute2`, `ss`), SSH, `iptables`, `nftables`, WireGuard, SSO.
- **Automação e Controle de Versão**: Python, C, C++, Git / GitHub, Pipelines Automatizados (`cron`, timers do `systemd`), `rclone`.

---

## 🚀 PROJETOS E EXPERIÊNCIA PRÁTICA EM INFRAESTRUTURA

### Infraestrutura Híbrida Self-Hosted, Redes e Virtualização | 2020 – Presente
*Ambiente de Laboratório Pessoal / Homelab de Alta Resiliência*
- **Virtualização e Segmentação Perimetral**: Arquitetei e administro hipervisor Proxmox VE operando firewall OPNsense virtualizado via PCIe Passthrough (IOMMU) de controladora física de rede dedicada. Implementei segmentação de tráfego com bridges Linux e VLANs 802.1Q (zonas confiáveis, dispositivos IoT e rede de convidados isolados), conectadas via trunk a um roteador Wi-Fi 6 com mapeamento para múltiplos SSIDs segregados.
- **Topologia de Rede Desacoplada e Alta Velocidade**: Desenvolvi arquitetura lógica com portas de acesso e bridges Linux para conectar estações de trabalho e microVMs internas com alta largura de banda e sem necessidade de gerenciar tagueamento no sistema operacional convidado.
- **Orquestração Modular de Contêineres em MicroVMs**: Implantei dezenas de cargas de trabalho em microVMs Alpine Linux com recursos otimizados, utilizando stacks desacopladas de Docker Compose gerenciadas via Portainer (TheLounge, Uptime Kuma, streaming de mídia com aceleração por GPU, telemetria, downloaders e servidores de jogos, e outros).
- **Plataforma de Armazenamento Centralizado**: Configurei máquina virtual de armazenamento com OpenMediaVault (OMV) recebendo controladora HBA dedicada via IOMMU. Estruturei pooling de discos heterogêneos via MergerFS e barramento de compartilhamento NFS v4.2 direto sobre bridge isolada sem roteamento ou DNS.
- **Estratégia de Backup 3-2-1 e Automação de Manutenção**: Automatizei fluxos de trabalho de manutenção de infraestrutura e backup criando shell scripts agendados com `rclone` para sincronização de dados criptografados e off-site (Hetzner, Backblaze, Google Drive). Encapsulei rotinas em contêineres Docker efêmeros descartáveis (`docker run --rm`, não-root e volume montado como `:ro`), versionamento para *Point-in-Time Recovery* e priorização de processos via kernel Linux (`nice` e `ionice`).
- **Observabilidade Orientada a Eventos**: Configurei monitoramento contínuo com Uptime Kuma para verificação de disponibilidade e latência com alertas imediatos por e-mail. Ativei monitoramento proativo de integridade física S.M.A.R.T. (`smartd`), limites de capacidade do pool e captura de status de saída de scripts com envio de logs de erro por e-mail.
- **Documentação Arquitetural e Engenharia**: Elaborei documentação arquitetural abrangente detalhando topologias de rede, alocações de hardware virtual e procedimentos de implantação usando uma stack self-hosted do Wiki.js e repositório versionado no Git.

### Implantação de Cloud Pública e Segurança | 2024
*Infraestrutura em Nuvem (Oracle Cloud Infrastructure - OCI)*
- Provisionei e protegi infraestrutura de nuvem pública na Oracle Cloud para hospedar servidores acessíveis publicamente, protegendo as interfaces de gerenciamento por meio de um proxy reverso Nginx com autenticação de dois fatores (2FA) obrigatória.
  - **URL / Demonstração:** [https://sua-url-ou-servico.com](https://sua-url-ou-servico.com)
- Estruturei arquitetura de Ingress seguro conectada via túnel WireGuard de saída (outbound) originado da rede local, viabilizando acesso externo controlado sem necessidade de abertura de portas de entrada ou regras de NAT no roteador local.

### Pipeline Automatizado de Processamento de Mídia | 2026
- Desenvolvi rotinas automatizadas utilizando `ffmpeg` e `yt-dlp` para ingestão, segmentação por timestamps e catalogação dinâmica de metadados em fluxos de áudio e vídeo.
- Versionamento estruturado no Git/GitHub aplicando boas práticas de sanitização de scripts (`set -euo pipefail`), parâmetros modulares e controle de dependências.

---

## 🌐 IDIOMAS
- **Português**: Nativo
- **Inglês**: Leitura e escrita técnica avançadas (documentações, RFCs, manuais e repositórios internacionais); comunicação intermediária.
