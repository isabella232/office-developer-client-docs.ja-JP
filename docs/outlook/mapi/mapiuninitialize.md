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
  

