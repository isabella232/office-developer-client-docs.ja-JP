---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 13c151a134e4334e8ed2e75e031a6fc9dddbf941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800452"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**適用されます**: Outlook 
  
コンテナーの検索条件を取得します。
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]渡された文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lppRestriction_
  
> [out]検索条件を定義する[SRestriction](srestriction.md)構造体へのポインターへのポインター。 クライアント アプリケーションは、 _lppRestriction_パラメーターに NULL を渡す、 **GetSearchCriteria**は**SRestriction**構造体を返しません。 
    
 _lppContainerList_
  
> [out]検索に含まれるコンテナーを表すエントリの識別子の配列へのポインターへのポインター。 クライアントは、 _lppContainerList_パラメーターに NULL を渡す、 **GetSearchCriteria**はエントリの識別子の配列を返しません。 
    
 _lpulSearchState_
  
> [out]検索の現在の状態を示すために使用されるフラグのビットマスクへのポインター。 場合は、クライアントでは、 _lpulSearchState_パラメーターに NULL を渡す、 **GetSearchCriteria**フラグを返しますありません。 次のフラグを設定することができます。 
    
SEARCH_FOREGROUND 
  
> 検索は、他の検索基準とした優先度の高いで実行する必要があります。 このフラグが設定されていない場合は、他の検索基準にして通常の優先順位で検索が実行されます。
    
SEARCH_REBUILD 
  
> 検索では、CPU を消費するのモードでの操作は、条件に一致するメッセージを検索しようとしています。 このフラグが設定されていない場合、CPU を消費するで検索の操作は上です。 このフラグは、意味、検索がアクティブな場合にのみ (つまり、SEARCH_RUNNING フラグが設定されます) 場合。
    
SEARCH_RECURSIVE 
  
> 検索は、指定されたコンテナーとそのすべての子コンテナーのエントリに一致する予定です。 このフラグが設定されていない場合、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドの最後の呼び出しで明示的に含まれているコンテナーだけを検索対象がします。 
    
SEARCH_RUNNING 
  
> 検索はアクティブで、メッセージ ・ ストア内の変更を反映または、アドレス帳コンテナーの内容のテーブルが更新されています。 このフラグが設定されていない場合、検索はアクティブではなく、内容のテーブルでは、静的です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 検索条件が正常に取得しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_NOT_INITIALIZED 
  
> コンテナーには、検索条件は確立されたことはありません。
    
## <a name="remarks"></a>備考

**IMAPIContainer::GetSearchCriteria**メソッドは、通常の検索結果フォルダーの検索をサポートするコンテナーの検索条件を取得します。 検索条件を作成するには、コンテナーの**IMAPIContainer::SetSearchCriteria**メソッドを呼び出すとします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

アドレス帳コンテナーは、 **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) のプロパティに関連付けられている高度な検索機能を提供する場合にのみ、 **GetSearchCriteria**をサポートする必要があります。 アドレス帳コンテナーの高度な検索機能を実装する方法の詳細については、[高度な検索を実装する](implementing-advanced-searching.md)を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

完了したら、 _lppRestriction_および_lppContainerList_パラメーターが指すデータ構造体を持つ、 [MAPIFreeBuffer](mapifreebuffer.md) 1 回の各構造体を解放するを呼び出します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI では、 **IMAPIContainer::GetSearchCriteria**メソッドを使用して表示するためのフォルダーから検索条件を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagSearch の標準的なプロパティ](pidtagsearch-canonical-property.md)
  
[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

