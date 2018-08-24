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
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580734"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
追加または既存のテーブルの先頭に列を移動します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダーです。  <br/> |
   
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
  
> [in]影響を MAPI テーブルへのポインター。
    
 _lpproptagColumnsNew_
  
> [in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む**SPropTagArray**構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> [in]**MAPIAllocateBuffer**関数へのポインター。 メモリの割り当てに使用されます。 
    
 _lpFreeBuffer_
  
> [in]**MAPIFreeBuffer**関数へのポインター。 メモリを解放するために使用します。 
    
## <a name="return-value"></a>戻り値

 **S_OK**
  
> 呼び出しが成功し、指定された列の移動先または追加されました。
    
## <a name="remarks"></a>注釈

**HrAddColumns**関数では、 _lpfnFilterColumns_を NULL に設定で**HrAddColumnsEx**を使用するのと同じです。 
  
## <a name="see-also"></a>関連項目



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

