---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569513"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
新しいメッセージの到着に関連する情報をについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> **LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpEntryID**
  
> 新しく到着したメッセージのエントリの識別子へのポインター。
    
 **cbParentID**
  
> **LpParentID**メンバーが指すエントリの識別子のバイト数をカウントします。 
    
 **lpParentID**
  
> 新しく到着したメッセージの受信フォルダーのエントリの識別子へのポインター。
    
 **ulFlags**
  
> メッセージに含まれている文字列のプロパティの形式を記述するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 **lpszMessageClass**
  
> 新しく到着したメッセージのメッセージ クラスへのポインター。 
    
 **ulMessageFlags**
  
> 新しく到着したメッセージの現在の状態を示すフラグのビットマスクです。 **UlMessageFlags**メンバーは、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティのコピーです。
    
## <a name="remarks"></a>注釈

**NEWMAIL_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **通知**の構造体の**ulEventType**メンバー設定されている**通知**の構造体のメンバー**情報**には、 **NEWMAIL_NOTIFICATION**構造体が含まれている、 _fnevNewMail です_。
  
MAPI では、アドバイズ シンクに通知イベントに関する情報を保持する、**通知**の構造体のメンバーとしてだけ**NEWMAIL_NOTIFICATION**構造体を使用します。 
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)


[MAPI の構造](mapi-structures.md)

