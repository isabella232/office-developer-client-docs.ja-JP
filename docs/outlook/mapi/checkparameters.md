---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2161c68517e2f83e2f2388cf209d464116cac454
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567761"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI によって呼び出されるサービス プロバイダー メソッドのデバッグ パラメーターを検証する内部関数を呼び出します。 
  
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
  
> [in]列挙で検証するメソッドを指定します。 
    
 _First_
  
> [in]スタックの最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

**CheckParameters マクロ** は [CheckParms マクロに取ってかえ](checkparms.md)されています。 **CheckParms は** 、すべてのプラットフォームで推奨されます。 
  

