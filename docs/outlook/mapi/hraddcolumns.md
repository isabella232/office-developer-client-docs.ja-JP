---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800267"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _lptbl_
  
> [in]影響を MAPI テーブルへのポインター。
    
 _lpproptagColumnsNew_
  
> [in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む**SPropTagArray**構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> [in]**MAPIAllocateBuffer**関数へのポインター。 メモリの割り当てに使用されます。 
    
 _lpFreeBuffer_
  
> [in]**MAPIFreeBuffer**関数へのポインター。 メモリを解放するために使用します。 
    
## <a name="return-value"></a>�߂�l

 **S_OK**
  
> 呼び出しが成功し、指定された列の移動先または追加されました。
    
## <a name="remarks"></a>備考

**HrAddColumns**関数では、 _lpfnFilterColumns_を NULL に設定で**HrAddColumnsEx**を使用するのと同じです。 
  
## <a name="see-also"></a>関連項目



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

