---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0bbd881b194ed3b2b94758f9e8a25eaf1e869c3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614060"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元の実装で指定されたコンテキストと、イベント通知によってトリガーされるコールバック関数を指定して、アアドバイス シンク オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>パラメーター

 _lpfnCallback_
  
> [in]新しく作成されたアアドバイス シンクの通知イベントが発生した場合に MAPI が呼び出す [NOTIFCALLBACK](notifcallback.md) プロトタイプに基づくコールバック関数へのポインター。 
    
 _lpvContext_
  
> [in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される呼び出し元データへのポインター。 呼び出し元データは、クライアントまたはプロバイダーにとって重要なアドレスを表すことができます。 通常、C++ コードの場合  _、lpvContext_ パラメーターはオブジェクトのアドレスへのポインターを表します。 
    
 _lppAdviseSink_
  
> [out]アアドバイス シンク オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

**HrAllocAdviseSink** 関数を使用するには、クライアント アプリケーションまたはサービス プロバイダーが通知を受け取るオブジェクトを作成し、そのオブジェクトに対応する [NOTIFCALLBACK](notifcallback.md)関数プロトタイプに基づいて通知コールバック関数を作成し **、HrAllocAdviseSink** 関数内のオブジェクトへのポインターを _lpvContext_ 値として渡します。 通知を実行します。通知プロセスの一部として、MAPI はオブジェクト ポインターをコンテキストとしてコールバック関数を呼び出します。 
  
MAPI は、通知エンジンを非同期的に実装します。 C++ では、通知コールバックにはオブジェクト メソッドを指定できます。 通知を生成するオブジェクトが存在しない場合、通知を要求するクライアントまたはプロバイダーは、オブジェクトのアアドバイス シンクに対して、そのオブジェクトの個別の参照カウントを保持する必要があります。 
  
> [!CAUTION]
> **HrAllocAdviseSink を** 使用する必要があります。クライアントが独自のアドバイス シンクを作成する方が安全です。 
  

