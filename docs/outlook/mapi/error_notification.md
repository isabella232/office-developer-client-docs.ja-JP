---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800020"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**適用されます**: Outlook 
  
重大なエラーに関連する情報をについて説明します。 これが原因でエラーの通知を生成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a>メンバー

 **cbEntryID**
  
> **LpEntryID**で示されるエントリの識別子のバイト数をカウントします。 
    
 **lpEntryID**
  
> エラーが発生するオブジェクトのエントリの識別子へのポインター。
    
 **scode**
  
> 重大なエラーのエラー値です。 
    
 **ulFlags**
  
> **LpMAPIError**が指す構造体の**lpszError**メンバーが指す文字列の書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 **lpMAPIError**
  
> エラーを説明する[MAPIERROR](mapierror.md)構造体へのポインター。 
    
## <a name="remarks"></a>備考

**ERROR_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **通知**の構造体のメンバー**情報**には、 **ERROR_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、 _fnevCriticalError_に設定されています。
  
**CbEntryID**メンバーと**lpEntryID**メンバーの値は NULL であることができます。 
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI でのイベントの通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知をサポートしています。](supporting-event-notification.md) <br/> |サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[�ʒm](notification.md)


[MAPI の構造](mapi-structures.md)
