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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6c149a215a048b96408025e08df55972fa989f46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801215"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**適用対象**: Outlook 
  
テーブル内の位置に基づいて行を取得します。 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>パラメーター

 _ulRowNumber_
  
> [in]プロパティを返す対象の行の数です。 _UlRowNumber_パラメーターの値は 0 から n までの 1、テーブルの最後の行を示す、テーブルの最初の行から任意の値にできます。 
    
 _lppSRow_
  
> [out]対象の行を記述する[SRow](srow.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行が正常に取得されたか、 _ulRowNumber_パラメーターで指定された行番号の行が存在しません。 
    
## <a name="remarks"></a>注釈

**ITableData::HrEnumRow**メソッドは、序数に基づく行を取得します。 この番号は、挿入の順序を表します (最初の行は 0 し、-1 行の数は、最後の行を示します)。 MAPI では、この時系列テーブルのデータ オブジェクトの有効期間の行を挿入の順序を維持します。 
  
番号で指定された_ulRowNumber_は、テーブル内の行には対応していない、 **HrEnumRow**は S_OK を返し、 _lppSRow_パラメーターを NULL に設定します。 
  
MAPI では、テーブルのデータ オブジェクトが作成されたときに[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、返された**SRow**構造体のメモリを割り当てます。 呼び出し元は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって、このメモリを解放する必要があります。 
  
挿入された順序で、テーブルから行を取得するためには、テーブルのデータ オブジェクトのユーザーは、 **HrEnumRow**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

