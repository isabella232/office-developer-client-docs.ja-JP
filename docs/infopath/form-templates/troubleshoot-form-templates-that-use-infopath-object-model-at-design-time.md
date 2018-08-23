---
title: デザイン時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティングを行う
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, troubleshooting at design time,troubleshooting form templates [InfoPath 2007], design time
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: ここでは、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルを使用する、マネージ コード フォーム テンプレートのデザイン時およびデバッグ時に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。
ms.openlocfilehash: af71c8058744561a4c8ee0870fb37054e9979751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799216"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>デザイン時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティングを行う

ここでは、 **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルを使用する、マネージ コード フォーム テンプレートのデザイン時およびデバッグ時に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>オブジェクト モデル セキュリティ レベル 3 のメソッドとプロパティへの呼び出しを使用するフォーム テンプレートをプレビューまたはデバッグできない

完全信頼を必要とするオブジェクト モデルのメンバーを呼び出すコードが含まれるマネージ コード プロジェクトをデバッグまたはプレビューしようとすると、"ハンドルされていないセキュリティの例外がフォームのコードで発生しました" というエラー メッセージが InfoPath によって表示され、フォームが開きません。 フォーム テンプレートのビジネス ロジックをデバッグまたはプレビューできるようにするには、セキュリティ レベルを [ **完全信頼**] に設定し、フォームにデジタル署名する必要があります。 これを行う方法の詳細については、[プレビューしその必要とする完全信頼フォーム テンプレートのデバッグ](how-to-preview-and-debug-form-templates-that-require-full-trust.md)を参照してください。
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>MatchPath パラメーターの値を手動で削除した場合に、イベント ハンドラーの XPath 式を更新できない

フィールドまたはグループにイベント ハンドラーを追加し、後から InfoPath の [ **フィールド**] 作業ウィンドウで、そのフィールドやグループに影響を与えるような方法で (たとえば、名前を変更したり移動したりする) データ ソースのスキーマを変更した場合、フォームのコードの XPath 式を更新するかどうかを確認するメッセージが表示されます。 このメッセージで言及されている XPath 式は、[MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) 属性の [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) パラメーターで指定されている値のことで、これらの値はイベント ハンドラーをフォームのデータ ソースのフィールドやグループに関連付けるために使用されます。 コードの他の XPath 式は更新されません。 XPath 式を更新するためのアルゴリズムは、フォーム コードで適用される **MatchPath** 属性の **InfoPathEventHandler** パラメーターに格納されている値によって異なります。 XPath 式を更新するかどうかを確認するメッセージに応答する前に、これらの値を手動で削除した場合、InfoPath は XPath 式を自動的に更新できなくなります。 詳細については、[追加のイベント ハンドラーを使用して InfoPath 2003 オブジェクト モデル](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)を参照してください。
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>InfoPath 2003 互換オブジェクト モデルのメンバーを別のスレッドで呼び出すことができない

InfoPath 2003 互換オブジェクト モデルでは、別のスレッドでの呼び出しがサポートされていません。たとえば、InfoPath オブジェクト モデルのメンバーを呼び出す LaunchOMFunction という関数を呼び出す次のコードは実行されません。 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

必要に応じて、この制限を回避する方法があります。詳細については、「[InfoPath 2003 オブジェクト モデルを使用する InfoPath プロジェクトにおけるスレッドのサポート](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)」を参照してください。
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>オプションのパラメーターを省略すると、Visual Basic および Visual C# でビルド エラーが発生する

InfoPath オブジェクト モデルのメンバーにオプションのパラメーターがある場合に、そのパラメーターの値を指定しないときは、代わりにそのパラメーターの **Type.Missing** フィールドを渡す必要があります。実際の値を省略したときに **Type.Missing** フィールドを渡さないと、ビルド エラーが発生します。これは Visual Basic と Visual C# のどちらで書かれたコードにも当てはまります。詳細と例については、「 [InfoPath 2003 互換オブジェクト モデル](infopath-2003-compatible-object-models.md)」の「InfoPath オブジェクト モデルのメンバーにオプションのパラメーターを渡す」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [コードを含むフォーム テンプレートのためのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)
- [コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)
- [InfoPath 2003 オブジェクト モデルを使用してエラーを処理する](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

