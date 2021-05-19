---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434152"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの送信キュー内のすべてのメッセージに関する情報を含む、送信キュー テーブルへのアクセスを提供します。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppTable_
  
> [out]送信キュー テーブルへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 送信キュー テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::GetOutgoingQueue** メソッドは、メッセージ ストアの送信メッセージのキューを示すテーブルへのアクセス権を MAPI スプーラーに提供します。 通常、メッセージは [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドが呼び出された後に送信キュー テーブルに配置されます。 ただし、送信の順序は、トランスポート プロバイダーへの前処理と送信の順序に影響を与えるので、送信用にマークされている一部のメッセージが送信キュー テーブルにすぐに表示されない場合があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

送信キュー テーブルに列として含める必要があるプロパティの一覧については、「送信キュー テーブル」 [を参照してください](outgoing-queue-tables.md)。 
  
MAPI スプーラーは、送信時刻の昇順でメッセージ ストアからのメッセージを受け入れするように設計されています。MAPI スプーラーは、この順序に一致するように送信キュー テーブルを並べ替えるか、既定の並べ替え順序として確立できます。
  
送信メッセージ キュー テーブルの通知をサポートし、キューの内容が変更された場合に MAPI スプーラーに通知を受け取る必要があります。 
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

