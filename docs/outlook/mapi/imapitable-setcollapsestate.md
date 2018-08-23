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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 252b6d6c7ff74acd5f0b288af48ff2901c2330ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800864"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**適用対象**: Outlook 
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)メソッドへの前回の呼び出しによって保存されたデータを使用して分類されたテーブルの現在の展開または折りたたみの状態を再構築します。 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _cbCollapseState_
  
> [in]_PbCollapseState_パラメーターが指す構造体のバイト数をカウントします。 
    
 _pbCollapseState_
  
> [in]テーブル ビューを再構築するために必要なデータを含む構造体へのポインター。
    
 _lpbkLocation_
  
> [out]折りたたまれた状態または展開された状態の再構築するテーブル内の行を識別するブックマークへのポインター。 このブックマークと[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)への呼び出し内の_lpbInstanceKey_パラメーターで渡されるインスタンスのキーは、同じ行を識別します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 分類されたテーブルの状態が正常に再構築されました。
    
MAPI_E_BUSY 
  
> 別の操作は、操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> テーブルでは、折りたたまれた状態または展開されたビューの再構築が完了できませんでした。
    
## <a name="remarks"></a>注釈

**IMAPITable::SetCollapseState**メソッドは、テーブル ビューの展開または折りたたみの状態を再確立します。 **SetCollapseState**および**GetCollapseState**が次のように協力しています。 
  
1. 分類されたテーブルの状態を変更しようとしていますが、すべての変更前の状態に関連するデータを保存するのには[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)が呼び出されます。 
    
2. テーブルのビューを保存した状態に復元するに**SetCollapseState**が呼び出されます。 **GetCollapseState**によって保存されたデータは、 **SetCollapseState**に渡されます。 **SetCollapseState**は、状態を復元するのにはそのデータを使用することです。 
    
3. **SetCollapseState**は、出力パラメーターとして**GetCollapseState**への入力として渡されるインスタンスのキーとして同じ行を識別するブックマークを返します。
    
分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

並べ替え順序および制限、正確に同じである**GetCollapseState**の呼び出しの時と同様に確認する責任があります。 変更を行った結果を予測できるので**SetCollapseState**は呼び出されません。 **GetCollapseState**とし、 **SortTable** **SetCollapseState**を呼び出す前に、並べ替えのキーを変更するのなど、クライアントが呼び出す場合は、これが起こります。 安全のため、保存されたデータは復元を続行する前に有効なことを確認してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SetCollapseState**を呼び出すには、する必要がありますが以前と呼ばれる**GetCollapseState**。 カテゴリを確立する並べ替え順序は、どちらのメソッドも同じにする必要があります。 並べ替え順が異なる場合、 **SetCollapseState**操作の結果は予測できません。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

