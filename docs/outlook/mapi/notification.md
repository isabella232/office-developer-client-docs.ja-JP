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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0d427adde72c24d4ca879c7bd883af09c4ecad53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579971"
---
# <a name="notification"></a>NOTIFICATION
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
イベントが発生したことと、イベントによって影響のあるデータに関する情報が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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

## <a name="members"></a>Members

**ulEventType**
  
> 発生した通知イベントの種類です。 **UlEventType**メンバーの値は、**情報**の共用体に含まれる構造体に対応します。 **UlEventType**メンバーは、次の値のいずれかに設定できます。 
    
 _fnevCriticalError_
  
> セッションの実行中のシャット ダウンなど、グローバル エラーが発生しました。 **情報**のメンバーには、 [ERROR_NOTIFICATION](error_notification.md)構造体が含まれています。 
    
 _fnevExtended_
  
> 特定のサービス プロバイダーによって定義されている内部のイベントが発生しました。 **情報**のメンバーには、 [EXTENDED_NOTIFICATION](extended_notification.md)構造体が含まれています。 
    
 _fnevNewMail_
  
> メッセージが配信されましたが、該当するメッセージ クラスのフォルダーが表示され、処理されるを待っています。 **情報**のメンバーには、 [NEWMAIL_NOTIFICATION](newmail_notification.md)構造体が含まれています。 
    
 _fnevObjectCopied_
  
> MAPI オブジェクトがコピーされました。 **情報**のメンバーには、 [OBJECT_NOTIFICATION](object_notification.md)構造体が含まれています。 
    
 _fnevObjectCreated_
  
> MAPI オブジェクトが用意されています。 **情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevObjectDeleted_
  
> MAPI オブジェクトが削除されました。 **情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevObjectModified_
  
> MAPI オブジェクトが変更されました。 **情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevObjectMoved_
  
> メッセージ ストアやアドレス帳オブジェクトが移動されました。 **情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevSearchComplete_
  
> 検索操作が完了し、結果が保存されます。 **情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。 
    
 _fnevTableModified_
  
> テーブル内の情報が変更されました。 **情報**のメンバーには、 [TABLE_NOTIFICATION](table_notification.md)構造体が含まれています。 
    
**情報**
  
> イベントの特定の種類の影響を受けるデータを記述する通知の構造体の共用体です。 **情報**のメンバーに含まれている構造体は、 **ulEventType**メンバーの値によって異なります。 
    
## <a name="remarks"></a>注釈

1 つまたは複数の**通知**の構造体は、登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すたびに、入力パラメーターとして渡されます。 **通知**の構造体は、発生し、影響を受けるオブジェクトについて説明する特定のイベントに関する情報を格納します。 
  
クライアントまたはサービス プロバイダーが通知の受信の場合は、イベントを処理する構造を使用できます、前に、イベントの種類を確認して、 **ulEventType**メンバーに示されている必要があります。 たとえば、ここでの新しいメッセージと、この種類のイベントを検出すると、到着の確認が表示されているコード サンプルは、メッセージのメッセージ クラスを出力します。 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)

