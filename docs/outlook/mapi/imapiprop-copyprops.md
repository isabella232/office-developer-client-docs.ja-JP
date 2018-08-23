---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ee6fcaf2fa168f6be91b798efa249799f738bfa0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571081"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
選択したプロパティのコピーまたは移動します。 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _lpIncludeProps_
  
> [in]コピーまたは移動するにはプロパティを指定するプロパティ タグ配列へのポインター。 **PR_NULL**([PidTagNull](pidtagnull-canonical-property.md)) は、配列に含めることができません。 _LpIncludeProps_パラメーターを**null**にすることはできません。
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpProgress_
  
> [in]進行状況のインジケーターの実装へのポインター。 **Null**が渡された場合、 _lpProgress_パラメーターで、MAPI 実装を使用して進行状況のインジケーターが表示されます。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。 
    
 _lpInterface_
  
> [in]_LpDestObj_パラメーターが指すオブジェクトにアクセスするために使用する必要がありますインターフェイスを表すインターフェイス識別子 (IID) へのポインターです。 _LpInterface_パラメーターを**null**にするにはできません。
    
 _lpDestObj_
  
> [in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DECLINE_OK 
  
> **CopyProps**は、処理、コピーまたは移動の操作をするには、 [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)メソッドを呼び出して場合、代わりにすぐに MAPI_E_DECLINE_COPY のエラー値を返す必要があります。 MAPI_DECLINE_OK フラグは、再帰を制限するのには MAPI によって設定されています。 クライアントでは、このフラグは設定されません。 
    
MAPI_DIALOG 
  
> 進行状況のインジケーターが表示されます。
    
MAPI_MOVE 
  
> **CopyProps**は、コピー操作ではなく移動操作を実行する必要があります。 このフラグが設定されていない場合、 **CopyProps**は、コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> コピー先オブジェクトの既存のプロパティを上書きしてはなりません。 このフラグが設定されていない場合、 **CopyProps**には、既存のプロパティが上書きされます。 
    
 _lppProblems_
  
> [で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、 **null**、エラー情報の必要性がないことを示します。 _LppProblems_が入力時に有効なポインターである場合は、 **CopyProps**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティは、正常にコピーまたは移動されています。
    
MAPI_E_COLLISION 
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで定義されている、同じ表示名のサブオブジェクトは、目的のオブジェクトに既に存在するため、サブオブジェクトをコピーできません。 
    
MAPI_E_DECLINE_COPY 
  
> サービス プロバイダーは、コピー操作を実装していません。
    
MAPI_E_FOLDER_CYCLE 
  
> ソース オブジェクトが直接的または間接的にコピーまたは移動操作を実行するには、目的のオブジェクトが含まれています。 重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> 先のオブジェクトでは、 _lpInterface_パラメーターで指定されたインターフェイスはサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。 目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。
    
次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**CopyProps**。 これらのエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された**CopyProps**は、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**CopyProps**は、Unicode だけをサポートしています。 
    
MAPI_E_COMPUTED 
  
> コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。 このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの型が正しくありません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元の型ではありません。
    
## <a name="remarks"></a>注釈

**IMAPIProp::CopyProps**メソッドは、コピーまたは、選択したプロパティを現在のオブジェクトからコピー先のオブジェクトに移動します。 **CopyProps**は、返信または転送するメッセージ、返信を移動またはコピーを転送元のメッセージからのプロパティの一部のみ、主に使用されます。 
  
ソース オブジェクトのサブオブジェクトは、自動的に操作に含まれているとコピーまたは移動した[SPropTagArray](sproptagarray.md)構造体で示されているプロパティの使用に関係なく、完全に。 既定では、 **CopyProps**には、ソース オブジェクトからプロパティに一致する対象のオブジェクトのプロパティが上書きされます。 コピー先オブジェクトにコピーまたは移動先のプロパティのいずれかの場合、 _ulFlags_パラメーターに MAPI_NOREPLACE フラグが設定されていない限り、既存のプロパティが新しいプロパティによって上書きされます。 変更は上書きされず、変換先オブジェクトの既存の情報は行われないです。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**CopyProps**の完全な実装を提供するか、サポート オブジェクトは、MAPI が提供する実装に依存します。 MAPI 実装を使用する場合は、 **IMAPISupport::DoCopyProps**メソッドを呼び出します。 ただし、 **DoCopyProps**に処理を委任する操作を行います、MAPI_DECLINE_OK フラグが渡されますが、サポートの呼び出しを避けるため、代わりに MAPI_E_DECLINE_COPY を返します。 呼び出されますこのフラグを持つフォルダーをコピーする場合に発生する可能性のある再帰を回避するのには MAPI によって。 
  
コピー操作できますが、時間がかかるため、進行状況インジケーターを表示する必要があります。 いずれかを使用する必要がある場合は、 _lpProgress_パラメーターに渡される[IMAPIProgress](imapiprogressiunknown.md)の実装を使用します。 _LpProgress_が**null**の場合は、MAPI 実装を使用する[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI_DECLINE_OK フラグを設定しません。メッセージ ストア プロバイダーの**CopyProps**の実装への呼び出しで MAPI によって使用されます。 
  
のコピーと移動の操作に時間がかかる場合、MAPI_DIALOG フラグを設定することにより、進行状況インジケーターの表示を要求することをお勧めします。 **IMAPIProgress**で、いずれかの操作をした場合の実装に、または**null**には、 _lpProgress_パラメーターを設定できます。 _LpProgress_が**null**の場合は、 **CopyProps**は MAPI によって提供される既定の進行状況のインジケーターを使用します。 
  
MAPI_DIALOG フラグを設定しない、進行状況インジケーターの表示を抑制できます。 **CopyProps**は、 _ulUIParam_および_lpProgress_パラメーターを無視して、インジケーターが表示されないようにします。 
  
 **CopyProps**には、グローバルおよび個々 のエラーの場合、またはプロパティのいずれかで発生するエラーを報告できます。 これらの個々 のエラーは、 **SPropProblemArray**構造体に配置されます。 **Null**、代わりに、プロパティの問題の配列構造体のパラメーターの有効なポインターを渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。 
  
エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。 **CopyProps**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。 **CopyProps**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。 代わりに、詳細なエラー情報を取得するために[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
  
**CopyProps**では、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。 
  
ソース オブジェクトの種類に固有のプロパティをコピーする場合は、目的のオブジェクトが同じ型のあることを確認の操作を行う必要があります。 **CopyProps**ができないから、通常、1 種類のオブジェクトの別の種類のオブジェクトに属するプロパティを関連付けることです。 変換先オブジェクトのプロパティをコピーすることの責任です。 などのアドレス帳コンテナーにメッセージのプロパティをコピーする必要がありますされません。 
  
同じ種類のオブジェクト間でコピーしていることを確認するには、元とコピー先のオブジェクトが同じ型、オブジェクトのポインターを比較するか、 [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出すことを確認してください。 ソース オブジェクトの標準的なインタ フェースを_lpInterface_が指すインターフェイスの識別子を設定します。 オブジェクト タイプまたは**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティは、2 つのオブジェクトに対して同じであることを確認してください。 たとえば、メッセージからコピーする場合は、IID_IMessage と MAPI_MESSAGE を両方のオブジェクトの**PR_OBJECT_TYPE**に_lpInterface_を設定します。 
  
場合は、 _lpDestObj_パラメーターに無効なポインターが渡されると、結果は予測できません。 
  
メッセージの受信者のリストをコピーするには、メッセージの**CopyProps**メソッドを呼び出すし、プロパティ タグ配列の**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティが含まれます。 メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティが含まれます。 
  
フォルダーまたはアドレス帳コンテナーの階層構造または内容のテーブルをコピーするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のプロパティで、プロパティ タグの配列です。 フォルダーの内容を関連するテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) のプロパティを配列に指定します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI では、1 つのメッセージから名前付きプロパティをコピーするのにには、 **IMAPIProp::CopyProps**メソッドを使用します。  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI では、 **IMAPIProp::CopyProps**メソッドを使用して、別のオブジェクトからコピーされたプロパティを貼り付けます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)
  
[PidTagFolderAssociatedContents 標準プロパティ](pidtagfolderassociatedcontents-canonical-property.md)
  
[PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[PidTagObjectType 標準プロパティ](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

