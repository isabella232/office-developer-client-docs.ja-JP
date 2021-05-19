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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416175"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
展開されたテーブル カテゴリを折りたたみ、そのカテゴリに属する下位レベルの見出しとリーフ行をテーブル ビューから削除します。
  
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
  
> [in]  _pbInstanceKey_ パラメーターがPR_INSTANCE_KEYするプロパティのバイト数。 
    
 _pbInstanceKey_
  
> [in]カテゴリの見出 **しPR_INSTANCE_KEY** を識別するプロパティ [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)へのポインター。 
    
 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _lpulRowCount_
  
> [out]テーブル ビューから削除される行の総数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 折りたたみ操作が成功しました。
    
MAPI_E_NOT_FOUND 
  
> _pbInstanceKey_ パラメーターで識別される行が存在しません。 
    
MAPI_E_INVALID_ENTRYID 
  
> _pbInstanceKey_ パラメーターで識別される行が存在しません。 このエラーは、このエラーの代わりにMAPI_E_NOT_FOUND。サービス プロバイダーは、どちらか 1 つを返す場合があります。 
    
## <a name="remarks"></a>注釈

**IMAPITable::CollapseRow** メソッドは、テーブル カテゴリを折りたたみ、テーブル ビューから削除します。 行は _、pbInstanceKey_ パラメーターが指す **PR_INSTANCE_KEYプロパティで** 識別される行から折りたたまれます。 ビューから削除された行の数は  _、lpulRowCount_ パラメーターの内容で返されます。 
  
折りたたみ操作の結果としてビューから削除されたテーブル行に対する通知は生成されません。 
  
ブックマークによって定義された行が表示されない状態で折りたたむ場合、ブックマークは次に表示される行を指す位置に移動されます。 
  
分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI では **、IMAPITable::CollapseRow** メソッドを使用してテーブル カテゴリを折りたたむ。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

