---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 670c5000d3bebc6723b37a5bce9821fdb069f78a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561671"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存のテーブルの先頭に列を追加または移動します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー。  <br/> |
   
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
  
> [in]影響を受ける MAPI テーブルへのポインター。
    
 _lpproptagColumnsNew_
  
> [in]テーブルの先頭に追加または移動するプロパティのプロパティ タグの配列を含む **SPropTagArray** 構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> [in] **MAPIAllocateBuffer 関数への** ポインター。 メモリの割り当てに使用されます。 
    
 _lpFreeBuffer_
  
> [in] **MAPIFreeBuffer 関数への** ポインター。 メモリを解放するために使用します。 
    
## <a name="return-value"></a>戻り値

 **S_OK**
  
> 呼び出しが成功し、指定された列が移動または追加されました。
    
## <a name="remarks"></a>注釈

**HrAddColumns 関数** は _、lpfnFilterColumns_ が NULL に設定された **HrAddColumnsEx** を使用するのと同じです。 
  
## <a name="see-also"></a>関連項目



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

