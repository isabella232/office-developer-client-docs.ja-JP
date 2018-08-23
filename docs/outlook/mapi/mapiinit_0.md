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
ms.openlocfilehash: 1eb4d7ac8d0287388a1bb76185f23636eddcf809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591675"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[生じます](mapiinitialize.md)にオプションを伝達します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |MAPIX。H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>Members

 **ulVersion**
  
> **MAPIINIT_0**構造体のバージョン番号を表す整数値。 **UlVersion**メンバーは、今後の拡張し、MAPI インターフェイスのバージョンではありません。 現在、 **ulVersion**は、MAPI_INIT_VERSION に設定する必要があります。 
    
 **ulFlags**
  
> MAPI セッションの初期化を制御するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI には、通知の**生じます**を呼び出すために使用する最初のスレッドではなく処理を専用のスレッドを使用して通知を生成する必要があります。
    
MAPI_NT_SERVICE 
  
> 呼び出し元は、Windows サービスとして実行しています。 Windows サービスではこのフラグが設定されていない必要がありますように実行されていない呼び出し元サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。
    
MAPI_NO_COINIT
  
> [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)の呼び出しで COM を初期化するために**生じます**が試みないように、MAPI_NO_COINT フラグを設定します。 **MAPIINIT_0**構造体が渡された場合に**生じます** _ulFlags_ MAPI_NO_COINIT に設定すると、MAPI は、COM が既に初期化されているし、 **CoInitialize**の呼び出しが省略されますと見なされます。
    
## <a name="remarks"></a>注釈

マルチ スレッド クライアントでは、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定する必要があります。 フラグが設定されていない場合**生じます**への最初の呼び出しを行うために使用するスレッドに通知を生成します。 
  
このフラグを設定して、クライアントのスレッドの安全性を実装する方法の詳細については、 [MAPI でのスレッド処理](threading-in-mapi.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)


[MAPI の構造](mapi-structures.md)

