---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ca03023d7edd81db214c080b8d4a744c1bf661cc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620829"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
折りたたみテーブル カテゴリを展開し、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブル ビューに追加します。
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>パラメーター

 _cbInstanceKey_
  
> [in]  _pbInstanceKey_ パラメーターがPR_INSTANCE_KEYするプロパティのバイト数。 
    
 _pbInstanceKey_
  
> [in]カテゴリの見出 **しPR_INSTANCE_KEY** を識別するプロパティ [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)へのポインター。 
    
 _ulRowCount_
  
> [in]  _lppRows_ パラメーターで返される行の最大数。 
    
 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _lppRows_
  
> [out]拡張の結果としてテーブル ビューに挿入された最初の _(ulRowCount_ まで) 行を受け取る [SRowSet](srowset.md)構造体へのポインター。 これらの行は  _、pbInstanceKey_ パラメーターで識別される見出し行の後に挿入されます。 _ulRowCount パラメーターが_ 0 の場合 _、lppRows_ パラメーターは NULL になります。 
    
 _lpulMoreRows_
  
> [out]テーブル ビューに追加された行の総数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> カテゴリが正常に展開されました。
    
MAPI_E_NOT_FOUND 
  
> _pbInstanceKey_ パラメーターで識別される行が存在しません。 
    
## <a name="remarks"></a>注釈

**IMAPITable::ExpandRow** メソッドは、折りたたみテーブル カテゴリを展開し、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブル ビューに追加します。 _lppRows_ パラメーターで返される行数の制限は _、ulRowCount パラメーターで指定_ できます。 _ulRowCount_ が 0 より大きい値に設定され _、lppRows_ が指す行セットで 1 つ以上の行が返される場合、ブックマーク BOOKMARK_CURRENT の位置は、行セットの最後の行の直後の行に移動されます。
  
_ulRowCount_ を 0 に設定し、カテゴリにリーフまたは下位レベルの見出し行を追加するか、またはカテゴリにリーフまたは下位レベルの見出し行がないのでゼロ行が返される場合、BOOKMARK_CURRENT の位置は _pbInstanceKey_ で識別される行の後の行に設定されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

カテゴリの展開によりテーブル ビューに追加される行に対して通知を生成しない。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppRows_ パラメーターが指す行セット内の行数は、テーブルに実際に追加された行の数、カテゴリのリーフまたは下位レベルの見出し行のセット全体と等しくない場合があります。 メモリ不足や、ulRowCount パラメーターで指定された数を超えるカテゴリの行数など、エラー  _が発生する可能性_ があります。 どちらの場合も、BOOKMARK_CURRENT最後の行に配置されます。 カテゴリ内の残りの行をすぐに取得するには [、IMAPITable::QueryRows を呼び出します](imapitable-queryrows.md)。
  
カテゴリの状態が変更された場合は、テーブル通知を受け取る必要があります。 すべての ExpandRow 呼び出しまたは **CollapseRow** 呼び出しで更新できる行のローカル キャッシュ **を維持** できます。 
  
分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI は **IMAPITable::ExpandRow** メソッドを使用して、折りたたみテーブル カテゴリを展開します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

