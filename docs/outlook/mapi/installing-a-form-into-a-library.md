---
title: ライブラリへのフォームのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 808bf3b934e05d4f7d856986fa5ead299a247d05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630524"
---
# <a name="installing-a-form-into-a-library"></a>ライブラリへのフォームのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
WINDOWS SDK に付属する既定の MAPI フォーム マネージャーは、さまざまなフォーム ライブラリにフォームをインストールするユーザー インターフェイスを提供します。 この理由から、ユーザーがフォームのインストールに使用できる小さなアプリケーション (または手順の詳細なセット) を作成する必要があります。
  
インストール アプリケーションを実装する場合、フォルダーに関連付けられたコンテンツ テーブルにフォームをインストールするために実行する必要がある一連のアクションは次のとおりです。
  
1. [MAPIOpenFormMgr 関数を呼び](mapiopenformmgr.md)出して、フォーム マネージャーを開きます。 
    
2. [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)または[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、フォームのターゲット コンテナーを選択して開きます。 
    
3. [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)関数を使用してフォームをインストールします。 
    
    手順 4 ~ 6 は、ローカル フォーム ライブラリにインストールするための手順です。
    
4. インストールがユーザーのワークステーションのローカル フォーム ライブラリにインストールされている場合は、すべてのファイルをローカル ディスク上の適切な場所にコピーします。 必要に応じて、フォーム構成ファイルを変更して、コンポーネントの現在のパスを反映します。 フォーム構成ファイルには相対パスを含め、その場合、この手順は必要ありません。
    
5. 適切な OLE 登録手順を実行して、メッセージの種類をインストール中のフォーム サーバーに関連付ける。
    
6. フォームがローカル フォーム ライブラリにインストールされている場合は、フォーム ライブラリが破損または削除された場合にフォームを自動的に復元できるよう、フォームのアイコン (.ico) および構成 (.cfg) ファイルを %WINDOWS%\FORMS\CONFIGS ディレクトリにコピーします。 この手順は推奨されますが、必須ではありません。
    
> [!NOTE]
> 手順 1 と 2 を [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) 関数の呼び出しに置き換え、ローカル フォーム ライブラリへのインストールを簡略化できます。 
  
## <a name="see-also"></a>関連項目



[MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

