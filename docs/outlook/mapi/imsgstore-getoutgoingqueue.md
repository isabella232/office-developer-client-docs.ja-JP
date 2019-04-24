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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317333"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信キューテーブル (メッセージストアの送信キューにあるすべてのメッセージに関する情報を含むテーブル) へのアクセスを提供します。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpptable_
  
> 読み上げ送信キューテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 送信キューテーブルが正常に返されました。
    
## <a name="remarks"></a>解説

**IMsgStore:: getoutgoingqueue**メソッドは、メッセージストアの送信メッセージのキューを示すテーブルへのアクセス権を MAPI スプーラーに提供します。 通常、メッセージは[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出された後に、送信キューテーブルに配置されます。 ただし、送信の順序は、トランスポートプロバイダーへの前処理と送信の順序に影響するため、送信用にマークされているメッセージの一部は、すぐに送信キューテーブルに表示されない場合があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

送信キューテーブルに列として含める必要があるプロパティの一覧については、「[送信キューテーブル](outgoing-queue-tables.md)」を参照してください。 
  
mapi スプーラーは、送信時間の昇順でメッセージストアからのメッセージを受信するように設計されているため、mapi スプーラーで送信キューテーブルを並べ替えて、この順序に一致するようにするか、または既定の並べ替え順序として設定することができます。
  
キューの内容が変更されたときに MAPI スプーラーに通知されるように、送信メッセージキューテーブルの通知をサポートする必要があります。 
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

