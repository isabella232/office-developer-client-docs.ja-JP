---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432836"
---
# <a name="uladdref"></a>UlAddRef

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE メソッド **IUnknown::AddRef を呼び出す別の方法を提供します**。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>パラメーター

 _punk_
  
> [in] **IUnknown** インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。
    
## <a name="remarks"></a>注釈

 **UlAddRef** は、インターフェイスの参照カウントの新しい値である **IUnknown::AddRef** メソッドによって返される値を返します。 値は 0 以外です。 
  
**IUnknown::AddRef** の詳細については [、「IUnknown インターフェイスの実装」を参照してください](implementing-the-iunknown-interface.md)。 
  

