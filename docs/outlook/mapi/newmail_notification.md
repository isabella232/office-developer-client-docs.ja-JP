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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801656"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

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
    
## <a name="remarks"></a>備考

**NEWMAIL_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **通知**の構造体の**ulEventType**メンバー設定されている**通知**の構造体のメンバー**情報**には、 **NEWMAIL_NOTIFICATION**構造体が含まれている、 _fnevNewMail です_。
  
MAPI では、アドバイズ シンクに通知イベントに関する情報を保持する、**通知**の構造体のメンバーとしてだけ**NEWMAIL_NOTIFICATION**構造体を使用します。 
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI でのイベントの通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知をサポートしています。](supporting-event-notification.md) <br/> |サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[PidTagMessageFlags の標準的なプロパティ](pidtagmessageflags-canonical-property.md)


[MAPI の構造](mapi-structures.md)

