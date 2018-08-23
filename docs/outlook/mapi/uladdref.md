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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592374"
---
# <a name="uladdref"></a>UlAddRef

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
OLE メソッド**IUnknown::AddRef**を起動する別の方法を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>パラメーター

 _パンク_
  
> [in]インターフェイスへのポインターは、任意の MAPI インターフェイスに、 **IUnknown**インターフェイスから派生します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

 **UlAddRef**は、インターフェイスの参照カウントの新しい値では、 **IUnknown::AddRef**メソッドによって返される値を返します。 値は、0 以外の値です。 
  
**IUnknown::AddRef**の詳細については、 [IUnknown インターフェイスを実装する](implementing-the-iunknown-interface.md)を参照してください。 
  

