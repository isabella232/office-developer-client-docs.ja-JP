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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429629"
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

## <a name="members"></a>Members

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

