# AI Software Team

Yazilim gelistirme sureclerini AI agentlar ile yoneten multi-agent sistemi. Claude Code uzerinde calisir.

## Ne Yapar?

Bu proje, tam bir yazilim gelistirme takimini AI agentlar olarak tanimlar. Her agent kendi uzmanlik alaninda calisir ve Project Manager agent tarafindan koordine edilir.

## Agentlar

| Agent | Rol | Model |
|-------|-----|-------|
| **Project Manager** | Orkestrator — diger agentlari yonetir | Opus |
| **Product Owner** | Kullanici hikayeleri ve onceliklendirme | Sonnet |
| **Business Analyst** | Gereksinim analizi ve dokumantasyon | Sonnet |
| **System Architect** | Mimari tasarim ve teknoloji kararlari | Opus |
| **UI Designer** | Arayuz tasarimi ve kullanici deneyimi | Sonnet |
| **Frontend Developer** | Arayuz gelistirme | Sonnet |
| **Backend Developer** | Sunucu tarafı gelistirme | Sonnet |
| **DBA** | Veritabani tasarimi ve optimizasyonu | Sonnet |
| **DevOps Engineer** | CI/CD, altyapi ve deployment | Sonnet |
| **Security Engineer** | Guvenlik analizi ve denetimi | Sonnet |
| **QA Tester** | Test planlama ve otomasyon | Sonnet |
| **Code Reviewer** | Kod kalite kontrolu | Opus |
| **Technical Writer** | Dokumantasyon | Sonnet |

## Kurulum

### On Kosullar
- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) kurulu olmali
- Anthropic API anahtari tanimli olmali

### Kullanim

1. Bu repoyu klonlayin:
```bash
git clone https://github.com/[username]/ai-software-team.git
cd ai-software-team
```

2. Claude Code'u baslatin:
```bash
claude
```

3. Bir gorev verin:
```
PM agent'i calistir: Kullanici kayit sistemi gelistir
```

Veya belirli bir agent'i dogrudan kullanin:
```
System architect: E-ticaret uygulamasi icin mimari tasarla
```

## Is Akisi

```
Siz ──► Project Manager
              │
              ├─► Product Owner ──► Kullanici hikayeleri
              ├─► Business Analyst ──► Gereksinimler
              ├─► System Architect ──► Mimari
              ├─► UI Designer ──► Tasarim
              ├─► DBA ──► Veritabani semasi
              ├─► Backend Developer ──► API kodu
              ├─► Frontend Developer ──► Arayuz kodu
              ├─► Code Reviewer ──► Kod incelemesi
              ├─► QA Tester ──► Testler
              ├─► Security Engineer ──► Guvenlik raporu
              ├─► DevOps Engineer ──► CI/CD & deploy
              └─► Technical Writer ──► Dokumantasyon
```

## Proje Yapisi

```
.claude/
└── agents/          # Agent tanimlari
    ├── project-manager.md
    ├── product-owner.md
    ├── business-analyst.md
    ├── system-architect.md
    ├── ui-designer.md
    ├── frontend-developer.md
    ├── backend-developer.md
    ├── dba.md
    ├── devops-engineer.md
    ├── security-engineer.md
    ├── qa-tester.md
    ├── code-reviewer.md
    └── technical-writer.md
docs/
├── architecture/    # Mimari kararlar (ADR)
├── requirements/    # Gereksinim dokumanlari
├── design/          # UI/UX tasarim dokumanlari
├── api/             # API dokumantasyonu
└── testing/         # Test planlari ve raporlari
```

## Ozellestirme

Her agent dosyasini projenize ozel olarak duzenleyebilirsiniz:

- **Tech stack degisikligi:** Agent prompt'larindaki teknoloji referanslarini guncelleyin
- **Yeni agent ekleme:** `.claude/agents/` altina yeni `.md` dosyasi olusturun
- **Model degisikligi:** Agent frontmatter'indaki `model` alanini degistirin (opus/sonnet/haiku)
- **Arac kisitlama:** `tools` listesinden araclari ekleyin/cikarin

## Lisans

MIT
