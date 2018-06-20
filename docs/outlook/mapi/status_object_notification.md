---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804025"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**適用されます**: Outlook 
  
変更によって影響のある状態のオブジェクトについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>メンバー

 **cbEntryID**
  
> **LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpEntryID**
  
> ステータスが変更されたオブジェクトのエントリの識別子へのポインター。
    
 **あう**
  
> **LpPropVals**メンバーが指す配列内の[SPropValue](spropvalue.md)構造体の数です。 
    
 **lpPropVals**
  
> ステータスが変更されたオブジェクトのプロパティを記述する**SPropValue**構造体の配列へのポインター。 
    
## <a name="remarks"></a>備考

**STATUS_OBJECT_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **STATUS_OBJECT_NOTIFICATION**構造体では、イベントの種類の_fnevStatusObjectModified_の状態のオブジェクトの通知に含まれています。 オブジェクトのステータスの通知は、内部の MAPI 通知です。クライアントとサービス ・ プロバイダーは、登録できませんし、サービス ・ プロバイダーが生成できません。
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI でのイベントの通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知をサポートしています。](supporting-event-notification.md) <br/> |サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

