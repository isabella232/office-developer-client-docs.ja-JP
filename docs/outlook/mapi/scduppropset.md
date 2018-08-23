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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581980"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI のメモリ、 [ScCopyProps](sccopyprops.md)および[ScCountProps](sccountprops.md)関数の操作を組み合わせることの 1 つのブロックでは、プロパティ値の配列を複製します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]_Rgprop_パラメーターで指定された配列内のプロパティ値の数。 
    
 _rgprop_
  
> [in]重複するプロパティの値を定義する[SPropValue](spropvalue.md)構造体の配列へのポインター。 
    
 _lpAllocateBuffer_
  
> [in]重複配列のメモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _prgprop_
  
> [out]返される複製された**SPropValue**構造体の配列が保存されているメモリ内の最初の位置へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    

