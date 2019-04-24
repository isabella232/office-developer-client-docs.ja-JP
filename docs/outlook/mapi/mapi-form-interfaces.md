---
title: MAPI フォームインターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351542"
---
# <a name="mapi-form-interfaces"></a>MAPI フォームインターフェイス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、フォームに関連する次のインターフェイスを定義します。
  
|**インターフェイス名**|**説明**|
|:-----|:-----|
|[imapiform](imapiformiunknown.md) <br/> |フォームオブジェクトを操作し、フォームオブジェクトのコマンドを処理します。  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |form オブジェクトが次のメッセージを処理できるかどうかを調べ、form オブジェクトの次または前の状態を変更します。  <br/> |
|[imapiformcontainer](imapiformcontaineriunknown.md) <br/> |特定のフォームコンテナーに対するフォームサーバーのインストール、アンインストール、および解決をサポートします。  <br/> |
|[imapiformfactory](imapiformfactoryiunknown.md) <br/> |構成可能な実行時フォームサーバーの使用をサポートします。  <br/> |
|[imapiforminfo](imapiforminfoimapiprop.md) <br/> |クライアントアプリケーションが、メッセージクラスに固有のプロパティを処理できるようにします。  <br/> |
|[imapiformmgr](imapiformmgriunknown.md) <br/> |クライアントアプリケーションがフォームサーバーに関する情報を取得し、フォームサーバーをアクティブ化して、メッセージングシステムにフォームサーバーをインストールできるようにします。  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |フォームオブジェクトに関連付けられたメッセージを操作するために使用します。  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |form オブジェクト内でイベントが発生したことをクライアントアプリケーションに通知します。  <br/> |
|[imapiviewcontext](imapiviewcontextiunknown.md) <br/> |form オブジェクト内の次、前、および削除コマンドに応答するために使用します。  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |メッセージストレージとの間でフォームオブジェクトの保存、初期化、および読み込みを行うために使用されます。  <br/> |
   
MAPI フォームインターフェイスのメソッドの詳細については、これらのインターフェイスのドキュメントを参照してください。 カスタムフォームを作成するために、すべての MAPI フォームインターフェイスを実装する必要はありません。 フォーム自体で必要なのは、 **IPersistMessage**、 **imapiform**、および**IMAPIFormAdviseSink**インターフェイスを実装することだけです。 また、 **imapiformfactory**および**imapiformfactory**を実装することもお勧めします。 **imapiformfactory**は OLE のコンプライアンスに役立ち、 **imapiformfactory**を使用すると、適切に記述されたクライアントアプリケーションがフォームをより適切に利用できるようになります。 
  
> [!NOTE]
> 厳密に言うと、 **IMAPIFormAdviseSink**はオプションのインターフェイスです。 ただし、フォームサーバーに実装することを強くお勧めします。 このインターフェイスは、メッセージングクライアントとフォームサーバー間の対話を効率的に行うために重要です。特に、フォームサーバーのメッセージクラスの複数のメッセージが処理されている場合です。 
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

