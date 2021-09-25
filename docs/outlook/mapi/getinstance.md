---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f320ebf3311e2227a2969086606d3b3e592d6e63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551570"
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
  

