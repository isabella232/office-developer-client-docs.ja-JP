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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426269"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
変更によって影響を受けた状態オブジェクトを示します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **lな tryid**メンバーによって指摘されたエントリ識別子のバイト数。 
    
 **lて tryid**
  
> 変更された状態オブジェクトのエントリ識別子へのポインター。
    
 **cvalues**
  
> **lppropvals**メンバーによって参照されている、配列内の[spropvalue](spropvalue.md)構造体の数。 
    
 **lppropvals**
  
> 変更されたステータスオブジェクトのプロパティを記述する**spropvalue**構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**STATUS_OBJECT_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。 **STATUS_OBJECT_NOTIFICATION**構造体は、 _fnevStatusObjectModified_型のイベントに対するステータスオブジェクト通知に含まれています。 状態オブジェクト通知は MAPI の内部通知です。クライアントおよびサービスプロバイダーはそれを登録できず、サービスプロバイダーはそれを生成できません。
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが**imapisupport**メソッドを使用して通知を生成する方法についての説明。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

