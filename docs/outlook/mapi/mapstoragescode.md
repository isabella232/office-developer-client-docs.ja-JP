---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 078c05c0f3355e633ab7edaed577c99b4c2a33b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595708"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
マップ OLE ストレージ オブジェクトから HRESULT 型に SCODE 戻り値を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>パラメーター

 _StgSCode_
  
> [in]HRESULT 値にマップする OLE ストレージ オブジェクトからの MAPI SCODE 戻り値。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値を返しました。
    
MAPI_E_CALL_FAILED 
  
> 関数は一致する値を見つけ出しません。
    
## <a name="remarks"></a>注釈

MAPI は、メッセージの実装をメッセージ DLL に基付け、MAPI コンポーネントを内部的に使用する **MapStorageSCode** 関数を提供します。 これらのコンポーネントは OLE ストレージ自体を開いているため、OLE ストレージの問題で返されるエラー値を HRESULT 値にマップできる必要があります。 
  
詳細については[、「Structured Storage」 を参照してください](structured-storage-in-mapi.md)。 
  

