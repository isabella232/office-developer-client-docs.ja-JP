---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357296"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPIInitialize](mapiinitialize.md)関数にオプションを伝えます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix。H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>Members

 **ulversion**
  
> **MAPIINIT_0**構造体のバージョン番号を表す整数値。 **ulversion**メンバは将来の拡張のためのものであり、MAPI インターフェイスのバージョンを表すものではありません。 現時点では、 **ulversion**を MAPI_INIT_VERSION に設定する必要があります。 
    
 **ulFlags**
  
> MAPI セッションの初期化を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI では、 **MAPIInitialize**を呼び出すために使用される最初のスレッドではなく、通知処理専用のスレッドを使用して通知を生成する必要があります。
    
MAPI_NT_SERVICE 
  
> 発信者が Windows サービスとして実行されている。 Windows サービスとして実行されていない発信者は、このフラグを設定してはなりません。サービスとして実行されている発信者は、このフラグを設定する必要があります。
    
MAPI_NO_COINIT
  
> MAPI_NO_COINT フラグを設定して、 **MAPIInitialize**が[CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)の呼び出しで COM を初期化しないようにします。 _ulflags_が MAPI_NO_COINIT に設定されている場合、 **MAPIINIT_0**構造体が**MAPIInitialize**に渡されると、MAPI は COM が既に初期化されていると見なし、 **CoInitialize**の呼び出しをバイパスします。
    
## <a name="remarks"></a>解説

マルチスレッドクライアントでは、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定する必要があります。 フラグが設定されていない場合、 **MAPIInitialize**への最初の呼び出しを行うために使用されるスレッドで通知が生成されます。 
  
このフラグを設定する状況と、クライアントにスレッドセーフを実装する方法の詳細については、「 [MAPI でのスレッド処理](threading-in-mapi.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)


[MAPI の構造](mapi-structures.md)

