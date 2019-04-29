---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427200"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの検索条件を確立します。
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> 順番検索条件を定義する[srestriction](srestriction.md)構造体へのポインター。 _lpRestriction_パラメーターで NULL が渡された場合、このコンテナーに対して最近使用された検索条件が再度使用されます。 コンテナー内の最初の検索では、 _lpRestriction_で NULL を渡すことはできません。 
    
 _lpContainerList_
  
> 順番検索に含めるコンテナーを表すエントリ識別子の配列へのポインター。 クライアントが_lpContainerList_パラメーターで NULL を渡した場合、最近このコンテナーを検索するために使用されたエントリ識別子が新しい検索に使用されます。 コンテナー内の最初の検索では、クライアントは_lpContainerList_で NULL を渡さないでください。 
    
 _ulsearchflags_
  
> 順番検索の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
BACKGROUND_SEARCH 
  
> 検索は、他の検索と比較して標準の優先度で実行する必要があります。 このフラグは、FOREGROUND_SEARCH フラグと同時には設定できません。
    
FOREGROUND_SEARCH 
  
> 検索は、他の検索と比較して高い優先度で実行する必要があります。 このフラグは、BACKGROUND_SEARCH フラグと同時には設定できません。
    
NON_CONTENT_INDEXED_SEARCH
  
> 検索では、一致するエントリを検索するために、コンテンツインデックスを使用しません。 このフラグは、Exchange ストアに対してのみ有効です。
    
RECURSIVE_SEARCH 
  
> 検索には、 _lpContainerList_パラメーターとそのすべての子コンテナーで指定されたコンテナーが含まれている必要があります。 このフラグは、SHALLOW_SEARCH フラグと同時には設定できません。 
    
RESTART_SEARCH 
  
> この検索は、 **setsearchcriteria**の最初の呼び出しである場合に開始するか、または検索が非アクティブな場合に再起動する必要があります。 このフラグは、STOP_SEARCH フラグと同時には設定できません。
    
SHALLOW_SEARCH 
  
> 検索は、一致するエントリに対して_lpContainerList_パラメーターで指定されたコンテナー内のみを参照する必要があります。 このフラグは、RECURSIVE_SEARCH フラグと同時には設定できません。 
    
STOP_SEARCH 
  
> 検索を停止する必要があります。 このフラグは、RESTART_SEARCH フラグと同時には設定できません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索条件が正常に設定されました。
    
MAPI_E_TOO_COMPLEX 
  
> サービスプロバイダーは、指定された検索条件をサポートしていません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer:: setsearchcriteria**メソッドは、検索をサポートするコンテナー (通常は検索結果フォルダー) の検索条件を設定します。 検索結果フォルダーには、検索条件に一致するメッセージへのリンクが含まれています。実際のメッセージは、元の場所に保存されたままになります。 検索結果フォルダーに格納されている一意のデータは、[コンテンツ] テーブルだけです。 検索結果フォルダーの contents テーブルには、検索制限が適用された後に、メッセージストアの内容がマージされています。 
  
検索操作は、この結合されたコンテンツテーブルでのみ動作します。他の検索結果フォルダーは検索されません。 検索結果には、検索条件に一致するメッセージのみが返されます。フォルダー階層は返されません。
  
検索が完了すると、コントロールはクライアントに返されます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

アドレス帳コンテナーは、コンテンツテーブルに制限を適用して検索条件を確立します。 検索条件とアドレス帳コンテナーの詳細については、「[高度な検索の実装](implementing-advanced-searching.md)」を参照してください。
  
検索結果フォルダー自体ではなく、検索結果フォルダー内のメッセージに対して、オープン、コピー、移動、および削除の操作をサポートする必要があります。 検索結果フォルダー内でのメッセージの作成またはコピーを許可しません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの受信者を検索するには、 [ssubrestriction](ssubrestriction.md)構造で**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定されている ulsubmember を持つサブ要素制限を指すように**** _lpRestriction_を設定します。 添付ファイルを検索するには**** 、ulsubobject メンバーを**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) に設定します。 受信者または添付ファイルの検索条件を記述するプロパティ制限をポイントするように、 **lpres**メンバーを設定します。 
  
たとえば、拡張子が mss の添付ファイルを検索するには、ulsubobject **** を**PR_MESSAGE_ATTACHMENTS**および**lpres**に設定して、 **PR_ATTACH_EXTENSION**に一致するプロパティ制限に設定します ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) を使用します。
  
_ulsearchflags_パラメーターに FOREGROUND_SEARCH フラグを設定すると、システムのパフォーマンスが低下する可能性があります。 
  
**setsearchcriteria**を使用して、既に進行中の検索条件を変更することができます。 新しい制限を指定したり、検索するフォルダーの新しいリストを指定したり、検索をより高い優先度にアップグレードするなどの新しい検索の優先度を指定したりできます。 検索優先度の変更によって既存の検索が再起動されることはありませんが、検索条件に対するその他の変更はできません。 
  
検索結果フォルダーを使用している場合は、フォルダーを削除するか、または後で使用するために開いたままにしておくことができます。 検索結果フォルダーを削除すると、メッセージリンクのみが削除されます。 実際のメッセージは親フォルダーに残ります。 
  
検索結果フォルダーの詳細については、「 [MAPI 検索フォルダー](mapi-search-folders.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|HierarchyTableDlg  <br/> |CHierarchyTableDlg:: oneditsearchcriteria  <br/> |mfcmapi は、 **IMAPIContainer:: setsearchcriteria**メソッドを使用して、ユーザーが編集した後のフォルダーの検索条件を書き込みます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

