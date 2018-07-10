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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800833"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**適用されます**: Outlook 
  
リーフ行がテーブルのビューからのカテゴリに属する、下位の見出しを削除する、拡張テーブルのカテゴリを折りたたみます。
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Parameters

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
    
## <a name="remarks"></a>備考

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
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
