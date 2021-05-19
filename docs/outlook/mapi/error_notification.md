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
# <a name="error_notification"></a>ERROR_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
重大なエラーに関連する情報を説明します。 これにより、エラー通知が生成されます。 
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> **lpEntryID** が指すエントリ識別子のバイト数です。 
    
 **lpEntryID**
  
> エラーの原因となるオブジェクトのエントリ識別子へのポインター。
    
 **scode**
  
> 重大なエラーのエラー値。 
    
 **ulFlags**
  
> **lpMAPIError** が指す構造体の **lpszError** メンバーが指すテキストの形式を指定するために使用されるフラグのビットマスクです。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 **lpMAPIError**
  
> エラーを説明 [する MAPIERROR](mapierror.md) 構造体へのポインター。 
    
## <a name="remarks"></a>注釈

この **ERROR_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用 **体のメンバー**[の 1](notification.md)つです。 **NOTIFICATION** 構造体 **の info** メンバーに ERROR_NOTIFICATION構造が含まれている場合 **、NOTIFICATION** **構造体** の **ulEventType** メンバーは _fnevCriticalError に設定されます_。
  
**cbEntryID** メンバーと **lpEntryID** メンバーの値には NULL を指定できます。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが **IMAPISupport** メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[�ʒm](notification.md)


[MAPI の構造](mapi-structures.md)

