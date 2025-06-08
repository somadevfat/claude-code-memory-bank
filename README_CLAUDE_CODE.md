# Memory Bank System for Claude Code v1.0

Claude Code専用に最適化されたタスク管理システム。VAN、PLAN、CREATIVE、IMPLEMENT、REFLECT、ARCHIVEモードと新しい一気通貫モードを統合。

## 🚀 クイックスタート

### 基本の使い方
1. **VAN**: プロジェクト初期化とタスク分析
2. **PLAN**: 詳細な実装計画作成
3. **CREATIVE**: 設計とアーキテクチャ決定
4. **IMPLEMENT**: コード実装とビルド
5. **REFLECT**: レビューと振り返り
6. **ARCHIVE**: ドキュメント整理

### 🏃 一気通貫モード (新機能)
**TURBO**モードで全フェーズを連続実行:
```
TURBO [タスク説明]
```

## ⚡ モード詳細

### VAN モード (🔍 初期化)
- プロジェクト構造分析
- 複雑度レベル判定
- タスクの優先順位決定

### PLAN モード (📋 計画)
- 実装戦略立案
- 依存関係の特定
- リスク評価

### CREATIVE モード (🎨 設計)
- アーキテクチャ設計
- 複数オプション検討
- 技術選択

### IMPLEMENT モード (⚒️ 実装)
- コード作成
- テスト実行
- デバッグ

### REFLECT モード (🔍 振り返り)
- 実装レビュー
- 課題の特定
- 改善点の抽出

### ARCHIVE モード (📦 整理)
- ドキュメント作成
- ナレッジベース更新
- プロジェクト完了

## 🎯 一気通貫モード: TURBO

すべてのフェーズを自動で実行する革新的なモード。

### 特徴
- **自動フェーズ切り替え**: VAN → PLAN → CREATIVE → IMPLEMENT → REFLECT → ARCHIVE
- **インテリジェント判断**: 必要なフェーズのみ実行
- **継続的実行**: エラー時も自動復旧
- **効率最優先**: 冗長な処理を排除

### 使用方法
```
TURBO 新しいログイン機能を追加してください
```

### フロー
```mermaid
graph LR
    T[TURBO] --> V[VAN]
    V --> P[PLAN]
    P --> C{CREATIVE必要?}
    C -->|Yes| CR[CREATIVE]
    C -->|No| I[IMPLEMENT]
    CR --> I
    I --> R[REFLECT]
    R --> A[ARCHIVE]
    A --> ✅[完了]
```

## 📁 ファイル構造

```
.cursor/
├── rules/
│   ├── main.mdc
│   └── isolation_rules/
│       ├── visual-maps/
│       ├── Level1-4/
│       └── Core/
└── memory_bank/
    ├── tasks.md          # 中央タスク管理
    ├── activeContext.md  # 現在のコンテキスト
    ├── progress.md       # 進捗追跡
    └── docs/
        └── archive/      # 完了タスクアーカイブ
```

## 🔧 Claude Code最適化

### メモリ管理
- 階層ルール読み込み
- トークン使用量最適化
- コンテキスト効率化

### ツール統合
- Bash、Read、Write、Edit等フル活用
- マルチツール並列実行
- エラーハンドリング強化

### 日本語対応
- 完全日本語インターフェース
- 日本の開発慣習に最適化
- セキュリティベストプラクティス統合

## 🛠️ セットアップ

### 1. ファイル配置
```bash
cd your-project
git clone https://github.com/vanzan01/cursor-memory-bank.git
cp -r cursor-memory-bank/.cursor .
cp -r cursor-memory-bank/custom_modes .
```

### 2. CLAUDE.mdに統合
プロジェクトルートに以下を配置:

```markdown
# Memory Bank System

@.cursor/rules/main.mdc

## 基本ルール
- 日本語で回答
- セキュリティファイルは即座に.gitignoreに追加
- ステップバイステップ実装
- スモールステップでテスト

## モード
- VAN: 初期化とタスク分析
- PLAN: 詳細計画作成
- CREATIVE: 設計決定
- IMPLEMENT: 実装とビルド
- REFLECT: レビューと振り返り
- ARCHIVE: ドキュメント整理
- TURBO: 全フェーズ連続実行

## 一気通貫モード
TURBO [タスク] で全フェーズ自動実行
```

## 📊 複雑度レベル

- **Level 1**: 簡単なバグ修正 (直接IMPLEMENT)
- **Level 2**: 機能拡張 (VAN→PLAN→IMPLEMENT→REFLECT)
- **Level 3**: 新機能開発 (全フェーズ)
- **Level 4**: システム改修 (全フェーズ + 詳細設計)

## 🔄 ワークフロー例

### 通常ワークフロー
```
1. VAN - プロジェクト分析
2. PLAN - 実装計画
3. CREATIVE - 設計決定 (必要時)
4. IMPLEMENT - コード実装
5. REFLECT - レビュー
6. ARCHIVE - ドキュメント化
```

### TURBOワークフロー
```
TURBO ユーザー認証機能を追加
→ 自動で全フェーズ実行
→ 完了通知
```

## 💡 ベストプラクティス

### セキュリティ
- 機密情報の.gitignore自動追加
- 環境変数の適切な管理
- セキュリティキーの保護

### 開発効率
- 並列ツール実行
- インクリメンタルテスト
- 継続的ドキュメント更新

### コード品質
- 型チェック自動実行
- リント自動実行
- テストファースト開発

## 🚨 トラブルシューティング

### よくある問題
1. **ルールが読み込まれない**
   - `.cursor/rules/`の配置確認
   - ファイル権限確認

2. **モード切り替えができない**
   - tasks.mdの状態確認
   - activeContext.mdの確認

3. **TURBOモードが止まる**
   - エラーログ確認
   - 個別モードで再実行

## 📝 ライセンス

MIT License - 個人・商用利用可能

---

Memory Bank System v1.0 - Claude Code Optimized