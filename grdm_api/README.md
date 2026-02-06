# grdm-api

GakuNin RDM (GRDM) API の動作を確認するためのテストコード集です。

## 必要条件

- Python >= 3.12
- [uv](https://docs.astral.sh/uv/) (パッケージマネージャ)
- GRDM のパーソナルアクセストークン

## セットアップ

```bash
uv sync
```

アクセストークンは環境変数 `GRDM_TOKEN` に設定するか、ノートブック実行時に対話的に入力できます。

```bash
export GRDM_TOKEN="your-token-here"
```

## ノートブック

| ファイル | 概要 |
|---|---|
| [test_to_use_grdm_api.ipynb](notebooks/test_to_use_grdm_api.ipynb) | GRDM API v2 の各種エンドポイント（nodes, users, logs, contributors）を試す |
| [test_to_get_grdm_file_metadata.ipynb](notebooks/test_to_get_grdm_file_metadata.ipynb) | GRDM API v1 を使ってプロジェクト内のファイルメタデータを取得・パースする（Pydantic モデル付き） |

## 依存パッケージ

- [requests](https://docs.python-requests.org/) - HTTP クライアント
- [pydantic](https://docs.pydantic.dev/) - データバリデーション / メタデータモデル定義
- [JupyterLab](https://jupyterlab.readthedocs.io/) - ノートブック実行環境
