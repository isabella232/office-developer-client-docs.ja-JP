---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416525"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
SCODE 戻り値を OLE ストレージオブジェクトから HRESULT 型にマップします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>パラメーター

 _StgSCode_
  
> 順番MAPI の HRESULT 値にマップされる OLE ストレージオブジェクトからの戻り値。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予期される値が返されました。
    
MAPI_E_CALL_FAILED 
  
> 関数は、一致する値を見つけることができません。
    
## <a name="remarks"></a>注釈

mapi では、メッセージ DLL のメッセージの実装に基づいて mapi コンポーネントを内部で使用するための**mapstoragescode**関数が提供されます。 これらのコンポーネントは ole ストレージ自体を開くため、ole 記憶域に関する問題に返されるエラー値を HRESULT 値にマップできる必要があります。 
  
詳細については、「[構造化ストレージ](structured-storage-in-mapi.md)」を参照してください。 
  

