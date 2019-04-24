---
title: imapipropcopyto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356393"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
明示的に除外されているプロパティ以外のすべてのプロパティをコピーまたは移動します。
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _ciidExclude_
  
> 順番プロパティがコピーまたは移動されたときに除外するインターフェイスの数。
    
 _rgiidExclude_
  
> 順番追加情報をコピーまたは移動先オブジェクトに移動するときに使用しないインターフェイスを指定するインターフェイス識別子 (IIDs) の配列。
    
 _lpexcludeprops_
  
> 順番コピー操作または移動操作から除外する必要があるプロパティタグを識別するプロパティタグ配列へのポインター。 _lpexcludeprops_パラメーターで**null**を渡すことは、オブジェクトのすべてのプロパティをコピーまたは移動する必要があることを示します。 _lpexcludeprops_によって指定される[spropprops 配列](spropproblemarray.md)構造の**cvalues**メンバが0に設定されている場合、 **CopyTo**は MAPI_E_INVALID_PARAMETER を返します。 
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpprogress_
  
> 順番進行状況インジケーターの実装へのポインター。 _lpprogress_パラメーターで**null**が渡された場合、MAPI は進行状況の実装を提供します。 MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。 
    
 _lpinterface_
  
> 順番_lpdestobj_パラメーターによって指定されたオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lpinterface_パラメーターを**null**にすることはできません。
    
 _lpdestobj_
  
> 順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> 順番コピー操作または移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DECLINE_OK 
  
