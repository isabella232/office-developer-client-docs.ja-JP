---
title: InfoPath オブジェクトモデルを使用するフォームテンプレートを実行時にトラブルシューティングする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- フォームテンプレートのトラブルシューティング [infopath 2007]、実行時、infopath 2003 互換フォームテンプレート、実行時のトラブルシューティング
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: 次のセクションでは、SemiTrust によって提供される infopath 2003 互換オブジェクトモデルを使用する infopath マネージコードフォームテンプレートの作業中に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。実行時の名前空間。
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414446"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>InfoPath オブジェクトモデルを使用するフォームテンプレートを実行時にトラブルシューティングする

次のセクションでは、 **infopath マネージコードフォームテンプレートの使用中に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。SemiTrust**名前空間は、実行時にあります。 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>実行時に未処理のマネージコード例外の通知を表示する

フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。 しかし、既定では、マネージ コード フォーム テンプレートを展開した場合の実行時には、未処理の例外は Info Path エラー ダイアログ ボックスに表示されることはありません。 実行時にマネージコードの例外が表示されるようにするには、「 [InfoPath 2003 オブジェクトモデルを使用してエラーを処理](how-to-handle-errors-using-the-infopath-2003-object-model.md)する」の「マネージコードの例外を処理する」セクションの手順に従ってください。
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>展開後のマネージコードフォームテンプレートに関する問題

マネージ コード フォーム テンプレートは、必ず最終的な展開先でテストしてください。 展開手順の詳細については、「[コードを含む InfoPath フォームテンプレートを展開](how-to-deploy-infopath-form-templates-with-code.md)する」を参照してください。 展開に影響を与えるセキュリティシナリオの詳細については、「[コードを含むフォームテンプレートのセキュリティモデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。
  
.NET Framework 1.1 Configuration ユーティリティおよび InfoPath フォーム テンプレート コード グループを使用して、マネージ コード フォーム テンプレート専用のアクセス許可を追加する場合、同じセキュリティ ポリシーをすべてのクライアント コンピューターに展開してください。 また、ローカル コンピューターの特定の場所を指す **URLEvidence** を指定する場合、指定先にはソリューションが最終的に展開されるフォルダー (展開中に使用される場所とは異なる場所) を指してください。 マネージコードフォームテンプレートの .net Framework セキュリティ設定を構成する方法については、「 [Configure security settings for form Templates for code](how-to-configure-security-settings-for-form-templates-with-code.md) 」の「特定の URL または UNC にあるフォームに FullTrust を割り当てる」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [コードを含むフォーム テンプレートのためのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)
- [コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)
- [InfoPath 2003 オブジェクト モデルを使用してエラーを処理する](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

