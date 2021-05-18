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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412024"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの検索条件を取得します。
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lppRestriction_
  
> [out]検索条件を定義する [SRestriction](srestriction.md) 構造体へのポインター。 クライアント アプリケーションが  _lppRestriction_ パラメーターで NULL を渡した場合 **、GetSearchCriteria** は **SRestriction 構造を返す必要** があります。 
    
 _lppContainerList_
  
> [out]検索に含めるコンテナーを表すエントリ識別子の配列へのポインター。 クライアントが  _lppContainerList_ パラメーターで NULL を渡した場合 **、GetSearchCriteria** はエントリ識別子の配列を返します。 
    
 _lpulSearchState_
  
> [out]検索の現在の状態を示すために使用されるフラグのビットマスクへのポインター。 クライアントが  _lpulSearchState_ パラメーターで NULL を渡した場合 **、GetSearchCriteria は** フラグを返します。 次のフラグを設定できます。 
    
SEARCH_FOREGROUND 
  
> 検索は、他の検索と相対的に高い優先度で実行する必要があります。 このフラグが設定されていない場合、検索は他の検索に対して通常の優先度で実行されます。
    
SEARCH_REBUILD 
  
> 検索は CPU 負荷の高い操作モードで、条件に一致するメッセージを検索します。 このフラグが設定されていない場合、検索の操作の CPU 負荷の高い部分は終了します。 このフラグは、検索がアクティブである場合にのみ意味を持ちます (つまり、SEARCH_RUNNINGフラグが設定されている場合)。
    
SEARCH_RECURSIVE 
  
> 検索では、指定したコンテナーとそのすべての子コンテナーで、一致するエントリが検索されます。 このフラグが設定されていない場合 [、IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) メソッドの最後の呼び出しに明示的に含まれるコンテナーだけが検索されます。 
    
SEARCH_RUNNING 
  
> 検索がアクティブで、コンテナーのコンテンツ テーブルが更新され、メッセージ ストアまたはアドレス帳の変更が反映されます。 このフラグが設定されていない場合、検索は非アクティブであり、コンテンツ テーブルは静的です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索条件が正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_NOT_INITIALIZED 
  
> コンテナーに対して検索条件が確立されていませんでした。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::GetSearchCriteria** メソッドは、検索をサポートするコンテナー (通常は検索結果フォルダー) の検索条件を取得します。 検索条件を作成するには、コンテナーの **IMAPIContainer::SetSearchCriteria メソッドを呼び出** します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

アドレス帳コンテナーは **、GetSearchCriteria** プロパティ [(PidTagSearch)](pidtagsearch-canonical-property.md)プロパティに関連付けられている高度な検索機能を提供する場合にのみ **、PR_SEARCH** GetSearchCriteria をサポートする必要があります。 アドレス帳コンテナーの高度な検索機能を実装する方法の詳細については [、「Implementing Advanced Searching」を参照してください](implementing-advanced-searching.md)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppRestriction_ パラメーターと _lppContainerList_ パラメーターが示すデータ構造が終了したら、リリースする構造体ごとに [MAPIFreeBuffer](mapifreebuffer.md)を 1 回呼び出します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI は **IMAPIContainer::GetSearchCriteria** メソッドを使用して、表示するフォルダーから検索条件を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagSearch 標準プロパティ](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

