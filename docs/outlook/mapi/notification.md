---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eff140179865d662545d0e21ca3789a6e8c2643b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583977"
---
# <a name="notification"></a>NOTIFICATION
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
発生したイベントと、イベントの影響を受けたデータに関する情報を格納します。
  
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

## <a name="members"></a>メンバー

**ulEventType**
  
> 発生した通知イベントの種類。 **ulEventType メンバーの値** は、情報ユニオンに含まれる構造に **対応** します。 **ulEventType メンバー** は、次のいずれかの値に設定できます。 
    
 _fnevCriticalError_
  
> 進行中のセッションのシャットダウンなど、グローバル エラーが発生しました。 info **メンバー** には、新しい構造 [ERROR_NOTIFICATION](error_notification.md) 含まれる。 
    
 _fnevExtended_
  
> 特定のサービス プロバイダーによって定義された内部イベントが発生しました。 info **メンバー** には、新 [しいEXTENDED_NOTIFICATION](extended_notification.md) があります。 
    
 _fnevNewMail_
  
> メッセージがメッセージ クラスの適切な受信フォルダーに配信され、処理を待機しています。 info **メンバー** には、特定の構造 [NEWMAIL_NOTIFICATION](newmail_notification.md) があります。 
    
 _fnevObjectCopied_
  
> MAPI オブジェクトがコピーされました。 info **メンバー** には、次 [のOBJECT_NOTIFICATIONがあります](object_notification.md) 。 
    
 _fnevObjectCreated_
  
> MAPI オブジェクトが作成されました。 info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。 
    
 _fnevObjectDeleted_
  
> MAPI オブジェクトが削除されました。 info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。 
    
 _fnevObjectModified_
  
> MAPI オブジェクトが変更されました。 info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。 
    
 _fnevObjectMoved_
  
> メッセージ ストアまたはアドレス帳オブジェクトが移動されました。 info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。 
    
 _fnevSearchComplete_
  
> 検索操作が完了し、結果を使用できます。 info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。 
    
 _fnevTableModified_
  
> テーブル内の情報が変更されました。 info **メンバー** には、新しい構造 [TABLE_NOTIFICATION](table_notification.md) があります。 
    
**info**
  
> 特定の種類のイベントの影響を受けるデータを記述する通知構造のユニオン。 info メンバーに含まれる構造は **、ulEventType メンバーの値によって異** なります。  
    
## <a name="remarks"></a>注釈

1 つ以上 **の NOTIFICATION** 構造体は、登録されたアアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドへのすべての呼び出しで入力パラメーターとして渡されます。 **NOTIFICATION 構造体** には、発生した特定のイベントに関する情報と、影響を受けるオブジェクトの説明が含まれます。 
  
通知を受け取るクライアントまたはサービス プロバイダーが構造を使用してイベントを処理する前に **、ulEventType** メンバーに示されているイベントの種類を確認する必要があります。 たとえば、次に示すコード サンプルは、新しいメッセージの到着を確認し、この種のイベントを検出すると、メッセージのメッセージ クラスを出力します。 
  
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
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)

