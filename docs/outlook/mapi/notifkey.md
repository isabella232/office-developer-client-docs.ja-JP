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
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280048"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドバイズシンク、アドバイズ元、および MAPI 間の接続を一意に識別します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> **ab**メンバーのバイト数。 
    
 **l**
  
> 通知キーを記述するバイトの配列。
    
## <a name="remarks"></a>解説

[imapisupport](imapisupportiunknown.md)の[Subscribe](imapisupport-subscribe.md)メソッドおよび[Notify](imapisupport-notify.md)メソッドは、 **NOTIFKEY**構造体を使用して、適切なアドバイズソースに関する適切なアドバイズシンクに対する通知を生成します。 
  
サービスプロバイダーは、**アドバイズ**メソッドが呼び出され、通知の登録とその後の通知の送信を処理するために、 **Subscribe**を呼び出すことを希望している場合に通知キーを生成します。 通知キーは、アドバイズ元のエントリ識別子にすることも、定数のような他の識別項目にすることもできます。 たとえば、メッセージストアプロバイダーは、その通知キーとしてフォルダーのパスを使用する場合があります。 
  
通知キーは、複数のプロセス間で機能します。 
  
通知キーのスコープ要件は、長期間のエントリ識別子の場合と似ています。 ただし、エントリ id とは異なり、通知キーはバイナリ比較可能である必要があります。 通常、通知キーには、サービスプロバイダーによって定義された**GUID**値と、その後にオブジェクトに固有の他のプロバイダー固有の情報が含まれます。 
  
**NOTIFKEY**構造を使用して、アドバイズシンクと通知を生成するオブジェクト間の接続を管理する方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

