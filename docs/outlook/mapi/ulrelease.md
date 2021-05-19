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
  
OLE メソッド **IUnknown::Release を呼び出す別の方法を提供します**。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>パラメーター

 _punk_
  
> [in] **IUnknown** インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。
    
## <a name="remarks"></a>注釈

参照カウントは、解放するオブジェクトへの既存のポインターの数です。 
  
punk _パラメーターが_ NULL の場合、関数は **IUnknown::Release** を呼び出さずに直ちに返します。
  
 **UlRelease** は **、IUnknown::Release** メソッドによって返される値を返します。これは、解放するオブジェクトの参照カウントと等しい場合があります。 
  
**IUnknown::Release** の詳細については [、「IUnknown インターフェイスの実装」を参照してください](implementing-the-iunknown-interface.md)。 
  

