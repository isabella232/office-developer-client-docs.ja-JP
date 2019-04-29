---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432878"
---
# <a name="notification"></a>NOTIFICATION
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
発生したイベントおよびイベントの影響を受けたデータに関する情報を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a>メンバー

**uleventtype**
  
> 発生した通知イベントの種類。 **uleventtype**メンバーの値は、 **info**ユニオンに含まれている構造に対応しています。 **uleventtype**メンバーは、次のいずれかの値に設定できます。 
    
 _fnevCriticalError_
  
> グローバルなエラーが発生しました。セッションが進行中にシャットダウンされた場合などです。 **info**メンバーには、 [ERROR_NOTIFICATION](error_notification.md)構造体が含まれています。 
    
 _fnevExtended_
  
> 特定のサービスプロバイダーによって定義された内部イベントが発生しました。 **info**メンバーには、 [EXTENDED_NOTIFICATION](extended_notification.md)構造体が含まれています。 
    
 _fnevNewMail_
  
> メッセージは、メッセージクラスの適切な受信フォルダーに配信され、処理を待機しています。 **info**メンバーには、 [NEWMAIL_NOTIFICATION](newmail_notification.md)構造体が含まれています。 
    
 _fnevObjectCopied_
  
> MAPI オブジェクトがコピーされました。 **info**メンバーには、 [OBJECT_NOTIFICATION](object_notification.md)構造体が含まれています。 
    
 _fnevObjectCreated_
  
> MAPI オブジェクトが作成されました。 **info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevObjectDeleted_
  
> MAPI オブジェクトが削除されました。 **info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevObjectModified_
  
> MAPI オブジェクトが変更されました。 **info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevObjectMoved_
  
> メッセージストアまたはアドレス帳オブジェクトが移動されました。 **info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevSearchComplete_
  
> 検索操作が終了し、結果を使用できるようになります。 **info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevTableModified_
  
> テーブル内の情報が変更されました。 **info**メンバーには、 [TABLE_NOTIFICATION](table_notification.md)構造体が含まれています。 
    
**info**
  
> 特定の種類のイベントの影響を受けるデータを記述する通知構造の和集合。 **info**メンバーに含まれる構造は、 **uleventtype**メンバーの値に依存します。 
    
## <a name="remarks"></a>注釈

登録されたアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドへのすべての呼び出しで、1つ以上の**通知**構造が入力パラメーターとして渡されます。 **通知**構造には、発生した特定のイベントに関する情報が含まれ、影響を受けるオブジェクトについて説明します。 
  
通知を受け取るクライアントまたはサービスプロバイダーは、構造体を使用してイベントを処理する前に、 **uleventtype**メンバーに示されているように、イベントの種類を確認する必要があります。 たとえば、次に示すコードサンプルでは、新しいメッセージの到着をチェックし、この種のイベントを検出すると、メッセージのメッセージクラスを出力します。 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが[imapisupport](imapisupportiunknown.md)メソッドを使用して通知を生成する方法についての説明。  <br/> |
   
## <a name="see-also"></a>関連項目


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)

