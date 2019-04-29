---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428901"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し側の実装によって指定されたコンテキストと、イベント通知によってトリガーされるコールバック関数を指定して、アドバイズシンクオブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>パラメーター

 _lpfnCallback_
  
> 順番新しく作成されたアドバイズシンクに対して通知イベントが発生したときに MAPI が呼び出す[NOTIFCALLBACK](notifcallback.md)プロトタイプに基づく、コールバック関数へのポインター。 
    
 _lpvcontext_
  
> 順番MAPI がコールバック関数に渡す、呼び出し元データへのポインター。 発信者データは、クライアントまたはプロバイダーの重要度のアドレスを表すことができます。 通常、C++ コードの場合、 _lpvcontext_パラメーターはオブジェクトのアドレスへのポインターを表します。 
    
 _lppAdviseSink_
  
> 読み上げアドバイズシンクオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

**HrAllocAdviseSink**関数を使用するために、クライアントアプリケーションまたはサービスプロバイダーは通知を受信するオブジェクトを作成し、そのオブジェクトに含まれる[NOTIFCALLBACK](notifcallback.md)関数プロトタイプに基づいて通知コールバック関数を作成します。を指定し、 **HrAllocAdviseSink**関数内のオブジェクトへのポインターを_lpvcontext_値として渡します。 これにより通知が行われます。通知処理の一環として、MAPI はオブジェクトポインターをコンテキストとしてコールバック関数を呼び出します。 
  
MAPI は、通知エンジンを非同期的に実装します。 C++ では、通知コールバックはオブジェクトメソッドにすることができます。 通知を生成するオブジェクトが存在しない場合は、通知を要求しているクライアントまたはプロバイダーは、オブジェクトのアドバイズシンクに対して、そのオブジェクトに対して個別の参照カウントを保持する必要があります。 
  
> [!CAUTION]
> **HrAllocAdviseSink**は控えめに使用する必要があります。クライアントが独自のアドバイズシンクを作成することは安全です。 
  

