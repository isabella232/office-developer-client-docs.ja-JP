---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: faf7ce0488584168ca0a73c13c835b18c5f89472
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566256"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つのプロパティ値のサイズを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValue_
  
> [in]測定するプロパティを定義する [SPropValue](spropvalue.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。
    
## <a name="remarks"></a>注釈

**UlPropSize** 関数は、指定したプロパティのプロパティ値のサイズをバイト単位で返します。 SPropValue 構造体の残りのサイズ **は無視** されます。 
  

