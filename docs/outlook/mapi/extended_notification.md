---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de9b5e377840b1fbfa3b6dd73fd952c0c72efeb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580643"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーに固有ではイベントに関連する情報をについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>Members

 **ulEvent**
  
> プロバイダーによって定義されている拡張イベント コードです。
    
 **cb**
  
> **PbEventParameters**が指すイベントに固有のパラメーターのバイト数をカウントします。 
    
 **pbEventParameters**
  
> イベント固有のパラメーターへのポインター。 使用されるパラメーターの型は、 **ulEvent**メンバーの値によって異なります。イベントを発行したプロバイダーによっては、これらのパラメーターが記載されています。 
    
## <a name="remarks"></a>注釈

**EXTENDED_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **通知**の構造体のメンバー**情報**には、 **EXTENDED_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、 _fnevExtended_に設定されています。
  
拡張イベントは、他の定義済みのイベントのいずれかで対応できない変更のタイプを表すためのサービス プロバイダーによって定義されます。 拡張イベントをサポートしているサービス プロバイダーを登録する前に知っているクライアントのみがそのイベントに対して登録できます。 クライアント サービス プロバイダーは、拡張イベントをサポートしている高度な知識がないかを確認することはできません。 サービス プロバイダーは、拡張イベントをサポートする場合は、受信したときにこのようなイベントを処理する方法を示します。
  
クライアントがログオフしたときのセッションでは、拡張の通知が送信されます。 _LpEntryID_パラメーターを NULL に設定され、 _cbEntryID_パラメーターを 0 に設定で[IMAPISession::Advise](imapisession-advise.md)を呼び出すことによって、この通知に登録します。 
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービス ・ プロバイダーが通知を生成する[IMAPISupport](imapisupportiunknown.md)メソッドを使用する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)


[MAPI の構造](mapi-structures.md)

