---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e3605dc630b6a7bcff46aa3a038d4a4ec7a1f114
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600968"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの現在の位置にブックマークを作成します。
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>パラメーター

 _lpbkPosition_
  
> [out]返される 32 ビットのブックマーク値へのポインター。 このブックマークは、後で [IMAPITable::SeekRow メソッドへの呼び出しで渡](imapitable-seekrow.md) されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> 要求された操作を完了する必要があります。
    
## <a name="remarks"></a>注釈

**IMAPITable::CreateBookmark** メソッドは、ブックマークと呼ばれる値を作成して、テーブルの位置をマークします。 ブックマークを使用すると、ブックマークで識別された位置に戻ります。 ブックマークされた位置は、テーブル内のその行のオブジェクトに関連付けされます。 
  
ブックマークは、添付ファイル テーブルではサポートされていません。 **また、CreateBookmark** 戻り値の添付ファイル テーブルの実装MAPI_E_NO_SUPPORT。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

ブックマークを使用してカーソル位置を維持する場合のメモリコストが大きいので、作成できるブックマークの数を制限します。 その番号に達すると、それ以降のすべての呼びMAPI_E_UNABLE_TO_COMPLETEから **CreateBookmark** を返します。
  
ブックマークは、テーブル ビューに含めなくなった行をポイントする場合があります。 呼び出し元がこのようなブックマークを使用する場合は、カーソルを次の表示行に移動して、そこで停止します。 
  
呼び出し元が、折りたたむため、表示できない行を指しているブックマークを使用しようとすると、ブックマークを移動した後MAPI_W_POSITION_CHANGEDを返します。 この時点で、または **SetCollapseState** メソッドで折りたたみが発生した場合に、ブックマークを次の表示行に再配置できます。 行が折りたたみ時にブックマークを移動する場合は、ブックマークが移動された時刻を正確に示すブックマーク (最後の使用以降、または作成後に使用されたことがない場合) を示す少しを保持する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CreateBookmark は** 、作成するブックマークのメモリを割り当てる。 [IMAPITable::FreeBookmark](imapitable-freebookmark.md)メソッドを呼び出して、ブックマークのリソースを解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

