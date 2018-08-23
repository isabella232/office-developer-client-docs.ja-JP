---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: 指定されたエラー メッセージ文字列を取得します。
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799497"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

指定されたエラー メッセージ文字列を取得します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkErrorUnknown](iolkerrorunknown.md)を参照してください。
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>パラメーター

_hr_
  
> [in]参照するエラー コードです。
    
_ppwszError_
  
> [out]対応するエラー メッセージに*hr* 。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)

