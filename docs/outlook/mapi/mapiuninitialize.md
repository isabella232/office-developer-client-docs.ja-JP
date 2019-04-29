---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408524"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI DLL のインスタンスごとのグローバルデータを、参照カウント、クリーンアップ、削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
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

クライアントアプリケーションは、 **MAPIUninitialize**関数を呼び出して MAPI との対話を終了させるため、 [MAPIInitialize](mapiinitialize.md)関数の呼び出しから開始されます。 **MAPIUninitialize**を呼び出した後、クライアントは他の MAPI 呼び出しを行うことはできません。 
  
 **MAPIUninitialize**は参照カウントをデクリメントし、対応する**MAPIInitialize**関数が参照カウントをインクリメントします。 そのため、1つの関数への呼び出しの数は、もう一方への呼び出しの数と等しくなければなりません。 
  
> [!NOTE]
> **MAPIInitialize**または**MAPIUninitialize**は、Win32 **DllMain**関数から、またはスレッドを作成または終了する他の関数内から呼び出すことはできません。 詳細については、「[スレッドセーフオブジェクトの使用](using-thread-safe-objects.md)」を参照してください。 
  

