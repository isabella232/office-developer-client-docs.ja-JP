---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348196"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存の表の先頭に列を追加または移動します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー。  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lptbl_
  
> 順番影響を受ける MAPI テーブルへのポインター。
    
 _lpproptagColumnsNew_
  
> 順番表の先頭に追加または移動するプロパティのプロパティタグの配列を含む**SPropTagArray**構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> 順番**MAPIAllocateBuffer**関数へのポインター。 メモリの割り当てに使用されます。 
    
 _lpfreebuffer_
  
> 順番**MAPIFreeBuffer**関数へのポインター。 メモリを解放するために使用します。 
    
## <a name="return-value"></a>戻り値

 **S_OK**
  
> 呼び出しが成功し、指定された列が移動または追加されました。
    
## <a name="remarks"></a>解説

**hraddcolumns**関数は、 _lpfnFilterColumns_が NULL に設定されている**hraddcolumnsex**を使用するのと同じです。 
  
## <a name="see-also"></a>関連項目



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

