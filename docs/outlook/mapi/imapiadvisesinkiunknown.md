---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573804"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
通知を処理するためのアドバイズ シンク オブジェクトを実装します。 アドバイズ シンク オブジェクトへのポインターは、通知の登録に使用される機構、サービス プロバイダーの**アドバイズ**メソッドへの呼び出しで渡されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |通知シンク オブジェクト  <br/> |
|によって実装されます。  <br/> |クライアント アプリケーションと MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダーおよび MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIAdviseSink  <br/> |
|ポインターの型。  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |通知に応答するには、1 つまたは複数のタスクを実行します。 実行するタスクは、イベントおよび通知を生成するオブジェクトの種類によって異なります。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

