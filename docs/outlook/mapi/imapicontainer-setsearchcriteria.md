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
  
コンテナーの検索条件を設定します。
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> [in]検索条件を [定義する SRestriction](srestriction.md) 構造体へのポインター。 _lpRestriction_ パラメーターで NULL が渡された場合、このコンテナーで最近使用された検索条件が再び使用されます。 コンテナー内の最初の検索  _では、lpRestriction_ で NULL を渡す必要があります。 
    
 _lpContainerList_
  
> [in]検索に含めるコンテナーを表すエントリ識別子の配列へのポインター。 クライアントが  _lpContainerList_ パラメーターで NULL を渡した場合、このコンテナーの検索に最近使用されたエントリ識別子が新しい検索に使用されます。 クライアントは、コンテナー内の最初の検索に  _lpContainerList_ で NULL を渡す必要があります。 
    
 _ulSearchFlags_
  
> [in]検索の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
BACKGROUND_SEARCH 
  
> 検索は、他の検索に対する通常の優先度で実行する必要があります。 このフラグは、このフラグと同時に設定FOREGROUND_SEARCHできません。
    
FOREGROUND_SEARCH 
  
> 検索は、他の検索と相対的に高い優先度で実行する必要があります。 このフラグは、このフラグと同時に設定BACKGROUND_SEARCHできません。
    
NON_CONTENT_INDEXED_SEARCH
  
> 一致するエントリを検索する場合は、コンテンツ インデックスを使用しない必要があります。 このフラグは、一部のストアExchangeです。
    
RECURSIVE_SEARCH 
  
> 検索には  _、lpContainerList_ パラメーターで指定されたコンテナーとそのすべての子コンテナーが含まれる必要があります。 このフラグは、このフラグと同時に設定SHALLOW_SEARCHできません。 
    
RESTART_SEARCH 
  
> **これが SetSearchCriteria** への最初の呼び出しである場合は検索を開始するか、検索が非アクティブな場合は再起動する必要があります。 このフラグは、このフラグと同時に設定STOP_SEARCHできません。
    
SHALLOW_SEARCH 
  
> 検索は、一致するエントリの  _lpContainerList_ パラメーターで指定されたコンテナーでのみ検索する必要があります。 このフラグは、このフラグと同時に設定RECURSIVE_SEARCHできません。 
    
STOP_SEARCH 
  
> 検索を停止する必要があります。 このフラグは、このフラグと同時に設定RESTART_SEARCHできません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索条件が正常に設定されました。
    
MAPI_E_TOO_COMPLEX 
  
> サービス プロバイダーは、指定された検索条件をサポートしていない。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::SetSearchCriteria** メソッドは、検索をサポートするコンテナー (通常は検索結果フォルダー) の検索条件を確立します。 検索結果フォルダーには、検索条件を満たすメッセージへのリンクが含まれます。実際のメッセージは、元の場所に保存されます。 検索結果フォルダーに含まれる唯一の一意のデータは、そのコンテンツ テーブルです。 検索結果フォルダーのコンテンツ テーブルには、検索制限が適用された後に、メッセージ ストアの結合されたコンテンツがあります。 
  
検索操作は、この結合されたコンテンツ テーブルでのみ機能します。他の検索結果フォルダーを検索しない。 検索結果は、検索条件に一致するメッセージのみを返します。フォルダー階層は返されません。
  
検索が完了すると、コントロールがクライアントに返されます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

アドレス帳コンテナーは、コンテンツ テーブルに制限を適用して検索条件を確立します。 検索条件とアドレス帳コンテナーの詳細については、「高度な検索の実装 [」を参照してください](implementing-advanced-searching.md)。
  
検索結果フォルダー自体ではなく、検索結果フォルダー内のメッセージに対する開く、コピー、移動、削除の操作をサポートする必要があります。 メッセージを検索結果フォルダー内に作成したり、検索結果フォルダーにコピーしたりすることはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ受信者を検索するには _、sSubRestriction_ 構造体の **ulSubObject** メンバーが PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)に設定されたサブオブジェクト制限をポイントする [lpRestriction](ssubrestriction.md)を設定します。  添付ファイルを検索するには **、ulSubObject** **メンバー** を PR_MESSAGE_ATTACHMENTS ([PidTagMessageAttachments) に設定します](pidtagmessageattachments-canonical-property.md)。 **lpRes メンバーに**、受信者または添付ファイルの検索条件を示すプロパティ制限を指定します。 
  
たとえば、拡張子が .mss の添付ファイルを検索するには **、ulSubObject** を **PR_MESSAGE_ATTACHMENTS** に **、lpRes** を **、.mss** の PR_ATTACH_EXTENSION ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) と一致するプロパティ制限に設定します。
  
_ulSearchFlags_ パラメーター FOREGROUND_SEARCHフラグを設定すると、システムのパフォーマンスが低下する可能性があります。 
  
**SetSearchCriteria を使用して**、既に進行中の検索の検索条件を変更できます。 新しい制限、検索するフォルダーの新しいリスト、および検索の優先度を高くするなどの新しい検索優先度を指定できます。 検索優先度の変更によって既存の検索が再開されるのではなく、検索条件に対するその他の変更が可能です。 
  
検索結果フォルダーを使用している場合は、フォルダーを削除するか、後で使用するために開いたままにできます。 検索結果フォルダーを削除すると、メッセージ リンクだけが削除されます。 実際のメッセージは親フォルダーに残ります。 
  
検索結果フォルダーの詳細については、「MAPI 検索フォルダー [」を参照してください](mapi-search-folders.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI は **IMAPIContainer::SetSearchCriteria** メソッドを使用して、ユーザーがフォルダーを編集した後にフォルダーの検索条件を書き込みます。  <br/> |
   
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

