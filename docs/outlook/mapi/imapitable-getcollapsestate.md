---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436077"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
分類されたテーブルの現在の折りたたみ状態または展開状態を再構築するために必要なデータを返します。
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _cbInstanceKey_
  
> [in]  _lpbInstanceKey_ パラメーターが指すインスタンス キー内のバイト数。 
    
 _lpbInstanceKey_
  
> [in]現在の折 **りたたPR_INSTANCE_KEY** または展開された状態を再構築する必要がある行の PR_INSTANCE_KEY ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティへのポインター。 _lpbInstanceKey パラメーター_ を NULL にすることはできません。 
    
 _lpcbCollapseState_
  
> [out]  _lppbCollapseState_ パラメーターが指す構造体の数へのポインター。 
    
 _lppbCollapseState_
  
> [out]現在のテーブル ビューを表すデータを含む構造体へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 分類されたテーブルの状態が正常に保存されました。
    
MAPI_E_BUSY 
  
> 操作の開始を妨げる別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> このテーブルでは、分類ビューと展開ビューと折りたたみビューはサポートされていません。
    
## <a name="remarks"></a>注釈

**IMAPITable::GetCollapseState** メソッドは [、IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)メソッドを使用して、分類されたテーブルのユーザーのビューを変更します。 **GetCollapseState** は、分類されたテーブルのカテゴリの適切なビューを再構築するために使用する **SetCollapseState** に必要なデータを保存します。 サービス プロバイダーは、保存するデータを決定します。 ただし **、GetCollapseState** を実装しているほとんどのサービス プロバイダーは、次の情報を保存します。 
  
- 並べ替えキー (標準の列とカテゴリ列)。
    
- インスタンス キーが表す行に関する情報。
    
- テーブルの折りたたみおよび展開されたカテゴリを復元する情報。
    
分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

テーブルのすべてのノードの現在の状態を  _lppbCollapseState パラメーターに格納_ します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SetCollapseState を呼び出す前に必** ず **GetCollapseState を呼び出してください**。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

