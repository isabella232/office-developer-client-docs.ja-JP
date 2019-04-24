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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329569"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーに渡されたパラメーターを確認します。 
  
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
  
> 順番検証するメソッドを列挙で指定します。 
    
 _First_
  
> 順番スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> すべてのパラメーターが有効です。 
    
MAPI_E_CALL_FAILED 
  
> 1つ以上のパラメーターが無効です。
    
## <a name="remarks"></a>解説

**validateparameters**マクロは、 [validateparameters](validateparms.md)マクロによって置き換えられました。 **validateparameters**は RISC プラットフォームでは正しく動作せず、これでコンパイルができなくなりました。 これは依然として、Intel プラットフォームではコンパイルされ、正しく動作しますが、すべてのプラットフォームで**validateparms**が推奨されています。 
  