> **CopyTo**が[imapisupport::D ocopyto](imapisupport-docopyto.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、エラー値 MAPI_E_DECLINE_COPY を使用して直ちに戻る必要があります。 MAPI_DECLINE_OK フラグは、再帰を制限するために MAPI によって設定されます。 クライアントはこのフラグを設定しません。 
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。
    
MAPI_MOVE 
  
> **CopyTo**では、コピー操作の代わりに移動操作を実行する必要があります。 このフラグが設定されていない場合、 **CopyTo**はコピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。 このフラグが設定されていない場合、 **CopyTo**は既存のプロパティを上書きします。 
    
 _lppproblems 問題_
  
> [入力]input の場合は、 **spropの配列**構造体へのポインターへのポインターを返します。それ以外の場合、エラー情報を必要としないことを示す**null**。 _lppproblems_が入力の有効なポインターである場合、 **CopyTo**は1つ以上のプロパティをコピーする際のエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティによって指定された同じ表示名のサブオブジェクトが対象オブジェクトに既に存在しているため、サブオブジェクトをコピーできません。 
    
MAPI_E_DECLINE_COPY 
  
> サービスプロバイダーがコピー操作を実装していません。
    
MAPI_E_FOLDER_CYCLE 
  
> コピーまたは移動操作を直接または間接的に実行しているソースオブジェクトは、目的のオブジェクトを直接または間接的に格納します。 この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpinterface_パラメーターで指定されたインターフェイスは、destination オブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。 destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。
    
次の値は、 **spropの配列**構造で返すことができますが、 **CopyTo**の戻り値としては返されません。 次のエラーが1つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されており、 **copyto**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **copyto**は unicode のみをサポートしています。 
    
MAPI_E_COMPUTED 
  
> このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元が想定した型ではありません。
    
## <a name="remarks"></a>解説

既定では、 **imapiprop:: CopyTo**メソッドは、現在のオブジェクトのすべてのプロパティを対象のオブジェクトにコピーまたは移動します。 **CopyTo**は、オブジェクトが正確にコピーまたは移動されるときに使用されます。プロパティのすべてまたはほとんどはそのままです。 
  
source オブジェクト内のすべてのサブオブジェクトは、自動的に操作に含まれ、全体でコピーまたは移動されます。 既定では、 **CopyTo**はコピー先オブジェクトのプロパティに一致するすべてのプロパティをソースオブジェクトから上書きします。 コピーまたは移動されたプロパティのいずれかがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが_ulflags_パラメーターで設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。 上書きされていない対象のオブジェクト内の既存の情報は、そのまま残ります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**CopyTo**の完全な実装を提供することも、MAPI がサポートオブジェクトで提供する実装に依存することもできます。 MAPI 実装を使用する場合は、 **imapisupport::D ocopyto**を呼び出します。 ただし、MAPI_DECLINE_OK フラグが渡された**** 場合に、委任処理を実行すると、サポートコールを避け、代わりに MAPI_E_DECLINE_COPY を返します。 MAPI は、フォルダーがコピーされたときに発生する可能性のある再帰を回避するために、このフラグを使用して呼び出します。 
  
コピー操作に長い時間がかかる可能性があるため、進行状況インジケーターを表示する必要があります。 _lpprogress_パラメーターに渡された[imapiprogress](imapiprogressiunknown.md)実装を使用します (存在する場合)。 _lpprogress_が**null**の場合は、MAPI 実装を使用するために[imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。 
  
対象のオブジェクトで読み取り専用プロパティを設定しようとしないでください。代わりに MAPI_E_NO_ACCESS を返します。
  
コピー元とコピー先のオブジェクトは、同じインターフェイスを使用する必要があります。 _lpinterface_が設定されていない場合は、MAPI_E_INVALID_PARAMETER を返します。 
  
既知のすべてのインターフェイスが除外されている場合は、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI_DECLINE_OK フラグは設定しません。MAPI では、メッセージストアプロバイダーの**CopyTo**実装への呼び出しでそれが使用されます。 
  
コピー操作および移動操作は時間がかかることがあるため、MAPI_DIALOG フラグを設定して進行状況インジケーターの表示を要求する必要があります。 _lpprogress_パラメーターは、 **imapiprogress**の実装に設定できます (存在する場合)。それ以外の場合は**null**に設定できます。 _lpprogress_が**null**の場合、 **CopyTo**は MAPI が提供する既定の進行状況インジケーターを使用します。 
  
MAPI_DIALOG フラグを設定しないと、進行状況インジケーターの表示を抑制することができます。 **CopyTo**では_uluiparam_パラメーターと_lpprogress_パラメーターは無視され、インジケーターは表示されません。 
  
 **CopyTo**では、グローバルおよび個別のエラー、あるいは1つ以上のプロパティで発生するエラーを報告できます。 これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。 プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく**null**を渡すことにより、プロパティレベルでエラー報告を抑制することができます。 
  
エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。 **CopyTo**が S_OK を返す場合は、構造内の個々のプロパティに関するエラーがあるかどうかを確認します。 **CopyTo**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。 代わりに、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)を呼び出して詳細なエラー情報を取得します。 
  
**CopyTo**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。 
  
ソースオブジェクトの種類に固有のプロパティをコピーする場合は、対象のオブジェクトが同じ種類であることを確認する必要があります。 **CopyTo**では、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けることはできません。 目的のオブジェクトに適したプロパティをコピーするのは、自分のユーザーです。 たとえば、メッセージのプロパティをアドレス帳のコンテナーにコピーしないでください。 
  
同じ種類のオブジェクト間でコピーされるようにするには、オブジェクトポインターを比較するか、 [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出して、コピー元とコピー先のオブジェクトが同じ種類であることを確認します。 _lpinterface_で示されるインターフェイス識別子を、source オブジェクトの標準インターフェイスに設定します。 また、オブジェクトの種類または**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティが、2つのオブジェクトに対して同じであることを確認してください。 たとえば、メッセージからコピーする場合は、 _lpinterface_を IID_IMessage に、両方のオブジェクトの**PR_OBJECT_TYPE**を MAPI_MESSAGE に設定します。 
  
_lpdestobj_パラメーターに無効なポインターが渡された場合、結果は予測できません。 
  
**CopyTo**呼び出しでプロパティを除外することが有用な場合があります。 たとえば、一部のオブジェクトには、オブジェクトの1つのインスタンスに固有のプロパティがあります (メッセージ配信の日時など)。 メッセージを別のフォルダーにコピーしたときにメッセージの配信時刻がコピーされないようにするには、property タグの除外配列で**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。 メッセージの宛先リストを除外するには、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。 メッセージの添付ファイルを除外するには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。
  
同様に、 **PR_CONTAINER_HIERARCHY** (PidTagContainerHierarchy) または PR_CONTAINER_CONTENTS ([](pidtagcontainerhierarchy-canonical-property.md)) または**** を含めることによって、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツテーブルをコピーまたは移動できないようにします ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティタグの除外配列。
  
コピー操作または移動操作からプロパティを除外するには、そのプロパティタグを_lpexcludeprops_パラメーターに含めます。 **PROP_TAG**マクロの結果を渡して、プロパティタグ配列の特定の識別子からプロパティタグを作成すると、その識別子を持つすべてのプロパティが除外されます。 たとえば、次のエントリをプロパティタグ配列に配置すると、型に関係なく、0x8002 の識別子が含まれるすべてのプロパティが除外されます。 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティタグを_lpexcludeprops_配列に含めることはできません。 
  
インターフェイスを除外するための**CopyTo**機能の有用性は、プロパティを除外することほど明確ではありません。 プロパティのグループについての知識がないオブジェクトにコピーするときに、インターフェイスを除外することができます。 たとえば、プロパティをフォルダーから添付ファイルにコピーした場合、添付ファイルで使用できるプロパティは、任意の[imapiprop](imapipropiunknown.md)実装で使用できる汎用プロパティだけです。 [imapifolder](imapifolderimapicontainer.md)をコピー操作から除外すると、添付ファイルは、より具体的なフォルダープロパティを受け取ることはありません。 
  
_rgiidExclude_パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したすべてのインターフェイスも除外されます。 たとえば、 [IMAPIContainer](imapicontainerimapiprop.md)を除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。 **imapiprop**または[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から派生しているインターフェイスが多いため、これを除外しないでください。 
  
_lppproblems_パラメーターの**sprop問題の配列**構造で返された MAPI_E_COMPUTED エラーを無視します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ファイル .cpp  <br/> |LoadFromMSG  <br/> |mfcmapi は、 **imapiprop:: CopyTo**メソッドを使用して、.msg ファイルのプロパティを[IMAPIMessageSite](imapimessagesiteiunknown.md)オブジェクトにコピーします。  <br/> |
|folderdlg  <br/> |cfolderdlg:: handlepaste  <br/> |mfcmapi は、 **imapiprop:: CopyTo**メソッドを使用して、貼り付け操作中にソースメッセージからターゲットメッセージにプロパティをコピーします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageDeliveryTime 標準プロパティ](pidtagmessagedeliverytime-canonical-property.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[PidTagObjectType 標準プロパティ](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

