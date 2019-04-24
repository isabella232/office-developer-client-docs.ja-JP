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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328928"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カテゴリ化されたテーブルの現在の折りたたまれた状態または展開された状態を再構築するために必要なデータを返します。
  
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
  
> 予約語0である必要があります。
    
 _cbInstanceKey_
  
> 順番_lpbInstanceKey_パラメーターによって示されるインスタンスキーのバイト数。 
    
 _lpbInstanceKey_
  
> 順番現在折りたたまれている状態または展開されている状態を再構築する必要がある行の**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティへのポインター。 _lpbInstanceKey_パラメーターを NULL にすることはできません。 
    
 _lpcbCollapseState_
  
> 読み上げ_lppbCollapseState_パラメーターによって参照されている構造体の数へのポインター。 
    
 _lppbCollapseState_
  
> 読み上げ現在のテーブルビューを説明するデータを含む構造体へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> カテゴリ内のテーブルの状態が正常に保存されました。
    
MAPI_E_BUSY 
  
> 操作が開始されないように、別の操作が進行中です。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> このテーブルでは、分類と展開されたビューおよび折りたたまれたビューをサポートしていません。
    
## <a name="remarks"></a>解説

**imapitable:: GetCollapseState**メソッドは[imapitable:: SetCollapseState](imapitable-setcollapsestate.md)メソッドを使用して、分類されたテーブルのユーザーのビューを変更します。 **GetCollapseState**は、 **SetCollapseState**が、カテゴリに分類されたテーブルのカテゴリの適切なビューを再構築するために使用するために必要なデータを保存します。 サービスプロバイダーは、保存するデータを決定します。 ただし、 **GetCollapseState**を実装するほとんどのサービスプロバイダーでは、次の内容が保存されます。 
  
- 並べ替えキー (標準列とカテゴリ列)。
    
- インスタンスキーが表す行に関する情報。
    
- 表の折りたたまれたカテゴリと展開されたカテゴリを復元するための情報。
    
カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lppbCollapseState_パラメーターに、テーブルのすべてのノードの現在の状態を格納します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SetCollapseState**を呼び出す前に、必ず**GetCollapseState**を呼び出してください。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

