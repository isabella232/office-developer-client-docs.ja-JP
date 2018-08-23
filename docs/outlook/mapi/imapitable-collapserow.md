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
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595301"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
リーフ行がテーブルのビューからのカテゴリに属する、下位の見出しを削除する、拡張テーブルのカテゴリを折りたたみます。
  
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
  
> [in]_PbInstanceKey_パラメーターが指す、PR_INSTANCE_KEY プロパティ内のバイト数です。 
    
 _pbInstanceKey_
  
> [in]カテゴリの見出しの行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインター。 
    
 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _lpulRowCount_
  
> [out]テーブル ビューから削除された行の総数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 折りたたみ操作が成功しました。
    
MAPI_E_NOT_FOUND 
  
> _PbInstanceKey_パラメーターで指定された行が存在しません。 
    
MAPI_E_INVALID_ENTRYID 
  
> _PbInstanceKey_パラメーターで指定された行が存在しません。 このエラーは、代わりに MAPI_E_NOT_FOUND です。サービス プロバイダーは、いずれかを返すことができます。 
    
## <a name="remarks"></a>注釈

**IMAPITable::CollapseRow**メソッドは、テーブルを解除し、表形式ビューから削除します。 _PbInstanceKey_パラメーターが指す、 **PR_INSTANCE_KEY**プロパティで識別される行で始まる行が折りたたまれます。 _LpulRowCount_パラメーターの内容をビューから削除された行の数が返されます。 
  
折りたたみ操作の結果として、ビューから削除されたテーブルの行の通知が生成されません。 
  
表示のブックマークで定義されている行が折りたたまれると、ブックマークが表示されている次の行を指すように移動します。 
  
分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI では、 **IMAPITable::CollapseRow**メソッドを使用して、テーブルのカテゴリを折りたたみます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

