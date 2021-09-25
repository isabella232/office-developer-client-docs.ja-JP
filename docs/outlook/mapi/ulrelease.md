---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6411a725ca786f7ae9143d32fc192aa0d721088d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578425"
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
  

