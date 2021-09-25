---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f58ad771c166675ca43d928b9135941a41518976
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551297"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ビューアーがフォーム ビューのコンテキストとフォーム通知を操作したり、フォーム動詞を実行したり、フォームをシャットダウンしたりできます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォーム オブジェクト  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォーム ビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIForm  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |フォームのビュー コンテキストを確立します。  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |フォームの現在のビュー コンテキストを返します。  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |フォームを閉じます。  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |フォームが特定の動詞に関連付けるタスクを実行する要求。  <br/> |
|[アドバイス](imapiform-advise.md) <br/> |フォームに影響を与えるイベントに関する通知用にフォーム ビューアーを登録します。  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Advise を呼び出して以前に確立されたフォーム ビューアーを使用して通知の登録を **取り消します**。  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |フォーム オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

