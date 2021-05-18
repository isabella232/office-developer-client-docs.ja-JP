---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414068"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)メソッドの以前の呼び出しによって保存されたデータを使用して、分類されたテーブルの現在の展開状態または折りたたみ状態を再構築します。 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _cbCollapseState_
  
> [in]  _pbCollapseState_ パラメーターが指す構造体内のバイト数。 
    
 _pbCollapseState_
  
> [in]テーブル ビューの再構築に必要なデータを含む構造体へのポインター。
    
 _lpbkLocation_
  
> [out]折りたたみまたは展開された状態を再構築するテーブル内の行を識別するブックマークへのポインター。 [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)への呼び出しで _lpbInstanceKey_ パラメーターに渡されたこのブックマークとインスタンス キーは、同じ行を識別します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 分類されたテーブルの状態が正常に再構築されました。
    
MAPI_E_BUSY 
  
> 操作の開始を妨げる別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> テーブルが折りたたみビューまたは展開ビューの再構築を終了する必要がありました。
    
## <a name="remarks"></a>注釈

**IMAPITable::SetCollapseState** メソッドは、テーブル ビューの展開または折りたたみ状態を再確立します。 **SetCollapseState と** **GetCollapseState は、** 次のように一緒に動作します。 
  
1. 分類されたテーブルの状態が変更され始め [、IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) が呼び出され、変更前の状態に関連するデータをすべて保存します。 
    
2. テーブルのビューを保存された状態に復元するには **、SetCollapseState が** 呼び出されます。 **GetCollapseState によって保存されたデータは** **SetCollapseState に渡されます**。 **SetCollapseState** は、そのデータを使用して状態を復元できます。 
    
3. **SetCollapseState** は **、GetCollapseState** に入力として渡されたインスタンス キーと同じ行を識別するブックマークを出力パラメーターとして返します。
    
分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

並べ替え順序と制限が **GetCollapseState** 呼び出し時とまったく同じことを確認する責任があります。 変更が行われた場合、結果が予測できない可能性があるため **、SetCollapseState** を呼び出す必要があります。 これは、たとえば、クライアントが **GetCollapseState** を呼び出してから **SortTable** を呼び出して **、SetCollapseState** を呼び出す前に並べ替えキーを変更する場合に発生します。 安全を確保するには、復元を進む前に、保存されたデータがまだ有効か確認してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SetCollapseState** を呼び出す場合は、**以前に GetCollapseState** を呼び出している必要があります。 カテゴリを確立する並べ替え順序は、両方のメソッドで同じである必要があります。 並べ替え順序が異なる場合 **、SetCollapseState** 操作の結果は予測できません。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

