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
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326244"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージの到着に関連する情報について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **lな tryid**メンバーによって指摘されたエントリ識別子のバイト数。 
    
 **lて tryid**
  
> 新しく到着したメッセージのエントリ識別子へのポインター。
    
 **cbparentid**
  
> **lpparentid**メンバーによって指摘されたエントリ識別子のバイト数。 
    
 **lpparentid**
  
> 新しく到着したメッセージの受信フォルダーのエントリ識別子へのポインター。
    
 **ulFlags**
  
> メッセージに含まれる文字列プロパティの形式を記述するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 **lpszmessageclass**
  
> 新しく到着したメッセージのメッセージクラスへのポインター。 
    
 **ulmessageflags**
  
> 新しく到着したメッセージの現在の状態を示すフラグのビットマスク。 **ulmessageflags**メンバーは、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティのコピーです。
    
## <a name="remarks"></a>解説

**NEWMAIL_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。 **通知**構造の**info**メンバーに**NEWMAIL_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは fnevNewMail に設定され_ます。_
  
MAPI では、通知シンクの通知イベントに関する情報を保持する**通知**構造のメンバとしてのみ**NEWMAIL_NOTIFICATION**構造が使用されます。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが[imapisupport](imapisupportiunknown.md)メソッドを使用して通知を生成する方法についての説明。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)


[MAPI の構造](mapi-structures.md)

