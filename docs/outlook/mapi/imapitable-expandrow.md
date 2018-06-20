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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800823"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**適用されます**: Outlook 
  
リーフまたは表形式ビューをカテゴリに属している下位レベルの見出しの行を追加する、折りたたまれているテーブルのカテゴリを展開します。
  
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

## <a name="parameters"></a>Parameters

 _cbInstanceKey_
  
> [in]_PbInstanceKey_パラメーターが指す、PR_INSTANCE_KEY プロパティ内のバイト数です。 
    
 _pbInstanceKey_
  
> [in]カテゴリの見出しの行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインター。 
    
 _ulRowCount_
  
> [in]_LppRows_パラメーターに返す行の最大数です。 
    
 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _lppRows_
  
> [out]拡張の結果としてテーブルのビューに挿入されている ( _ulRowCount_) までの最初のローを受信する[SRowSet](srowset.md)構造体へのポインター。 _PbInstanceKey_パラメーターで指定された見出しの行の後は、これらの行が挿入されます。 _LppRows_パラメーターは、 _ulRowCount_パラメーターが 0 の場合、NULL にすることができます。 
    
 _lpulMoreRows_
  
> [out]テーブル ビューに追加された行の総数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> カテゴリは正常に展開されています。
    
MAPI_E_NOT_FOUND 
  
> _PbInstanceKey_パラメーターで指定された行が存在しません。 
    
## <a name="remarks"></a>備考

**IMAPITable::ExpandRow**メソッドでは、リーフやテーブル ・ ビューをカテゴリに属している下位レベルの見出しの行を追加する、折りたたまれているテーブルのカテゴリを展開します。 _LppRows_パラメーターで返される行の数に制限は、 _ulRowCount_パラメーターで指定できます。 _UlRowCount_が 0 より大きい値に設定すると、 _lppRows_で指定された行セットの 1 つまたは複数の行が返されます、BOOKMARK_CURRENT は、行の最後の行の直後の行に移動するブックマークの位置を設定します。
  
行に BOOKMARK_CURRENT の位置を設定するカテゴリに追加する_ulRowCount_を 0 に設定すると、リーフは 0、または下位の見出し行を要求するか、リーフまたはカテゴリ内の下位レベルの見出しの行がないために、0 個の行が返されます、次の_pbInstanceKey_で識別される行です。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

カテゴリの拡張のためのテーブル ビューに追加される行に通知を生成しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LppRows_パラメーターで指定された行セット内の行の数ではテーブルに実際に追加された行の数が等しくない場合がありますが、全体のリーフの設定または下位の見出し行のカテゴリ。 メモリ不足、または_ulRowCount_パラメーターで指定された数を超えるカテゴリ内の行の数などは、エラーが発生することができます。 BOOKMARK_CURRENT は、いずれの場合も、返された最後の行に配置されます。 カテゴリ内の行の残りの部分をすぐに取得するには、 [IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。
  
カテゴリの状態を変更するとテーブルの通知が受信されないようにします。 **ExpandRow**または**CollapseRow**呼び出しのたびに更新される行のローカル キャッシュを保持することができます。 
  
分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI では、 **IMAPITable::ExpandRow**メソッドを使用して、折りたたまれているテーブルのカテゴリを展開します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

