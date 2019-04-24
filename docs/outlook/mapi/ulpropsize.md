---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315303"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つのプロパティ値のサイズを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _lpspropvalue_
  
> 順番測定するプロパティを定義する[spropvalue](spropvalue.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。
    
## <a name="remarks"></a>解説

**ulpropsize**関数は、指定されたプロパティのプロパティ値のサイズをバイト単位で返します。 **spropvalue**構造の残りの部分のサイズは無視されます。 
  

