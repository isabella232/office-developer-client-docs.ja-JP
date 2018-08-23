---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800803"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**適用対象**: Outlook 
  
[送受信] ダイアログ ボックスに表示される詳細情報を提供します。 同期中にエラーが発生する場合、ストア プロバイダーは、この関数を呼び出します。
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>パラメーター

 **hResult**
  
> 警告またはエラーの HRESULT。
    
 **pwcszErrorStr**
  
> 表示されるエラーに関連付けられている文字列へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

