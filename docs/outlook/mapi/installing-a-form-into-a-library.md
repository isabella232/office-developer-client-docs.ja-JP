---
title: ライブラリへのフォームのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433144"
---
# <a name="installing-a-form-into-a-library"></a>ライブラリへのフォームのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Windows SDK で提供される既定の MAPI フォームマネージャーは、さまざまなフォームライブラリにフォームをインストールするためのユーザーインターフェイスを提供しません。 このため、ユーザーがフォームのインストールに使用できる小さなアプリケーションまたは詳細な手順のセットを作成する必要があります。
  
インストールアプリケーションを実装する場合、フォームをフォルダーに関連付けられたコンテンツテーブルにインストールするために実行する必要がある一連のアクションは次のとおりです。
  
1. [MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出して、フォームマネージャーを開きます。 
    
2. [imapiformmgr:: openformcontainer](imapiformmgr-openformcontainer.md)または[imapiformmgr:: selectformcontainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、フォームのターゲットコンテナーを選択して開きます。 
    
3. [imapiformcontainer:: installform](imapiformcontainer-installform.md)関数を使用して、フォームをインストールします。 
    
    手順 4 ~ 6 は、ローカルフォームライブラリへのインストールに使用できます。
    
4. インストールがユーザーのワークステーション上のローカルフォームライブラリにインストールされている場合は、すべてのファイルをローカルディスク上の適切な場所にコピーします。 必要に応じて、コンポーネントの現在のパスを反映するようにフォーム構成ファイルを変更します。 フォーム構成ファイルには相対パスを含めることができます。この場合、この手順は必要ありません。
    
5. 適切な OLE 登録手順を実行して、メッセージの種類とインストールされているフォームサーバーを関連付けます。
    
6. フォームがローカルフォームライブラリにインストールされている場合は、フォームのアイコン (.ico) ファイルと構成ファイル (cfg) を%WINDOWS%\FORMS\CONFIGS ディレクトリにコピーして、フォームライブラリが破損または削除された場合に、フォームを自動的に復元できるようにします。 この手順は推奨されていますが、必須ではありません。
    
> [!NOTE]
> 手順1と2を[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数の呼び出しで置き換えることにより、ローカルフォームライブラリへのインストールを簡素化できます。 
  
## <a name="see-also"></a>関連項目



[MAPI フォームサーバーの開発](developing-mapi-form-servers.md)

