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
  
テーブル行を取得します。
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValue_
  
> [in]取得する行のインデックス列を表すプロパティ値構造へのポインター。 プロパティ値構造体の **ulPropTag** メンバーには [、ITableData](itabledataiunknown.md)実装にアクセスする [CreateTable](createtable.md)関数の呼び出しから _ulPropTagIndexColumn_ パラメーターと同じプロパティ タグを含む必要があります。 
    
 _lppSRow_
  
> [out]取得した行へのポインターを指すポインター。 
    
 _lpuliRow_
  
> [in, out]入力時に、情報を返す必要がないかどうかを示す有効なポインターまたは NULL。 出力時に、行の行番号 (テーブル内の行の位置を識別する連続番号) を指す有効なポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に取得されました。
    
MAPI_E_INVALID_PARAMETER 
  
> [lpSPropValue](spropvalue.md)がポイント _する SPropValue_ 構造体には、index 列プロパティは含めではありません。 
    
## <a name="remarks"></a>注釈

**ITableData::HrQueryRow** メソッドは _、lpSPropValue_ が指すプロパティ構造に含まれるインデックス列の値と一致するインデックス列を持つ行のすべてのプロパティを取得します。 **HrQueryRow** は、呼び出し元が要求した場合、テーブル内の行の位置を識別する行番号も返します。 
  
**HrQueryRow は** _lpSPropValue_ によって指される **SPropValue** 構造体を変更しないので、呼び出し元は **HrQueryRow** が戻る際に構造体を解放する必要があります。 呼び出し元は、取得した行を含む **SRow** 構造も解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

