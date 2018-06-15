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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800432"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink: IUnknown

  
  
**適用されます**: Outlook 
  
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

