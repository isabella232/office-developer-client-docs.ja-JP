---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a92089c9df921259b0df638ec94b118fa53276cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613927"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル オブジェクトで発生した最後のエラーに関する情報を返します。
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]失敗したメソッドからの戻り値。
    
 _ulFlags_
  
> [in]使用しない、0 (ゼロ) に設定します。
    
 _lppMAPIError_
  
> [out]テーブル オブジェクトに対して発生した最後のエラーに関する情報を含む [MAPI MAPIERROR](mapierror.md) 構造体をポイントします。 
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

