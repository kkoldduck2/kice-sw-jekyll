# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Language Guidelines

**IMPORTANT: 모든 응답은 반드시 한글로 작성해야 합니다.** 사용자가 영어로 질문하더라도 한글로 답변하세요. 이 프로젝트는 한국어 소프트웨어 아키텍처 문서화 사이트입니다.

## Project Overview

This is a Jekyll documentation site using the Just the Docs theme. The site appears to be focused on software architecture documentation, with comprehensive reference materials covering topics like database configuration, JVM tuning, MSA architecture, Kubernetes, and performance monitoring.

## Development Commands

### Local Development
- `bundle install` - Install Ruby dependencies
- `bundle exec jekyll serve` - Start local development server (serves at localhost:4000)
- `bundle exec jekyll build` - Build the site to `_site/` directory

### Theme and Dependencies
- Uses Jekyll ~4.4.1
- Uses Just the Docs theme version 0.10.1 (pinned)
- Ruby version 3.3+ required

## Site Architecture

### Content Structure
- `index.md` - Homepage with site introduction
- `docs/reference.md` - Large reference document containing software architecture documentation
- `_config.yml` - Jekyll configuration with site title, theme, and navigation settings
- Content is organized in markdown with YAML front matter

### GitHub Actions Workflows
- `.github/workflows/pages.yml` - Deploys to GitHub Pages on main branch pushes
- `.github/workflows/ci.yml` - CI builds on pushes and PRs to validate site builds

### Key Files
- `Gemfile` - Ruby gem dependencies
- `_config.yml` - Site configuration including title, description, and auxiliary links
- Front matter in markdown files controls page layout and navigation

## Documentation Guidelines

The reference documentation covers four main categories:
1. Software Architecture 설계/구축 (Design/Construction)
2. Software Architecture 핵심 (Core Concepts)  
3. Software Architecture 환경 (Environment)
4. Software Architecture 운영/문제해결 (Operations/Troubleshooting)

Content includes technical guides, reference links, configuration examples, and troubleshooting procedures for enterprise software architecture topics.

## GitHub Pages Wiki Setup

이 프로젝트는 GitHub Pages를 통해 docs 폴더의 내용을 위키/문서 사이트로 배포하기 위한 목적으로 설정되었습니다.

### Wiki 배포 설정
- GitHub Pages는 자동으로 main 브랜치의 변경사항을 감지하여 사이트를 재배포합니다
- docs 폴더 내의 마크다운 파일들이 Just the Docs 테마를 통해 정리된 문서 사이트로 변환됩니다
- 새로운 문서를 추가할 때는 docs 폴더에 마크다운 파일을 생성하고 적절한 YAML front matter를 추가하세요

### 문서 구조화 가이드라인
- 각 문서는 YAML front matter로 시작하여 제목, 레이아웃, 네비게이션 순서를 정의합니다
- 대분류는 폴더로, 소분류는 개별 마크다운 파일로 구성하는 것을 권장합니다
- Just the Docs 테마의 네비게이션 기능을 활용하여 계층적 문서 구조를 만들 수 있습니다