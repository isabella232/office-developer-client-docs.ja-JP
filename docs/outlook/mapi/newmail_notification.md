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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439857"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージの到着に関連する情報を説明します。 
  
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
  
> **lpEntryID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpEntryID**
  
> 新しく到着したメッセージのエントリ識別子へのポインター。
    
 **cbParentID**
  
> **lpParentID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpParentID**
  
> 新しく到着したメッセージの受信フォルダーのエントリ識別子へのポインター。
    
 **ulFlags**
  
> メッセージに含まれる文字列プロパティの形式を記述するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 **lpszMessageClass**
  
> 新しく到着したメッセージのメッセージ クラスへのポインター。 
    
 **ulMessageFlags**
  
> 新しく到着したメッセージの現在の状態を表すフラグのビットマスク。 **ulMessageFlags** メンバーは、メッセージのプロパティ [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md) **PR_MESSAGE_FLAGSコピーです**。
    
## <a name="remarks"></a>注釈

この **NEWMAIL_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md) つです。 **NOTIFICATION** 構造体 **の info** メンバーに、NEWMAIL_NOTIFICATION構造が含まれている場合 **、NOTIFICATION** 構造体の **ulEventType** メンバーは _fnevNewMail に設定されます。_
  
MAPI は **、NEWMAIL_NOTIFICATION** 通知シンクの通知イベントに関する情報を保持する **NOTIFICATION** 構造体のメンバーとしてのみ使用します。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)


[MAPI の構造](mapi-structures.md)

