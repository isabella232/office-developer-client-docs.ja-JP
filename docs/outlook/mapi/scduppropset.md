---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406018"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ScCopyProps](sccopyprops.md)関数と[ScCountProps](sccountprops.md)関数の操作を組み合わせた MAPI メモリの 1 つのブロック内のプロパティ値配列を複製します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>パラメーター

 _cprop_
  
> [in]rgprop パラメーターで示される配列内の  _プロパティ値の_ 数。 
    
 _rgprop_
  
> [in]重複するプロパティ値を [定義する SPropValue](spropvalue.md) 構造体の配列へのポインター。 
    
 _lpAllocateBuffer_
  
> [in]重複した配列のメモリを割り当てるのに使用する [MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _prgprop_
  
> [out] **SPropValue** 構造体の返された重複配列が格納されているメモリ内の最初の位置へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    

