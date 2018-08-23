---
title: ライブラリへのフォームのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d3b20c9fb4b4f1a26eb4ed1a9a498bd56a915a70
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579782"
---
# <a name="installing-a-form-into-a-library"></a>ライブラリへのフォームのインストール

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Windows SDK に付属している既定の MAPI フォーム マネージャーでは、各種のフォーム ライブラリにフォームをインストールするためのユーザー インターフェイスを行いません。 このため、小規模なアプリケーションを作成する必要がある、または一連の命令の詳細: ユーザーがフォームをインストールするのには使用できます。
  
インストール アプリケーションを実装する場合、一連のアクションを実行する必要の表は、次のとおりのフォルダーの関連する内容にフォームをインストールするのには。
  
1. マネージャーを開くには、フォームの[MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出します。 
    
2. [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)または[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、選択し、フォームの移動先のコンテナーを開きます。 
    
3. フォームをインストールするのにには、 [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)関数を使用します。 
    
    4 ~ 6 の手順は、ローカルのフォーム ライブラリにインストールのことです。
    
4. インストールがユーザーのワークステーション上のローカル フォーム ライブラリにある場合は、ローカル ディスク上の適切な場所にすべてのファイルをコピーします。 必要に応じて、コンポーネントの現在のパスを反映するようにフォーム構成ファイルを変更します。 フォーム構成ファイルは、場合にこの手順は必要ありません、相対パスを含めることができます。
    
5. インストールされているフォームのサーバーにメッセージの種類を関連付けるには、適切な OLE 登録手順を完了します。
    
6. ローカル フォーム ライブラリにフォームがインストールされた場合、フォームのアイコン (.ico) と構成 (.cfg) ファイル ディレクトリにコピー、%WINDOWS%\FORMS\CONFIGS フォーム復元できるように自動的にフォーム ライブラリが破損または削除された場合にします。 この手順は、推奨されるが、必須ではないです。
    
> [!NOTE]
> 手順 1 と 2 を[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数の呼び出しに置き換えることによって、ローカルのフォーム ライブラリにインストールを簡略化できます。 
  
## <a name="see-also"></a>関連項目



[MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

