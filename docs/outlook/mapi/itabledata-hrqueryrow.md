---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ef0dc212a6a6f761cd8dd0cae5312c548c02ae50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583821"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルの行を取得します。
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValue_
  
> [in]取得する行のインデックス列を説明するプロパティ値の構造体へのポインター。 プロパティ値の構造体の**ulPropTag**メンバーは、 [ITableData](itabledataiunknown.md)の実装にアクセスする、 [CreateTable](createtable.md)関数への呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティ タグを含める必要があります。 
    
 _lppSRow_
  
> [out]取得した行へのポインターへのポインター。 
    
 _lpuliRow_
  
> [で [チェック アウト]入力、有効なポインターまたは NULL の場合は、返される情報が必要がないことをことを示します。 出力では、有効なポインターを指す行の行番号、テーブル内の行の位置を示す序数。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行が正常に取得しました。
    
MAPI_E_INVALID_PARAMETER 
  
> [SPropValue](spropvalue.md)構造をその_lpSPropValue_が指すインデックス列のプロパティが含まれていません。 
    
## <a name="remarks"></a>注釈

**ITableData::HrQueryRow**メソッドは、すべての_lpSPropValue_が指すプロパティの構造体に含まれているインデックス列の値に一致するインデックス列を持つ行のプロパティを取得します。 **HrQueryRow**は、呼び出し元が要求した場合、テーブル内の行の位置を識別するにも、行番号を返します。 
  
**HrQueryRow**は、 _lpSPropValue_が指す**SPropValue**構造体を変更しません、ため呼び出し元は、 **HrQueryRow**が返されるときに構造体を解放する必要があります。 呼び出し元では、取得した行を格納する**SRow**構造体を解放する必要がありますも。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

