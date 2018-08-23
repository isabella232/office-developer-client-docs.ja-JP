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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589666"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在を再構築するために必要なデータを返しますは、折りたたむか、カテゴリ別のテーブルの状態を展開します。
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _cbInstanceKey_
  
> [in]_LpbInstanceKey_パラメーターが指すインスタンスのキーのバイト数です。 
    
 _lpbInstanceKey_
  
> [in]現在の折りたたみまたは展開された状態の行の**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインターを再構築する必要があります。 _LpbInstanceKey_パラメーターは、NULL にすることはできません。 
    
 _lpcbCollapseState_
  
> [out]_LppbCollapseState_パラメーターが指す構造体の数へのポインターです。 
    
 _lppbCollapseState_
  
> [out]現在のテーブル ビューを記述するデータを含む構造体へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 分類されたテーブルの状態が正常に保存されました。
    
MAPI_E_BUSY 
  
> 別の操作は、操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは、分類し、展開と縮小のビューをサポートしていません。
    
## <a name="remarks"></a>注釈

**IMAPITable::GetCollapseState**メソッドは、ユーザーの分類されたテーブルのビューを変更するのには[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)メソッドを使用して動作します。 **GetCollapseState**は、 **SetCollapseState**を使用して適切なカテゴリに分類されたテーブルのビューを再構築するのに必要なデータを保存します。 サービス プロバイダーは、保存するデータを決定します。 ただし、 **GetCollapseState**を実装するほとんどのサービス プロバイダーは、次を保存します。 
  
- (標準の列と列のカテゴリ) の並べ替えのキーです。
    
- インスタンス キーを表す行に関する情報です。
    
- テーブルの折りたたみと展開されているカテゴリを復元する情報です。
    
分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

_LppbCollapseState_パラメーターでは、テーブルのすべてのノードの現在の状態を格納します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

常に**SetCollapseState**を呼び出す前に**GetCollapseState**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

