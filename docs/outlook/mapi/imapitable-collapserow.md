---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328965"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
拡張されたテーブルカテゴリを折りたたみ、テーブルビューからそのカテゴリに属する下位レベルの見出しとリーフ行をすべて削除します。
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>パラメーター

 _cbInstanceKey_
  
> 順番_pbInstanceKey_パラメーターが指す PR_INSTANCE_KEY プロパティのバイト数。 
    
 _pbInstanceKey_
  
> 順番カテゴリの見出し行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティへのポインター。 
    
 _ulFlags_
  
> 予約語0である必要があります。
    
 _lアウト rowcount_
  
> 読み上げテーブルビューから削除されている行の合計数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 折りたたみ操作が成功しました。
    
MAPI_E_NOT_FOUND 
  
> _pbInstanceKey_パラメーターで指定された行が存在しません。 
    
MAPI_E_INVALID_ENTRYID 
  
> _pbInstanceKey_パラメーターで指定された行が存在しません。 このエラーは MAPI_E_NOT_FOUND の代わりになります。サービスプロバイダーはどちらかを返すことができます。 
    
## <a name="remarks"></a>解説

**IMAPITable:: CollapseRow**メソッドは、テーブルのカテゴリを折りたたんで、テーブルビューから削除します。 行は、 _pbInstanceKey_パラメーターによって示される**PR_INSTANCE_KEY**プロパティによって識別される行から折りたたまれます。 ビューから削除された行の数は、 _lルー rowcount_パラメーターの内容で返されます。 
  
折りたたみ操作の結果としてビューから削除されたテーブルの行に対して通知が生成されることはありません。 
  
ブックマークによって定義された行が非表示になっている場合、ブックマークは次の表示される行を指すように移動されます。 
  
カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl::D oexpandcollapse  <br/> |mfcmapi は、 **IMAPITable:: CollapseRow**メソッドを使用して、テーブルカテゴリを折りたたみます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

