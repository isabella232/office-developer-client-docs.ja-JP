---
title: 実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- フォーム テンプレートのトラブルシューティング [infopath 2007]、実行時、InfoPath 2003 互換フォーム テンプレート、実行時のトラブルシューティング
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: 次のセクションでは、Microsoft が提供する InfoPath 2003 互換オブジェクト モデルを使用する InfoPath マネージ コード フォーム テンプレートの操作中に発生する可能性のある一般的なトラブルシューティングシナリオについて説明します。Office.Interop.InfoPath.SemiTrust 名前空間を実行時に指定します。
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414446"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティング

以下のセクションでは、実行時に **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルを使用する InfoPath マネージ コード フォーム テンプレートを操作する際に発生する一般的なトラブルシューティングシナリオについて説明します。 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>実行時に未処理のマネージ コード例外の通知を表示する

フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。 しかし、既定では、マネージ コード フォーム テンプレートを展開した場合の実行時には、未処理の例外は Info Path エラー ダイアログ ボックスに表示されることはありません。 実行時にマネージ コード例外を表示する場合は [、「InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用したエラーの処理」の「マネージ コード例外の処理」セクションの手順に従います。
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>展開後のマネージ コード フォーム テンプレートの問題

マネージ コード フォーム テンプレートは、必ず最終的な展開先でテストしてください。 展開手順の詳細については、「コードを使用して [InfoPath フォーム テンプレートを展開する」を参照してください](how-to-deploy-infopath-form-templates-with-code.md)。 展開に影響するセキュリティ シナリオの詳細については、「コードを使用したフォーム テンプレートのセキュリティ モデルについて [」を参照してください](about-the-security-model-for-form-templates-with-code.md)。
  
.NET Framework 1.1 Configuration ユーティリティおよび InfoPath フォーム テンプレート コード グループを使用して、マネージ コード フォーム テンプレート専用のアクセス許可を追加する場合、同じセキュリティ ポリシーをすべてのクライアント コンピューターに展開してください。 また、ローカル コンピューターの特定の場所を指す **URLEvidence** を指定する場合、指定先にはソリューションが最終的に展開されるフォルダー (展開中に使用される場所とは異なる場所) を指してください。 マネージ コード フォーム テンプレートの .NET Framework セキュリティ設定の構成の詳細については、「Configure Security 設定 for Form [Templates](how-to-configure-security-settings-for-form-templates-with-code.md) with Code」の「特定の URL または UNC でのフォームへのフルトラストの割り当て」セクションを参照してください。 
  
## <a name="see-also"></a>関連項目

- [コードを含むフォーム テンプレートのためのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)
- [コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)
- [InfoPath 2003 オブジェクト モデルを使用してエラーを処理する](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

