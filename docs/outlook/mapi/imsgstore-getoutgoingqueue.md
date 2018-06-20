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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801009"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**適用されます**: Outlook 
  
発信キュー テーブル、メッセージ ストアの送信キュー内のすべてのメッセージに関する情報が含まれているテーブルへのアクセスを提供します。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppTable_
  
> [out]発信キュー テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 発信キューのテーブルが正常に返されました。
    
## <a name="remarks"></a>備考

**IMsgStore::GetOutgoingQueue**メソッドでは、MAPI スプーラーに送信メッセージのメッセージ ストアのキューを表示するテーブルへのアクセスを提供します。 通常、メッセージは、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出された後、発信キュー テーブルに配置されます。 ただし、提出書類の順序は、前処理およびトランスポート プロバイダーへの送信の順序に影響するためいくつかのメッセージを送信するためにマークされている可能性がありますテーブルに表示されない、送信キューすぐにします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

発信キュー テーブル内の列として含める必要があるプロパティの一覧では、[送信キューのテーブル](outgoing-queue-tables.md)を参照してください。 
  
MAPI スプーラーが送信時の順序を昇順でのメッセージ ストアからメッセージを受け付けるように設計されているためか、この順序と一致または既定の並べ替え順序として設定する発信キュー テーブルを並べ替えるには、MAPI スプーラーを許可します。
  
通知を送信メッセージ キュー テーブルのサポート キューの内容を変更すると、MAPI スプーラーに通知することを確認する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

