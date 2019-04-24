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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349295"
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
  
> 順番渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lppRestriction_
  
> 読み上げ検索条件を定義する[srestriction](srestriction.md)構造体へのポインターへのポインター。 クライアントアプリケーションが_lppRestriction_パラメーターで NULL を渡した場合、 **getsearchcriteria**は**srestriction**構造を返しません。 
    
 _lppContainerList_
  
> 読み上げ検索に含めるコンテナーを表すエントリ識別子の配列へのポインターへのポインター。 クライアントが_lppContainerList_パラメーターで NULL を渡した場合、 **getsearchcriteria**はエントリ識別子の配列を返しません。 
    
 _lpulsearchstate_
  
> 読み上げ検索の現在の状態を示すために使用されるフラグのビットマスクへのポインター。 クライアントが_lpulsearchstate_パラメーターで NULL を渡すと、 **getsearchcriteria**はフラグを返しません。 次のフラグを設定できます。 
    
SEARCH_FOREGROUND 
  
> 検索は、他の検索と比較して高い優先度で実行する必要があります。 このフラグが設定されていない場合、検索は他の検索と比較して標準の優先度で実行されます。
    
SEARCH_REBUILD 
  
> 検索は、CPU を集中的に消費する操作で、条件に一致するメッセージを見つけようとしています。 このフラグが設定されていない場合は、検索の処理の CPU に負荷のかかる部分があります。 このフラグは、検索がアクティブである場合 (つまり、SEARCH_RUNNING フラグが設定されている場合) にのみ意味を持ちます。
    
SEARCH_RECURSIVE 
  
> 指定されたコンテナーと、そのすべての子コンテナーを検索して、一致するエントリを探します。 このフラグが設定されていない場合、 [IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドへの最後の呼び出しに明示的に含まれているコンテナーのみが検索されます。 
    
SEARCH_RUNNING 
  
> 検索がアクティブで、メッセージストアまたはアドレス帳の変更を反映するためにコンテナーの contents テーブルが更新されています。 このフラグが設定されていない場合、検索は非アクティブで、contents テーブルは静的です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索条件が正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_NOT_INITIALIZED 
  
> コンテナーに対して検索条件が設定されていません。
    
## <a name="remarks"></a>解説

**IMAPIContainer:: getsearchcriteria**メソッドは、通常、検索結果フォルダーである検索をサポートするコンテナーの検索条件を取得します。 検索条件を作成するには、コンテナーの**IMAPIContainer:: setsearchcriteria**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティに関連付けられている高度な検索機能を提供する場合にのみ、アドレス帳コンテナーで**getsearchcriteria**をサポートする必要があります。 アドレス帳コンテナーの高度な検索機能を実装する方法の詳細については、「[高度な](implementing-advanced-searching.md)検索の実装」を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppRestriction_パラメーターと_lppContainerList_パラメーターで示されるデータ構造が完成したら、各構造体を解放するために、 [MAPIFreeBuffer](mapifreebuffer.md)を1回呼び出します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|HierarchyTableDlg  <br/> |CHierarchyTableDlg:: oneditsearchcriteria  <br/> |mfcmapi は、 **IMAPIContainer:: getsearchcriteria**メソッドを使用して、フォルダーから表示する検索条件を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagSearch 標準プロパティ](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

