---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800437"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**適用されます**: Outlook 
  
Table オブジェクトには、最後に発生したエラーに関する情報を返します。
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in]失敗したメソッドからの戻り値です。
    
 _ulFlags_
  
> [in]使用しないとは、0 (ゼロ) に設定します。
    
 _lppMAPIError_
  
> [out]Table オブジェクトに対して発生した最後のエラーに関する情報を格納する MAPI [MAPIERROR](mapierror.md)構造体へのポインター。 
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

