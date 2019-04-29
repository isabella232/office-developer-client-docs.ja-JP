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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425443"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
重大なエラーに関連する情報について説明します。 これにより、エラー通知が生成されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **lな tryid**で示されるエントリ識別子のバイト数。 
    
 **lて tryid**
  
> エラーを発生させるオブジェクトのエントリ識別子へのポインター。
    
 **scode as scode**
  
> 重大なエラーのエラー値。 
    
 **ulFlags**
  
> **lpMAPIError**によって参照されている構造体で、 **lpszerror**メンバーが指すテキストの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 **lpMAPIError**
  
> エラーを説明する[MAPIERROR](mapierror.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**ERROR_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。 **通知**構造の**info**メンバーに**ERROR_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは_fnevCriticalError_に設定されます。
  
**cbEntryID**メンバーの値と**l tryid**メンバーは NULL にすることができます。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが**imapisupport**メソッドを使用して通知を生成する方法についての説明。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[�ʒm](notification.md)


[MAPI の構造](mapi-structures.md)

