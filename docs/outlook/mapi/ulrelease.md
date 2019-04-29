---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415846"
---
# <a name="ulrelease"></a>UlRelease

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE メソッド**IUnknown:: Release**を呼び出す別の方法を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>パラメーター

 _パンク_
  
> 順番**IUnknown**インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。
    
## <a name="remarks"></a>注釈

参照カウントは、解放されるオブジェクトへの既存のポインターの数です。 
  
_punk_パラメーターが NULL の場合、この関数は**IUnknown:: Release**を呼び出すことなく、すぐに戻ります。
  
 **ulrelease**は、 **IUnknown:: Release**メソッドによって返された値を返します。これは、解放されるオブジェクトの参照カウントと同じにすることができます。 
  
**iunknown:: Release**の詳細については、「 [iunknown インターフェイスを実装する](implementing-the-iunknown-interface.md)」を参照してください。 
  

