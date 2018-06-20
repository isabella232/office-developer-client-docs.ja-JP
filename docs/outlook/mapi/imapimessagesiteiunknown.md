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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800615"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite: IUnknown

  
  
**適用されます**: Outlook 
  
メッセージを操作して、このような操作に応答するフォーム ビューアー コード (通常はクライアント アプリケーション) によって実装されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |サイト オブジェクトのメッセージ  <br/> |
|によって実装されます。  <br/> |フォームの閲覧者  <br/> |
|によって呼び出されます。  <br/> |フォーム オブジェクト  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIMessageSite  <br/> |
|ポインターの型。  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |現在のメッセージを作成または開いたの MAPI セッションを返します。  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |このようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |このようなフォルダーが存在する場合は、フォルダーを現在のメッセージを作成または開いたを返します。  <br/> |
|[自動インクリメント](imapimessagesite-getmessage.md) <br/> |現在のメッセージを返します。  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |フォーム サーバーが別のフォームのサーバーを開くに使用できるフォーム マネージャーのインターフェイスを返します。  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |新しいメッセージを作成します。  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |現在のメッセージをフォルダーにコピーします。  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |現在のメッセージをフォルダーに移動します。  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |現在のメッセージを削除します。  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |現在のメッセージを保存するように要求します。  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |現在のメッセージが配信のキューに置かれることを要求します。  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |メッセージに関するメッセージのサイト オブジェクトの現在のメッセージのサイトの機能に対応する情報を返します。  <br/> |
|[発生しました](imapimessagesite-getlasterror.md) <br/> |メッセージ サイト オブジェクトに発生する前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

