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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800462"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**適用対象**: Outlook 
  
コンテナーの検索基準を確立します。
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> [in]検索条件を定義する[SRestriction](srestriction.md)構造体へのポインター。 _LpRestriction_パラメーターに NULL を渡した場合、このコンテナーの最も最近使用した検索条件が再度使用されます。 NULL 渡すことはできません_lpRestriction_のコンテナー内の最初の検索をします。 
    
 _lpContainerList_
  
> [in]検索に含まれるコンテナーを表すエントリの識別子の配列へのポインター。 _LpContainerList_パラメーターに NULL を渡すと、クライアント、新しい検索のこのコンテナーを検索するのには最近使った項目識別子が使用されます。 クライアントは、コンテナー内の最初の検索の_lpContainerList_に NULL を渡さないでください。 
    
 _ulSearchFlags_
  
> [in]検索の実行方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
BACKGROUND_SEARCH 
  
> 検索は、他の検索基準にして通常の優先順位で実行する必要があります。 FOREGROUND_SEARCH フラグと同時には、このフラグを設定することはできません。
    
FOREGROUND_SEARCH 
  
> 検索は、他の検索基準とした優先度の高いで実行する必要があります。 BACKGROUND_SEARCH フラグと同時には、このフラグを設定することはできません。
    
NON_CONTENT_INDEXED_SEARCH
  
> 検索使用しないでくださいコンテンツのインデックス作成に一致するエントリを検索します。 このフラグで、Exchange ストアに対してのみです。
    
RECURSIVE_SEARCH 
  
> 検索では、 _lpContainerList_パラメーターとそのすべての子コンテナーで指定されたコンテナーを含める必要があります。 SHALLOW_SEARCH フラグと同時には、このフラグを設定することはできません。 
    
RESTART_SEARCH 
  
> 検索は、これは、 **SetSearchCriteria**、最初の呼び出しを開始または検索がアクティブでない場合に再起動する必要があります。 STOP_SEARCH フラグと同時には、このフラグを設定することはできません。
    
SHALLOW_SEARCH 
  
> 検索に一致するエントリの_lpContainerList_パラメーターで指定したコンテナーでのみです。 RECURSIVE_SEARCH フラグと同時には、このフラグを設定することはできません。 
    
STOP_SEARCH 
  
> 検索を停止する必要があります。 RESTART_SEARCH フラグと同時には、このフラグを設定することはできません。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 検索条件が正しく設定されました。
    
MAPI_E_TOO_COMPLEX 
  
> サービス プロバイダーは、指定された検索条件をサポートしていません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::SetSearchCriteria**メソッドは、通常の検索結果フォルダーの検索をサポートするコンテナーの検索基準を確立します。 検索結果フォルダーには、検索条件に一致するメッセージへのリンクが含まれています。実際のメッセージは、元の場所に保存されています。 検索結果のフォルダーに含まれているのみに固有のデータは、その内容のテーブルです。 検索結果フォルダーの内容のテーブルでは、検索の制限が適用された後にメッセージ ・ ストアがマージされた内容があります。 
  
検索操作は、この内容が結合されたテーブルでのみ動作します。他の検索結果のフォルダーを検索しません。 検索結果が検索条件に一致するメッセージのみを返すフォルダー階層は返されません。
  
検索が完了すると、制御がクライアントに返されます。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

アドレス帳コンテナーは、その内容のテーブルに制限を適用することで検索条件を確立します。 詳細については検索条件とアドレス帳コンテナー、[高度な検索を実装する](implementing-advanced-searching.md)を参照してください。
  
必要がありますオープンをサポートして、コピー、移動、および削除の各操作の検索結果のフォルダー内のメッセージに、検索結果フォルダー自体ではなく。 内に作成または検索結果のフォルダーにコピーするメッセージを許可しません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの受信者を検索するには、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定する[SSubRestriction](ssubrestriction.md)構造体の**ulSubObject**メンバーとサブオブジェクトの制限] をポイントする_lpRestriction_を設定します。 添付ファイルを検索するには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) に**ulSubObject**のメンバーを設定します。 受信者や添付ファイルの検索条件を記述するプロパティの制限] をポイントして、 **lpRes**のメンバーを設定します。 
  
たとえば、拡張子 .mss を含む添付ファイルを探すように**PR_MESSAGE_ATTACHMENTS**と**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)に一致するプロパティの制限を**lpRes**に**ulSubObject**を設定します。) を持つ。 mss。
  
_UlSearchFlags_パラメーターに FOREGROUND_SEARCH フラグを設定すると、システム パフォーマンスが低下可能性があります。 
  
既に進行中の検索の検索条件を変更するのには**SetSearchCriteria**を使用することができます。 新しい制限を検索するには、フォルダーと新しい検索の優先順位、優先度の高い検索にアップグレードするなどの新しいリストを指定できます。 検索の優先順位の変更を再起動して、既存の検索が発生しないが、条件を検索するには、その他の変更ができます。 
  
検索結果フォルダーを使用するが、フォルダーを削除するか、後で使用するために開いたままにできるようにします。 検索結果フォルダーを削除すると、メッセージのリンクのみが削除されます。 実際のメッセージは、その親フォルダーに残ります。 
  
検索結果フォルダーの詳細については、 [MAPI 検索フォルダー](mapi-search-folders.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI では、 **IMAPIContainer::SetSearchCriteria**メソッドを使用して、ユーザーがそれを編集した後、フォルダーの検索条件を記述します。  <br/> |
   
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

