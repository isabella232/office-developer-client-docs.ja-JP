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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5a5e736e8be1120f5fb90048f01fdc8a44479060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800272"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**適用されます**: Outlook 
  
呼び出し元の実装とイベント通知が開始されるようにコールバック関数で指定されたコンテキストを指定、アドバイズ シンク オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameters

 _lpfnCallback_
  
> [in]MAPI は、新しく作成されたアドバイズ シンクに通知イベントが発生したときに呼び出される[NOTIFCALLBACK](notifcallback.md)プロトタイプに基づいてコールバック関数へのポインター。 
    
 _lpvContext_
  
> [in]呼び出し元のデータへのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。 呼び出し元のデータには、重要では、クライアント、またはプロバイダーにアドレスを表すことができます。 通常、C++ コードでは、 _lpvContext_パラメーターのポインターを表しますオブジェクトのアドレスにします。 
    
 _lppAdviseSink_
  
> [out]アドバイズ シンク オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

**HrAllocAdviseSink**関数を使用するには、クライアント アプリケーションまたはサービス プロバイダーに通知を受け取るオブジェクトを作成、そのオブジェクトを使用する[NOTIFCALLBACK](notifcallback.md)関数のプロトタイプに基づく通知のコールバック関数を作成および_lpvContext_の値として**HrAllocAdviseSink**関数内のオブジェクトへのポインターをパスします。 通知; を実行してこれを行う通知プロセスの一環としては、MAPI はコンテキストとオブジェクトへのポインターでコールバック関数を呼び出します。 
  
MAPI では、その通知エンジンを非同期的に実装します。 C++ では、通知コールバック オブジェクトのメソッドがあります。 通知を生成するオブジェクトがクライアントに提供、または通知を要求するプロバイダーは、オブジェクトのためには、そのオブジェクトの個別の参照カウントを保つ必要があるではない場合は、シンクを案内します。 
  
> [!CAUTION]
> **HrAllocAdviseSink**に限って使ってください。クライアント独自のアドバイズ シンクを作成することができます。 
  

