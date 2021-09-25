---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6665569b157a874aec248312b30e0528f48c0bcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625190"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドバイス シンク、アドバイス ソース、MAPI の間の接続を一意に識別します。
  
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

## <a name="members"></a>メンバー

 **cb**
  
> ab メンバーのバイト **数** 。 
    
 **ab**
  
> 通知キーを記述するバイトの配列。
    
## <a name="remarks"></a>注釈

[IMAPISupport](imapisupportiunknown.md)の Subscribe メソッドと [Notify](imapisupport-notify.md)メソッドは **、NOTIFKEY** 構造体を使用して、適切なアドバイス ソースに関する適切なアアドバイス シンクへの通知を生成します。 [](imapisupport-subscribe.md) 
  
サービス プロバイダーは **、Advise** メソッドが呼び出され、通知登録とその後の通知の送信を処理するために **Subscribe** を呼び出す場合に通知キーを生成します。 通知キーには、アドバイス ソースのエントリ識別子を指定するか、定数などの他の識別アイテムを指定できます。 たとえば、メッセージ ストア プロバイダーは、フォルダーのパスを通知キーとして使用できます。 
  
通知キーは、複数のプロセスで機能する必要があります。 
  
通知キーのスコープ要件は、長期的なエントリ識別子の要件と似ている。 ただし、エントリ識別子とは異なり、通知キーはバイナリと同等である必要があります。 通常、通知キーには、サービス プロバイダーによって定義された **GUID** 値と、そのオブジェクトに固有の他のプロバイダー固有の情報が含まれます。 
  
**NOTIFKEY** 構造体を使用して、通知を生成するアアドバイス シンクとオブジェクト間の接続を管理する方法については、「サポート イベント通知」[を参照してください](supporting-event-notification.md)。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

