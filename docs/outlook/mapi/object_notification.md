---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 876c8fc3667929e3c2e7403e71e6d392981d34f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573356"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
変更が行われて、次のようにしてコピーまたは変更されたオブジェクトに関する情報が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> **LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpEntryID**
  
> 影響を受けるオブジェクトのエントリの識別子へのポインター。
    
 **ulObjType**
  
> 影響を受けるオブジェクトの種類です。 使用可能な型は次のとおりです。
    
MAPI_STORE 
  
> メッセージ ・ ストアです。 
    
MAPI_ADDRBOOK 
  
> アドレス帳です。 
    
MAPI_FOLDER 
  
> フォルダーです。
    
MAPI_ABCONT 
  
> アドレス帳コンテナーです。
    
MAPI_MESSAGE 
  
> メッセージ。
    
MAPI_MAILUSER 
  
> メッセージングのユーザーです。
    
MAPI_ATTACH 
  
> 添付ファイルです。
    
MAPI_DISTLIST 
  
> 配布リストです。
    
MAPI_PROFSECT 
  
> プロファイル セクションです。
    
MAPI_STATUS 
  
> 状態オブジェクト。
    
MAPI_SESSION 
  
> セッション オブジェクトです。
    
 **cbParentID**
  
> **LpParentID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpParentID**
  
> 影響を受けるオブジェクトの親オブジェクトのエントリの識別子へのポインター。
    
 **cbOldID**
  
> **LpOldID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpOldID**
  
> 元のオブジェクトのエントリの識別子へのポインター。 イベントが元のオブジェクトを必要としない場合は、このポインターを NULL にできます。
    
 **cbOldParentID**
  
> **LpOldParentID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpOldParentID**
  
> 元のオブジェクトの親オブジェクトのエントリの識別子へのポインター。 イベントが元のオブジェクトを必要としない場合は、このポインターを NULL にできます。
    
 **lpPropTagArray**
  
> イベントによって影響を受けるプロパティを識別するプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**OBJECT_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **通知**の構造体のメンバー**情報**には、 **OBJECT_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、次の種類のイベントのいずれかに設定されます。 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
FnevSearchComplete イベントの種類によって表される、検索の完了イベントは、ドメインの 1 つの検索フォルダーを最初に検索が完了したことを示します。
  
元のオブジェクトに関する情報が含まれている次のメンバーは、移動およびコピーのイベントでのみ使用されます。 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
これらのメンバーは、他の種類のイベントには適用されません。
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI の構造](mapi-structures.md)

