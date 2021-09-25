---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 814bd8866863794740aafd553047c6443f192b04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614221"
---
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダー固有のイベントに関連する情報を説明します。 
  
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

## <a name="members"></a>メンバー

 **ulEvent**
  
> プロバイダーによって定義される拡張イベント コード。
    
 **cb**
  
> **pbEventParameters** が指すイベント固有のパラメーターのバイト数です。 
    
 **pbEventParameters**
  
> イベント固有のパラメーターへのポインター。 使用されるパラメーターの種類は **、ulEvent メンバーの値によって異** なります。これらのパラメーターは、イベントを発行したプロバイダーによって文書化されます。 
    
## <a name="remarks"></a>注釈

この **EXTENDED_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md) つです。 **NOTIFICATION** 構造体 **の info** メンバーに EXTENDED_NOTIFICATION構造が含まれている場合 **、NOTIFICATION** 構造体の **ulEventType** メンバーは _fnevExtended に設定されます_。
  
拡張イベントは、他の定義済みイベントではカバーできない変更の種類を表すサービス プロバイダーによって定義されます。 サービス プロバイダーが拡張イベントをサポートすると登録する前に知っているクライアントだけが、そのイベントに登録できます。 サービス プロバイダーが拡張イベントをサポートしている場合、クライアントは高度な知識なしに判断できない。 サービス プロバイダーが拡張イベントをサポートしている場合は、受信時にそのようなイベントを処理する方法を示します。
  
クライアントがログオフすると、セッションによって拡張通知が送信されます。 [IMAPISession::Advise](imapisession-advise.md)を呼び出して、この通知に登録し _、lpEntryID_ パラメーターを NULL に設定し _、cbEntryID_ パラメーターを 0 に設定します。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)


[MAPI の構造](mapi-structures.md)

