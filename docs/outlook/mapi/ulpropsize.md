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
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804151"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**適用対象**: Outlook 
  
1 つのプロパティの値のサイズを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValue_
  
> [in]測定するプロパティを定義する[SPropValue](spropvalue.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

**UlPropSize**関数は、指定されたプロパティのプロパティ値のバイト単位のサイズを返します。 **SPropValue**構造体の残りの部分のサイズを無視します。 
  

