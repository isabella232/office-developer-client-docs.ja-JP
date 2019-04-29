---
title: itabledatahrqueryrow
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434768"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の行を取得します。
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>パラメーター

 _lpspropvalue_
  
> 順番取得する行のインデックス列を記述するプロパティ値構造へのポインター。 プロパティ値構造の**ulPropTag**メンバーには、 _ulPropTagIndexColumn_パラメーターと同じプロパティタグが含まれている必要があります。この関数は、 [itabledata](itabledataiunknown.md)実装にアクセスする[CreateTable](createtable.md)関数を呼び出します。 
    
 _lppsrow_
  
> 読み上げ取得した行へのポインターへのポインター。 
    
 _lpulirow_
  
> [入力]入力時に、有効なポインターまたは NULL を返します。これは、返される情報がないことを示します。 出力では、行の行番号をポイントする有効なポインターは、テーブル内の行の位置を識別する連続した番号です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に取得されました。
    
MAPI_E_INVALID_PARAMETER 
  
> _lpspropvalue_がポイントする[spropvalue](spropvalue.md)構造に、インデックス列プロパティが含まれていません。 
    
## <a name="remarks"></a>注釈

**itabledata:: hrqueryrow**メソッドは、 _lpspropvalue_が指すプロパティ構造に含まれるインデックス列の値に一致するインデックス列を持つ行のすべてのプロパティを取得します。 **** また、呼び出し元が要求した場合、テーブル内の行の位置を示す行番号も返します。 
  
**hrqueryrow**は、 _lpspropvalue_によって示される**spropvalue**構造体を変更しないので、 **hrqueryrow**が戻るときには、呼び出し元は構造を解放する必要があります。 呼び出し元は、取得した行を含む**srow**構造も解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

