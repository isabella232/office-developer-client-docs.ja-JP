---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800822"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**適用対象**: Outlook 
  
テーブルの現在の位置にブックマークを作成します。
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>パラメーター

 _lpbkPosition_
  
> [out]返される 32 ビットのブックマークの値へのポインター。 このブックマークは、後で[IMAPITable::SeekRow](imapitable-seekrow.md)メソッドの呼び出しに渡されます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> 要求された操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

**IMAPITable::CreateBookmark**メソッドは、ブックマークと呼ばれる値を作成することによって、テーブルの位置をマークします。 ブックマークで識別される位置に戻るには、ブックマークを使用できます。 ブックマークの位置は、テーブル内で行の位置にあるオブジェクトに関連付けられます。 
  
、添付ファイル テーブルのブックマークがサポートされていませんし、 **CreateBookmark**の添付ファイル テーブルの実装は、MAPI_E_NO_SUPPORT を返します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

ブックマークとカーソルの位置を維持するためのメモリの経費のために作成できるブックマークの数を制限します。 その番号が表示されたら、以降の呼び出しは**CreateBookmark**から MAPI_E_UNABLE_TO_COMPLETE を返します。
  
ブックマークは、不要になったテーブル ・ ビュー内にある行を指しています。 呼び出し元は、このようなブックマークを使用する場合表示されている次の行にカーソルを移動し、停止があります。 
  
呼び出し元が縮小されたために、非表示の行を指しているブックマークを使用しようとするときは、ブックマークに移動した後 MAPI_W_POSITION_CHANGED を返します。 表示されている次の行にブックマークの位置を変更するにはこの時点で、または**SetCollapseState**メソッドで発生した場合、縮小します。 正確に移動するとき、ブックマークされたかを示すブックマークのビットに保持する必要があります、行が折りたたまれている時にブックマークを移動する場合: その最後の使用から、または作成されてから使用されていない場合。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CreateBookmark**は、ブックマークを作成するためのメモリを割り当てます。 [IMAPITable::FreeBookmark](imapitable-freebookmark.md)メソッドを呼び出すことによって、ブックマークのリソースを解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

