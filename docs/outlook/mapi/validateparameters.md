---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425204"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーに渡したパラメーターを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _eMethod_
  
> [in]列挙で検証するメソッドを指定します。 
    
 _First_
  
> [in]スタックの最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> すべてのパラメーターが有効です。 
    
MAPI_E_CALL_FAILED 
  
> 1 つ以上のパラメーターが無効です。
    
## <a name="remarks"></a>注釈

**ValidateParameters マクロ** は [ValidateParms マクロに取ってかえ](validateparms.md)されています。 **ValidateParameters** は RISC プラットフォームで正しく動作し、コンパイルが行えなくなります。 Intel プラットフォームではコンパイルおよび正常に動作しますが **、ValidateParms は** すべてのプラットフォームで推奨されます。 
  

