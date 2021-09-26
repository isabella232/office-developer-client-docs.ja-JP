---
title: MAPI フォーム インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b314e9c3d0e8ffd82a94ae981b259cb3b845254c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610322"
---
# <a name="mapi-form-interfaces"></a>MAPI フォーム インターフェイス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、フォームに関連する次のインターフェイスを定義します。
  
|**インターフェイス名**|**説明**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |フォーム オブジェクトを操作し、フォーム オブジェクト コマンドを処理します。  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |フォーム オブジェクトが次のメッセージを処理できるかどうかを判断し、フォーム オブジェクトの次または前の状態を変更します。  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |特定のフォーム コンテナーに対するフォーム サーバーのインストール、アンインストール、および解決をサポートします。  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |構成可能な実行時フォーム サーバーの使用をサポートします。  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |クライアント アプリケーションがメッセージ クラスに固有のプロパティを操作できます。  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |クライアント アプリケーションがフォーム サーバーに関する情報を取得し、フォーム サーバーをアクティブ化し、メッセージング システムにフォーム サーバーをインストールできます。  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |フォーム オブジェクトに関連付けられたメッセージを操作するために使用します。  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |フォーム オブジェクトでイベントが発生したとクライアント アプリケーションに通知します。  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |フォーム オブジェクトの [次へ]、[前へ]、および [削除] のコマンドに応答するために使用します。  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |メッセージ ストレージ間のフォーム オブジェクトの保存、初期化、読み込みに使用されます。  <br/> |
   
MAPI フォーム インターフェイスのメソッドの詳細については、これらのインターフェイスのドキュメントを参照してください。 カスタム フォームを作成するには、すべての MAPI フォーム インターフェイスを実装する必要があります。 フォーム自体は **、IPersistMessage、IMAPIForm、****および IMAPIFormAdviseSink** インターフェイスを実装する必要があります。  さらに **、IMAPIFormFactory と IMAPIFormInfo** を実装 **するのも良い考えです**。 **IMAPIFormFactory は** OLE コンプライアンスに役立ち **、IMAPIFormInfo** を使用すると、適切に記述されたクライアント アプリケーションでフォームをより有効に利用できます。 
  
> [!NOTE]
> 厳密に言えば **、IMAPIFormAdviseSink** はオプションのインターフェイスです。 ただし、フォーム サーバーに実装する必要があります。 このインターフェイスは、特にフォーム サーバーのメッセージ クラスのいくつかのメッセージが処理されている場合に、メッセージング クライアントとフォーム サーバー間の効率的なやり取りを行う上で重要です。 
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

