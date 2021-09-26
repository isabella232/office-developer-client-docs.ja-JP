---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e2df45a2955182639cf0e551d914d95476762e41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629453"
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
  

