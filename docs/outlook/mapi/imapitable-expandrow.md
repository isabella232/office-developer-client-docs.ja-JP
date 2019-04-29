---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415167"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
折りたたまれたテーブルカテゴリを展開して、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブルビューに追加します。
  
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
  
> 順番_pbInstanceKey_パラメーターが指す PR_INSTANCE_KEY プロパティのバイト数。 
    
 _pbInstanceKey_
  
> 順番カテゴリの見出し行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティへのポインター。 
    
 _ulrowcount_
  
> 順番_lpprows_パラメーターで取得する行の最大数。 
    
 _ulFlags_
  
> 予約語0である必要があります。
    
 _lpprows_
  
> 読み上げ拡張の結果としてテーブルビューに挿入された最初の (最大_ulrowcount_) 行を受信する[srowset](srowset.md)構造体へのポインター。 これらの行は、 _pbInstanceKey_パラメーターによって指定される見出し行の後に挿入されます。 _ulrowcount_パラメーターが0の場合は、 _lpprows_パラメーターを NULL にすることができます。 
    
 _lpulMoreRows_
  
> 読み上げテーブルビューに追加された行の合計数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> カテゴリが正常に展開されました。
    
MAPI_E_NOT_FOUND 
  
> _pbInstanceKey_パラメーターで指定された行が存在しません。 
    
## <a name="remarks"></a>注釈

**IMAPITable:: expandrow**メソッドは、折りたたまれたテーブルカテゴリを展開し、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブルビューに追加します。 _lpprows_パラメーターで返される行数の制限は、 _ulrowcount_パラメーターで指定できます。 _ulrowcount_が0より大きい値に設定されている場合に、 _lpprows_が指す行セットで1つ以上の行が返されると、bookmark BOOKMARK_CURRENT の位置は、行セットの最後の行の直後の行に移動します。
  
_ulrowcount_が0に設定されている場合、0個のリーフまたは下位レベルの見出し行をカテゴリに追加することを要求するか、カテゴリにリーフまたは下位レベルの見出し行がないために0行が返される場合、BOOKMARK_CURRENT の位置は行に設定されます。_pbInstanceKey_によって識別される行の次のとおりです。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

カテゴリの拡張によってテーブルビューに追加された行に対して通知を生成しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpprows_パラメーターによって指定された行セット内の行数が、そのカテゴリのリーフまたは下位レベルの見出し行のセット全体で、実際にテーブルに追加された行数と一致しない場合があります。 メモリが不足しているなどのエラー、または_ulrowcount_パラメーターで指定された数を超えるカテゴリ内の行の数が発生することがあります。 どちらの場合でも、BOOKMARK_CURRENT は返された最後の行に配置されます。 カテゴリ内の残りの行をすぐに取得するには、「 [IMAPITable:: QueryRows](imapitable-queryrows.md)」という呼び出しを行います。
  
カテゴリの状態が変更されたときに、テーブル通知を受け取ることはありません。 すべての**expandrow**または**CollapseRow**呼び出しで更新できる行のローカルキャッシュを維持できます。 
  
カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl::D oexpandcollapse  <br/> |mfcmapi は、 **IMAPITable:: expandrow**メソッドを使用して、折りたたまれたテーブルカテゴリを展開します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

