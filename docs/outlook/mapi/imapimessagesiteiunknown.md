---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cc27b5d5ce3b0bbfd2dd407248be60a6baa157b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575912"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを操作し、そのような操作に応答するフォーム ビューアー コード (通常はクライアント アプリケーション) によって実装されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージ サイト オブジェクト  <br/> |
|実装元:  <br/> |フォーム ビューアー  <br/> |
|呼び出し元:  <br/> |フォーム オブジェクト  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIMessageSite  <br/> |
|ポインターの種類:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |現在のメッセージが作成または開かされた MAPI セッションを返します。  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |そのようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |そのようなフォルダーが存在する場合は、現在のメッセージが作成または開かされたフォルダーを返します。  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |現在のメッセージを返します。  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |フォーム サーバーが別のフォーム サーバーを開くのに使用できるフォーム マネージャー インターフェイスを返します。  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |新しいメッセージを作成します。  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |現在のメッセージをフォルダーにコピーします。  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |現在のメッセージをフォルダーに移動します。  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |現在のメッセージを削除します。  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |現在のメッセージを保存する要求。  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |現在のメッセージを配信キューに入れろという要求。  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |現在のメッセージに対するメッセージ サイトの機能に関する情報をメッセージ サイト オブジェクトから返します。  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |メッセージ サイト オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

