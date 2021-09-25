---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1807497f75b37b4aed041ba680cdd231337157e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600954"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知を処理するためのアアドバイス シンク オブジェクトを実装します。 アドバイス シンク オブジェクトへのポインターは、サービス プロバイダーの **Advise** メソッド (通知の登録に使用されるメカニズム) への呼び出しで渡されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |シンク オブジェクトのアドバイス  <br/> |
|実装元:  <br/> |クライアント アプリケーションと MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダーと MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIAdviseSink  <br/> |
|ポインターの種類:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |1 つ以上のタスクを実行して通知に応答します。 実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

