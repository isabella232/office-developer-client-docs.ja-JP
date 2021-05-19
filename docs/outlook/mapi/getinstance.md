---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418723"
---
# <a name="getinstance"></a>GetInstance

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数値プロパティ内の 1 つの値を、同じ型の単一値プロパティにコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |MAPIUTIL。H  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>パラメーター

 _pvalMv_
  
> [in]複数値プロパティ [を定義する SPropValue](spropvalue.md) 構造体へのポインター。 
    
 _pvalSv_
  
> [in]データを受信する単一値プロパティへのポインター。 
    
 _uliInst_
  
> [in]  _pvalMv_ パラメーターで示される構造体からコピーされる値のインスタンス番号 (配列要素)。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

コピーされた値が割り当てられたメモリに対して大きすぎる場合 **、GetInstance** 関数は、新しいメモリを割り当てる代わりにポインターのみをコピーします。 
  

