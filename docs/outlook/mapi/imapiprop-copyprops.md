---
title: imapipropcopyprops
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
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345508"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
選択されたプロパティをコピーまたは移動します。 
  
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

 _lpincludeprops_
  
> 順番コピーまたは移動するプロパティを指定するプロパティタグ配列へのポインター。 **PR_NULL**([PidTagNull](pidtagnull-canonical-property.md)) を配列に含めることはできません。 _lpincludeprops_パラメーターを**null**にすることはできません。
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpprogress_
  
> 順番進行状況インジケーターの実装へのポインター。 _lpprogress_パラメーターで**null**が渡された場合は、MAPI 実装を使用して進行状況インジケーターが表示されます。 MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。 
    
 _lpinterface_
  
> 順番_lpdestobj_パラメーターによって指定されたオブジェクトへのアクセスに使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lpinterface_パラメーターを**null**にすることはできません。
    
 _lpdestobj_
  
> 順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> 順番コピー操作または移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DECLINE_OK 
  
> **copyprops**が[imapisupport::D ocopyprops](imapisupport-docopyprops.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、エラー値 MAPI_E_DECLINE_COPY を使用して直ちに戻る必要があります。 MAPI_DECLINE_OK フラグは、再帰を制限するために MAPI によって設定されます。 クライアントはこのフラグを設定しません。 
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。
    
MAPI_MOVE 
  
> **copyprops**はコピー操作ではなく、移動操作を実行する必要があります。 このフラグが設定されていない場合、 **copyprops**はコピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。 このフラグが設定されていない場合、 **copyprops**は既存のプロパティを上書きします。 
    
 _lppproblems 問題_
  
> [入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は**null**。エラー情報を必要としないことを示します。 _lppproblems_が入力の有効なポインターの場合、 **copyprops**は1つまたは複数のプロパティをコピーするときのエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで定義されているのと同じ表示名を持つサブオブジェクトが、対象オブジェクト内に既に存在するため、サブオブジェクトをコピーできません。 
    
MAPI_E_DECLINE_COPY 
  
> サービスプロバイダーがコピー操作を実装していません。
    
MAPI_E_FOLDER_CYCLE 
  
> コピーまたは移動操作を直接または間接的に実行しているソースオブジェクトは、目的のオブジェクトを直接または間接的に格納します。 この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpinterface_パラメーターで指定されたインターフェイスは、destination オブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。 destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。
    
次の値は、 **spropの配列**構造で返すことができますが、 **copyprops**の戻り値として返すことはできません。 これらのエラーは、1つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、 **copyprops**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **copyprops**は unicode のみをサポートしています。 
    
MAPI_E_COMPUTED 
  
> このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元が想定した型ではありません。
    
## <a name="remarks"></a>解説

**imapiprop:: copyprops**メソッドは、選択したプロパティを現在のオブジェクトから移動先のオブジェクトにコピーまたは移動します。 **copyprops**は、主に、元のメッセージの一部のプロパティのみが返信または転送されたコピーで送信されるメッセージの返信と転送に使用します。 
  
[SPropTagArray](sproptagarray.md)構造体で指定されたプロパティの使用に関係なく、ソースオブジェクト内のすべてのサブオブジェクトは、自動的に操作に含まれ、コピーまたは移動されます。 既定では、 **copyprops**は、source オブジェクトのプロパティに一致する destination オブジェクト内のすべてのプロパティを上書きします。 コピーまたは移動されたプロパティのいずれかがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが_ulflags_パラメーターで設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。 上書きされていない対象のオブジェクト内の既存の情報は、そのまま残ります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**copyprops**の完全な実装を提供することも、MAPI がサポートオブジェクトで提供する実装を利用することもできます。 MAPI 実装を使用する場合は、 **imapisupport::D ocopyprops**メソッドを呼び出します。 ただし、 **docopyprops**に対して処理を委任し、MAPI_DECLINE_OK フラグが渡された場合は、サポートコールを避け、代わりに MAPI_E_DECLINE_COPY を返します。 フォルダーのコピー時に発生する可能性のある再帰を回避するために、このフラグを使用して MAPI によって呼び出されます。 
  
コピー操作に長い時間がかかる可能性があるため、進行状況インジケーターを表示する必要があります。 _lpprogress_パラメーターに渡された[imapiprogress](imapiprogressiunknown.md)実装を使用します (存在する場合)。 _lpprogress_が**null**の場合は、MAPI 実装を使用するために[imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI_DECLINE_OK フラグは設定しません。これは、メッセージストアプロバイダーの**copyprops**実装への呼び出しで MAPI によって使用されます。 
  
コピー操作および移動操作は時間がかかることがあるため、MAPI_DIALOG フラグを設定して進行状況インジケーターの表示を要求することをお勧めします。 _lpprogress_パラメーターは、 **imapiprogress**の実装に設定できます (存在する場合)。それ以外の場合は**null**に設定できます。 _lpprogress_が**null**の場合、 **copyprops**は MAPI によって提供される既定の進行状況インジケーターを使用します。 
  
MAPI_DIALOG フラグを設定しないと、進行状況インジケーターの表示を抑制することができます。 **copyprops**は_uluiparam_パラメーターと_lpprogress_パラメーターを無視し、インジケーターを表示しないようにします。 
  
 **copyprops**では、グローバルおよび個別のエラー、あるいは1つ以上のプロパティで発生するエラーを報告できます。 これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。 プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく**null**を渡すことにより、プロパティレベルでエラー報告を抑制することができます。 
  
エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。 **copyprops**が S_OK を返す場合は、構造内の各プロパティにエラーがあるかどうかを確認します。 **copyprops**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。 代わりに、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出して詳細なエラー情報を取得します。 
  
**copyprops**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。 
  
ソースオブジェクトの種類に固有のプロパティをコピーする場合は、対象のオブジェクトが同じ種類であることを確認する必要があります。 **copyprops**では、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けることができます。 目的のオブジェクトに適したプロパティをコピーするのは、自分のユーザーです。 たとえば、メッセージのプロパティをアドレス帳のコンテナーにコピーしないでください。 
  
同じ種類のオブジェクト間でコピーしていることを確認するには、オブジェクトポインターを比較するか、または[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出して、コピー元とコピー先のオブジェクトが同じ種類であることを確認します。 _lpinterface_で示されるインターフェイス識別子を、source オブジェクトの標準インターフェイスに設定します。 また、オブジェクトの種類または**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティが、2つのオブジェクトに対して同じであることを確認してください。 たとえば、メッセージからコピーする場合は、 _lpinterface_を IID_IMessage に、両方のオブジェクトの**PR_OBJECT_TYPE**を MAPI_MESSAGE に設定します。 
  
_lpdestobj_パラメーターに無効なポインターが渡された場合、結果は予測できません。 
  
メッセージの宛先リストをコピーするには、メッセージの**copyprops**メソッドを呼び出して、property タグ配列に**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを含めます。 メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含めます。 
  
フォルダーまたはアドレス帳のコンテナーの階層またはコンテンツテーブルをコピーするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを追加します。プロパティタグ配列。 フォルダーに関連付けられたコンテンツテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを配列に含めます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |copynamedprops  <br/> |mfcmapi は、 **imapiprop:: copyprops**メソッドを使用して、あるメッセージから別のメッセージに名前付きプロパティをコピーします。  <br/> |
|SingleMAPIPropListCtrl  <br/> |CSingleMAPIPropListCtrl:: OnPasteProperty  <br/> |mfcmapi は、 **imapiprop:: copyprops**メソッドを使用して、別のオブジェクトからコピーされたプロパティを貼り付けます。  <br/> |
   
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

