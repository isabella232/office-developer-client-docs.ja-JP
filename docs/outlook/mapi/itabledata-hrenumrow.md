---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348896"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の位置に基づいて行を取得します。 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>パラメーター

 _ulrownumber_
  
> 順番プロパティを返す行の番号を指定します。 _ulrownumber_パラメーターの値には、テーブルの最初の行を示す0から、テーブルの最後の行を示す n-1 までの任意の値を指定できます。 
    
 _lppsrow_
  
> 読み上げ目的の行を記述する[srow](srow.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に取得されたか、 _ulrownumber_パラメーターで指定された行番号の行が存在しません。 
    
## <a name="remarks"></a>解説

**itabledata:: HrEnumRow**メソッドは、連続した番号に基づいて行を取得します。 この数は、挿入の順序 (0 は最初の行を示し、行数から1を引いた数は最後の行を示します) を表します。 MAPI では、この順序で行が挿入され、テーブルデータオブジェクトの有効期間が維持されます。 
  
_ulrownumber_で指定された数値がテーブルの行に対応していない場合、 **HrEnumRow**は S_OK を返し、 _lppsrow_パラメーターを NULL に設定します。 
  
MAPI は、テーブルデータオブジェクトの作成時に[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、返された**srow**構造のメモリを割り当てます。 呼び出し元は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出してこのメモリを解放する必要があります。 
  
テーブルから挿入された順序で行を取得するには、テーブルデータオブジェクトのユーザーは**HrEnumRow**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

