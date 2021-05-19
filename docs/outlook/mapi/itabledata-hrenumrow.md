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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418373"
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

 _ulRowNumber_
  
> [in]プロパティを返す行の数。 _ulRowNumber_ パラメーターの値には、表の最初の行を示す 0 から、表の最後の行を示す n ~ 1 の任意の値を指定できます。 
    
 _lppSRow_
  
> [out]ターゲット行を表す [SRow](srow.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に取得されたか  _、ulRowNumber_ パラメーターで指定された行番号の行が存在しません。 
    
## <a name="remarks"></a>注釈

**ITableData::HrEnumRow** メソッドは、順次番号に基づいて行を取得します。 この数値は、挿入の順序を表します (0 は最初の行を示し、行数から 1 を引いた数は最後の行を示します)。 MAPI は、テーブル データ オブジェクトの有効期間の間、行の挿入のこの時系列の順序を維持します。 
  
_ulRowNumber_ で指定された番号がテーブル内の行に対応していない場合 **、HrEnumRow** は S_OK を返し _、lppSRow_ パラメーターを NULL に設定します。 
  
MAPI は、テーブル データ オブジェクトの作成時に [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、返される **SRow** 構造体のメモリを割り当てる。 呼び出し元は [、MAPIFreeBuffer 関数を呼び出して、このメモリを解放する必要](mapifreebuffer.md) があります。 
  
テーブルから挿入された順序で行を取得するには、テーブル データ オブジェクトのユーザーが **HrEnumRow メソッドを呼び出** します。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

