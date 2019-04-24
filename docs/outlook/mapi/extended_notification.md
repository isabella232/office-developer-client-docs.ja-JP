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
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341119"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダー固有のイベントに関連する情報について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>Members

 **ulevent**
  
> プロバイダーによって定義された拡張イベントコード。
    
 **cb**
  
> **p傾斜 entparameters**で示されるイベント固有のパラメーターのバイト数。 
    
 **p斜め entparameters**
  
> イベント固有のパラメーターへのポインター。 使用されるパラメーターの型は**ulevent**メンバーの値に依存します。これらのパラメーターは、イベントを発行したプロバイダーによってドキュメント化されます。 
    
## <a name="remarks"></a>解説

**EXTENDED_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。 **通知**構造の**info**メンバーに**EXTENDED_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは_fnevExtended_に設定されます。
  
拡張イベントは、サービスプロバイダーによって定義され、他のどの定義済みイベントによってもカバーできない変更の種類を表します。 サービスプロバイダーが拡張イベントをサポートすることを登録する前に知っているクライアントのみが、そのイベントの登録を行うことができます。 サービスプロバイダーが拡張イベントをサポートしている場合、クライアントは高度な知識がなくても判断できません。 サービスプロバイダーが拡張イベントをサポートしている場合は、受信時にこのようなイベントを処理する方法を示しています。
  
クライアントがログオフすると、セッションによって拡張通知が送信されます。 この通知を登録するには、 _lpentryid_パラメーターを NULL に設定し、 _cbEntryID_パラメーターを0に設定して、 [imapitryid](imapisession-advise.md)パラメーターを呼び出します。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが[imapisupport](imapisupportiunknown.md)方法を使用して通知を生成する方法についての説明。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)


[MAPI の構造](mapi-structures.md)

