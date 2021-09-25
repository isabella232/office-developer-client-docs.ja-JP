---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e06dfe806ca3d99f35a369eb4a7cf6fe8da50717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551129"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI DLL の参照カウントをデクレメントし、クリーンアップし、インスタンスごとのグローバル データを削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>パラメーター

なし 
  
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

クライアント アプリケーションは **、MAPIUninitialize** 関数を呼び出して MAPI との対話を終了します [。MAPIInitialize](mapiinitialize.md) 関数の呼び出しで開始します。 **MAPIUninitialize が呼** び出された後、クライアントによって他の MAPI 呼び出しを行う必要はありません。 
  
 **MAPIUninitialize** デクリメントは参照カウントを、対応する **MAPIInitialize** 関数は参照カウントをインクリメントします。 したがって、1 つの関数に対する呼び出しの数は、もう一方の関数への呼び出しの数と等しくする必要があります。 
  
> [!NOTE]
> Win32 **DllMain** 関数またはスレッドを作成または終了するその他の関数内から **MAPIInitialize** または **MAPIUninitialize** を呼び出す必要があります。 詳細については、「Using [Thread-Safe オブジェクト」を参照してください](using-thread-safe-objects.md)。 
  

