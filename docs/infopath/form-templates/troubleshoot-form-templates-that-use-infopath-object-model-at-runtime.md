---
title: 実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティングを行う
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- troubleshooting form templates [infopath 2007], run time,InfoPath 2003-compatible form templates, troubleshooting at run time
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: ここでは、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間によって実行時に提供される InfoPath 2003 互換オブジェクト モデルを使用する、InfoPath マネージ コード フォーム テンプレートの操作時に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799222"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティングを行う

ここでは、 **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって実行時に提供される InfoPath 2003 互換オブジェクト モデルを使用する、InfoPath マネージ コード フォーム テンプレートの操作時に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>実行時にマネージ コードの未処理の例外の通知を表示します。

フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。 しかし、既定では、マネージ コード フォーム テンプレートを展開した場合の実行時には、未処理の例外は Info Path エラー ダイアログ ボックスに表示されることはありません。 マネージ コード例外の実行時に表示する場合は、[処理エラーを使用して InfoPath 2003 オブジェクト モデル](how-to-handle-errors-using-the-infopath-2003-object-model.md)の「マネージ コード例外の処理」セクションの手順に従います。
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>展開後のマネージ コードのフォーム テンプレートの問題

マネージ コード フォーム テンプレートは、必ず最終的な展開先でテストしてください。 展開手順については、[コードを含む InfoPath フォーム テンプレートの展開](how-to-deploy-infopath-form-templates-with-code.md)を参照してください。 展開に関係するセキュリティ シナリオの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。
  
.NET Framework 1.1 Configuration ユーティリティおよび InfoPath フォーム テンプレート コード グループを使用して、マネージ コード フォーム テンプレート専用のアクセス許可を追加する場合、同じセキュリティ ポリシーをすべてのクライアント コンピューターに展開してください。 また、ローカル コンピューターの特定の場所を指す **URLEvidence** を指定する場合、指定先にはソリューションが最終的に展開されるフォルダー (展開中に使用される場所とは異なる場所) を指してください。 マネージ コード フォーム テンプレートの.NET Framework のセキュリティの設定を構成する方法の詳細については、[コードのフォーム テンプレートのセキュリティ設定の構成](how-to-configure-security-settings-for-form-templates-with-code.md)のトピックの「を割り当てること FullTrust をフォームで特定の URL または UNC」セクションを参照してください。 
  
## <a name="see-also"></a>関連項目

- [コードを含むフォーム テンプレートのためのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)
- [コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)
- [InfoPath 2003 オブジェクト モデルを使用してエラーを処理する](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

