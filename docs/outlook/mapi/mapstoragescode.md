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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8dbb871a234d94f8bb2e21b15ce5de6f0db0e4ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581833"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
SCODE のマップでは、HRESULT の種類に OLE ストレージ オブジェクトから値を返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>パラメーター

 _StgSCode_
  
> [in]SCODE の MAPI では、HRESULT の値にマップされる OLE ストレージ オブジェクトから値を返します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値が返されます。
    
MAPI_E_CALL_FAILED 
  
> 関数は、一致する値を見つけることができません。
    
## <a name="remarks"></a>注釈

MAPI は、DLL のメッセージで、メッセージの実装を基本の MAPI コンポーネントの内部使用のため、 **MapStorageSCode**関数を提供します。 これらのコンポーネント ファイルを開く OLE ストレージ自体、HRESULT 値を OLE ストレージの問題を返されるエラー値をマップできる必要があります。 
  
詳細については、[構造化ストレージ](structured-storage-in-mapi.md)を参照してください。 
  

