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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800173"
---
# <a name="getinstance"></a>GetInstance

  
  
**適用対象**: Outlook 
  
同じ型の単一値プロパティに、複数値を持つプロパティ内の 1 つの値をコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |MAPIUTIL。H  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>パラメーター

 _pvalMv_
  
> [in]複数値を持つプロパティを定義する[SPropValue](spropvalue.md)構造体へのポインター。 
    
 _pvalSv_
  
> [in]データを受信する単一値のプロパティへのポインター。 
    
 _uliInst_
  
> [in]インスタンス番号は、 _pvalMv_パラメーターで指定された構造体からコピーされる値の配列要素は、です。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

コピーされる値が割り当てられたメモリに対して大きすぎる場合は、 **GetInstance**関数は新しいメモリの割り当てではなくポインターのみをコピーします。 
  

