---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321351"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを操作し、そのような操作に応答するフォームビューアコード (通常はクライアントアプリケーション) によって実装されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |メッセージサイトオブジェクト  <br/> |
|実装元:  <br/> |フォームビューアー  <br/> |
|呼び出し元:  <br/> |フォーム オブジェクト  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIMessageSite  <br/> |
|ポインターの種類:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[getsession](imapimessagesite-getsession.md) <br/> |現在のメッセージが作成または開かれた MAPI セッションを返します。  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |そのようなストアが存在する場合は、現在のメッセージが含まれているメッセージストアを返します。  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |現在のメッセージが作成または開かれたフォルダー (そのフォルダーが存在する場合) を返します。  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |現在のメッセージを返します。  <br/> |
|[getformmanager](imapimessagesite-getformmanager.md) <br/> |フォームサーバーが別のフォームサーバーを開くために使用できるフォームマネージャーインターフェイスを返します。  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |新しいメッセージを作成します。  <br/> |
|[copymessage](imapimessagesite-copymessage.md) <br/> |現在のメッセージをフォルダーにコピーします。  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |現在のメッセージをフォルダーに移動します。  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |現在のメッセージを削除します。  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |現在のメッセージを保存するよう要求します。  <br/> |
|[submitmessage](imapimessagesite-submitmessage.md) <br/> |現在のメッセージが配信のためにキューに入れられるように要求します。  <br/> |
|[getsitestatus](imapimessagesite-getsitestatus.md) <br/> |現在のメッセージのメッセージサイトの機能に関する情報をメッセージサイトオブジェクトから返します。  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |メッセージサイトオブジェクトに発生する前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

