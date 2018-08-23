---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 36b8381e2bf98f5ddcb88a54b56f2b5c91b3b668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572600"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドバイズ シンク、アドバイズ ソースと MAPI との間の接続を一意に識別します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> **Ab**メンバーのバイト数をカウントします。 
    
 **ab**
  
> 通知キーを記述するバイトの配列です。
    
## <a name="remarks"></a>注釈

[IMAPISupport](imapisupportiunknown.md)の[購読](imapisupport-subscribe.md)と[通知](imapisupport-notify.md)方法は、適切なアドバイスのソースに関する適切なアドバイズ シンクに通知を生成するのに**NOTIFKEY**構造体を使用します。 
  
サービスのプロバイダーは、**そのメソッド**が呼び出され、通知の登録と通知のそれ以降の送信を処理するために**購読**を呼び出すときに通知キーを生成します。 アドバイズ ソースのエントリ id は、通知のキーまたは定数などの他の識別項目を指定できます。 などのメッセージ ストア プロバイダーでは、その通知キーとしてフォルダーのパスを使用する可能性があります。 
  
通知キーは、複数のプロセス間で動作するはずです。 
  
通知キーのスコープ要件では、長期のエントリ id のようになります。 ただし、エントリの識別子とは異なり通知キーをバイナリ比較する必要があります。 通常、通知のキーには、オブジェクトに固有の他のプロバイダー固有情報の後にサービス ・ プロバイダーによって定義された**GUID**の値が含まれています。 
  
管理する**NOTIFKEY**構造体の使用の詳細については、通知を生成するオブジェクトとアドバイズ シンクの接続には、[イベント通知をサポートしている](supporting-event-notification.md)が参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

