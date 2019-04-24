---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332077"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、MAPI によって呼び出されるサービスプロバイダーメソッドのデバッグパラメーターを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT CheckParameters(
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
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>解説

checkparameters マクロによって**checkparameters**マクロ[](checkparms.md)が置き換えられました。 **checkparms**は、すべてのプラットフォームで推奨されます。 
  

