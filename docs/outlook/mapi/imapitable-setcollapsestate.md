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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328834"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
以前の[IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md)メソッドの呼び出しによって保存されたデータを使用して、カテゴリ化されたテーブルの現在の展開状態または折りたたみ状態を再構築します。 
  
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
  
> 予約語0である必要があります。
    
 _cbCollapseState_
  
> 順番_pbCollapseState_パラメーターによって参照されている構造体のバイト数。 
    
 _pbCollapseState_
  
> 順番テーブルビューを再構築するために必要なデータを含む構造体へのポインター。
    
 _lpbkLocation_
  
> 読み上げ折りたたまれているか展開された状態を示す、テーブル内の行を識別するブックマークへのポインター。 このブックマークとインスタンスキーが[IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md)の呼び出しで_lpbInstanceKey_パラメーターに渡された場合、同じ行を識別します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> カテゴリ化されたテーブルの状態が正常に再構築されました。
    
MAPI_E_BUSY 
  
> 操作が開始されないように、別の操作が進行中です。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> テーブルで、折りたたまれたビューまたは展開されたビューの再構築を完了できませんでした。
    
## <a name="remarks"></a>解説

**IMAPITable:: SetCollapseState**メソッドは、テーブルビューの展開または折りたたみ状態を再度確立します。 **SetCollapseState**と**GetCollapseState**は、次のように連携して動作します。 
  
1. カテゴリ内のテーブルの状態が変更されるときに、 [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md)が呼び出され、変更前の状態に関するすべてのデータが保存されます。 
    
2. テーブルのビューを保存された状態に復元するには、 **SetCollapseState**が呼び出されます。 **GetCollapseState**によって保存されたデータは、 **SetCollapseState**に渡されます。 **SetCollapseState**は、そのデータを使用して状態を復元できます。 
    
3. **SetCollapseState**は、 **GetCollapseState**への入力として渡されたインスタンスキーと同じ行を識別するブックマークを出力パラメーターとして返します。
    
カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

並べ替えの順序と制限が**GetCollapseState**呼び出し時とまったく同じであることを確認する責任があります。 変更が行われた場合、結果は予測できないため、 **SetCollapseState**を呼び出すことはできません。 これは、たとえば、クライアントが**GetCollapseState**を呼び出してから、 **SetCollapseState**を呼び出す前に並べ替えキーを変更するために、 **sorttable**を呼び出した場合に発生する可能性があります。 安全にするには、復元を続行する前に、保存したデータが有効であることを確認してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SetCollapseState**を呼び出すには、以前に**GetCollapseState**と呼ばれていなければなりません。 カテゴリを確立する並べ替え順序は、両方の方法で同じである必要があります。 並べ替え順序が異なる場合、 **SetCollapseState**操作の結果は予測できません。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

