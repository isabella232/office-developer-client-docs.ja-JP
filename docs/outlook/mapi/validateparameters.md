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
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586068"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
パラメーターのクライアント アプリケーションがサービス プロバイダーに渡されますが確認するのには内部の関数を呼び出します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _」方法_
  
> [in]確認する方法を列挙型を指定します。 
    
 _First/先頭のレコード_
  
> [in]スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> すべてのパラメーターは、有効です。 
    
MAPI_E_CALL_FAILED 
  
> 1 つまたは複数のパラメーターが有効ではありません。
    
## <a name="remarks"></a>注釈

[ValidateParms](validateparms.md)マクロでは、 **ValidateParameters**マクロを置き換えられています。 **ValidateParameters**は、RISC プラットフォームで正常に動作しないとしてコンパイルができなきます。 それをコンパイルし、インテルのプラットフォームで正常に動作しますが、すべてのプラットフォームで**ValidateParms**をお勧めします。 
  

