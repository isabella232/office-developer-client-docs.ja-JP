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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329009"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の現在の位置にブックマークを作成します。
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>パラメーター

 _lpbkPosition_
  
> 読み上げ返される32ビットのブックマーク値へのポインター。 このブックマークは、後で[IMAPITable:: seekrow](imapitable-seekrow.md)メソッドを呼び出して渡すことができます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> 要求された操作を完了できませんでした。
    
## <a name="remarks"></a>解説

**IMAPITable:: createbookmark**メソッドは、ブックマークと呼ばれる値を作成して、テーブルの位置を示します。 ブックマークを使用すると、ブックマークで指定した位置に戻ることができます。 ブックマーク位置は、テーブルのその行にあるオブジェクトに関連付けられています。 
  
ブックマークは、添付ファイルテーブルではサポートされておらず、 **createbookmark** return MAPI_E_NO_SUPPORT の添付ファイルテーブルの実装ではサポートされていません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

ブックマークを使用してカーソル位置を維持するためのメモリ費用があるため、作成できるブックマークの数を制限します。 その番号に達すると、それ以降のすべての呼び出しから**createbookmark**に MAPI_E_UNABLE_TO_COMPLETE が返されます。
  
ブックマークがテーブルビューに表示されなくなった行を指している場合があります。 呼び出し元がこのようなブックマークを使用する場合は、カーソルを次の表示行に移動し、そこで停止します。 
  
非表示になっているために、呼び出し元がブックマークを使用しようとした場合は、ブックマークを移動した後に MAPI_W_POSITION_CHANGED を返します。 この時点で、または**SetCollapseState**メソッドで折りたたみが行われるときに、ブックマークを次の表示可能な行に再配置することができます。 行が折りたたまれたときにブックマークを移動した場合は、ブックマークが最後に使用された日時、または作成後に使用されていないかどうかを示す、ブックマークのビットを保持する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **createbookmark**は、作成するブックマークのメモリを割り当てます。 [IMAPITable:: freebookmark](imapitable-freebookmark.md)メソッドを呼び出して、ブックマークのリソースを解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

