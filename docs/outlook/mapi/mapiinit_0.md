---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f94c4b5eac189a672771a91e6b9969462f187ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610126"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPIInitialize 関数にオプションを伝達](mapiinitialize.md)します。 
  
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

## <a name="members"></a>メンバー

 **ulVersion**
  
> 指定した構造体のバージョン番号を表す **MAPIINIT_0** 値。 **ulVersion メンバー** は将来の拡張用であり、MAPI インターフェイスのバージョンを表すのではありません。 現時点では **、ulVersion** を設定する必要MAPI_INIT_VERSION。 
    
 **ulFlags**
  
> MAPI セッションの初期化を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI は、MAPIInitialize を呼び出す最初のスレッドではなく、通知処理専用のスレッドを使用して通知 **を生成する必要があります**。
    
MAPI_NT_SERVICE 
  
> 呼び出し元は、Windowsサービスとして実行されています。 サービスとして実行されていない呼び出し元Windowsこのフラグを設定する必要があります。サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。
    
MAPI_NO_COINIT
  
> **MAPIInitialize** MAPI_NO_COINT呼び出しで COM を初期化しようとしないので、このフラグを [設定します](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)。 MAPIINIT_0 構造体 **が** **mapiInitialize** に渡され  _、ulFlags_ が MAPI_NO_COINIT に設定されている場合、MAPI は COM が既に初期化済みであり **、CoInitialize** への呼び出しをバイパスすると想定します。
    
## <a name="remarks"></a>注釈

マルチスレッド クライアントは、このフラグを設定MAPI_MULTITHREAD_NOTIFICATIONS必要があります。 フラグが設定されていない場合 **、MAPIInitialize** の最初の呼び出しに使用されるスレッドで通知が生成されます。 
  
このフラグを設定する場合と、クライアントでスレッドセーフを実装する方法の詳細については、「MAPI でのスレッド処理 [」を参照してください](threading-in-mapi.md)。 
  
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)


[MAPI の構造](mapi-structures.md)

