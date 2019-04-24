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
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279887"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コピー、変更など、変更されたオブジェクトに関する情報を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **lな tryid**メンバーによって指摘されたエントリ識別子のバイト数。 
    
 **lて tryid**
  
> 影響を受けるオブジェクトのエントリ id へのポインター。
    
 **ulobjtype**
  
> 影響を受けるオブジェクトの種類。 可能な種類は次のとおりです。
    
MAPI_STORE 
  
> メッセージストア。 
    
MAPI_ADDRBOOK 
  
> アドレス帳 
    
MAPI_FOLDER 
  
> ].
    
MAPI_ABCONT 
  
> アドレス帳のコンテナー。
    
MAPI_MESSAGE 
  
> メッセージ。
    
MAPI_MAILUSER 
  
> メッセージングユーザー。
    
MAPI_ATTACH 
  
> 資料.
    
MAPI_DISTLIST 
  
> 配布リスト
    
MAPI_PROFSECT 
  
> プロファイルセクション。
    
MAPI_STATUS 
  
> Status オブジェクト。
    
MAPI_SESSION 
  
> Session オブジェクト。
    
 **cbparentid**
  
> **lpparentid**メンバーによって指摘されたエントリ識別子のバイト数。 
    
 **lpparentid**
  
> 影響を受けるオブジェクトの親のエントリ id へのポインター。
    
 **cbold did**
  
> **lpOldID**メンバーによって示されるエントリ識別子のバイト数。 
    
 **lpOldID**
  
> 元のオブジェクトのエントリ識別子へのポインター。 イベントに元のオブジェクトが必要ない場合は、このポインターを NULL にすることができます。
    
 **cbold parentid**
  
> **lpOldParentID**メンバーによって示されるエントリ識別子のバイト数。 
    
 **lpOldParentID**
  
> 元のオブジェクトの親のエントリ id へのポインター。 イベントに元のオブジェクトが必要ない場合は、このポインターを NULL にすることができます。
    
 **lpPropTagArray**
  
> イベントの影響を受けるプロパティを識別するプロパティタグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
## <a name="remarks"></a>解説

**OBJECT_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。 **通知**構造の**info**メンバーに**OBJECT_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは、次のいずれかの種類のイベントに設定されます。 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
fnevSearchComplete イベントの種類で表される検索の完了イベントは、1つの検索フォルダーのドメインの最初の検索が完了したことを示します。
  
元のオブジェクトに関する情報を格納している次のメンバーは、移動イベントとコピーイベントでのみ使用されます。 
  
- **cbold did**
    
- **lpOldID**
    
- **cbold parentid**
    
- **lpOldParentID**
    
これらのメンバーは、他の種類のイベントには適用されません。
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが[imapisupport](imapisupportiunknown.md)メソッドを使用して通知を生成する方法についての説明。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI の構造](mapi-structures.md)

