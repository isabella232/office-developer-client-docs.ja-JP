---
title: IMAPIPropCopyTo
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800649"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**適用されます**: Outlook 
  
明確に除外されたプロパティ以外のすべてのプロパティを移動またはコピーします。
  
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

## <a name="parameters"></a>Parameters

 _ciidExclude_
  
> [in]プロパティをコピーまたは移動した場合を除外するのにはインターフェイスの数。
    
 _rgiidExclude_
  
> [in]補足情報をコピーまたは移動先のオブジェクトに移動するとき使用しないインターフェイスを指定するインターフェイス id (Iid) の配列です。
    
 _lpExcludeProps_
  
> [in]コピーから除外する必要がありますまたは移動操作のプロパティ タグを識別するプロパティ タグ配列へのポインター。 _LpExcludeProps_パラメーターに**null**を渡す場合に、されるすべてのオブジェクトのプロパティがコピーまたは移動することを示します。 **CopyTo**は、MAPI_E_INVALID_PARAMETER、**あう**、 [SPropProblemArray](spropproblemarray.md)構造体のメンバーが_lpExcludeProps_で示される場合は 0 に設定を取得します。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpProgress_
  
> [in]進行状況インジケーターの実装へのポインター。 **Null**が渡された場合、 _lpProgress_パラメーターで、MAPI は、進行状況の実装を提供します。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。 
    
 _lpInterface_
  
> [in]_LpDestObj_パラメーターが指すオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインターです。 _LpInterface_パラメーターを**null**にするにはできません。
    
 _lpDestObj_
  
> [in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DECLINE_OK 
  
> 場合は、 **CopyTo**メソッドを呼び出して、 [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)処理、コピーまたは移動操作は、代わりにすぐに MAPI_E_DECLINE_COPY のエラー値を返す必要があります。 MAPI_DECLINE_OK フラグは、再帰を制限するのには MAPI によって設定されています。 クライアントでは、このフラグは設定されません。 
    
MAPI_DIALOG 
  
> 進行状況のインジケーターが表示されます。
    
MAPI_MOVE 
  
> **CopyTo**は、コピー操作ではなく移動操作を実行する必要があります。 このフラグが設定されていない、 **CopyTo**は、コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> コピー先オブジェクトの既存のプロパティを上書きしてはなりません。 このフラグが設定されていない、 **CopyTo**によって既存のプロパティが上書きされます。 
    
 _lppProblems_
  
> [で [チェック アウト]**SPropProblemArray**構造体へのポインターへのポインターの入力でそれ以外の場合、 **null**、エラー情報の必要性がないことを示します。 _LppProblems_が入力時に有効なポインターである場合は、 **CopyTo**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティは、正常にコピーまたは移動されています。
    
MAPI_E_COLLISION 
  
> サブオブジェクトと同じ名前を表示するためにサブオブジェクトをコピーすることはできません- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティで指定された、目的のオブジェクトに既に存在します。 
    
MAPI_E_DECLINE_COPY 
  
> サービス プロバイダーは、コピー操作を実装していません。
    
MAPI_E_FOLDER_CYCLE 
  
> ソース オブジェクトが直接的または間接的にコピーまたは移動操作を実行するには、目的のオブジェクトが含まれています。 重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> 先のオブジェクトでは、 _lpInterface_パラメーターで指定されたインターフェイスはサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。 目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。
    
次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**CopyTo**です。 次のエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された**CopyTo**は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、 **CopyTo**は、Unicode だけをサポートしています。 
    
MAPI_E_COMPUTED 
  
> コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。 このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの型が正しくありません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元の型ではありません。
    
## <a name="remarks"></a>備考

既定では、 **IMAPIProp::CopyTo**メソッドは、コピーまたは、すべての現在のオブジェクトのプロパティをコピー先のオブジェクトに移動します。 **CopyTo**は、オブジェクトをコピーまたはすべてまたはほとんどのプロパティをそのままの状態を正確に移動する必要があるときに使用されます。 
  
ソース オブジェクトのサブオブジェクト操作に自動的に含まれ、コピーまたは移動の全体。 **CopyTo**は既定では、ソース オブジェクトからプロパティに一致する対象のオブジェクトのプロパティを上書きします。 コピー先オブジェクトにコピーまたは移動先のプロパティのいずれかの場合、 _ulFlags_パラメーターに MAPI_NOREPLACE フラグが設定されていない限り、既存のプロパティが新しいプロパティによって上書きされます。 変更は上書きされず、変換先オブジェクトの既存の情報は行われないです。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**CopyTo**の完全な実装を提供するか、サポート オブジェクトは、MAPI が提供する実装に依存します。 MAPI 実装を使用する場合は、 **IMAPISupport::DoCopyTo**を呼び出します。 ただし、 **DoCopyTo**に処理を委任する操作を行います、MAPI_DECLINE_OK フラグが渡されますが、サポートの呼び出しを避けるため、代わりに MAPI_E_DECLINE_COPY を返します。 MAPI は、フォルダーがコピーされるときに発生する可能性のある再帰を回避するには、このフラグを呼び出します。 
  
コピー操作できますが、時間がかかるため、進行状況インジケーターを表示する必要があります。 いずれかを使用する必要がある場合は、 _lpProgress_パラメーターに渡された[IMAPIProgress](imapiprogressiunknown.md)の実装を使用します。 _LpProgress_が**null**の場合は、MAPI 実装を使用する[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。 
  
目的のオブジェクトのすべての既知の読み取り専用プロパティを設定しようとはしないで代わりに MAPI_E_NO_ACCESS を返します。
  
元とコピー先のオブジェクトは、同じインターフェイスを使用する必要があります。 _LpInterface_が設定されていない場合は、MAPI_E_INVALID_PARAMETER を返します。 
  
既知のすべてのインタ フェースが除外されている場合は、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI_DECLINE_OK フラグを設定しません。MAPI の呼び出しでメッセージのストア プロバイダーの**CopyTo**の実装に使用します。 
  
のコピーと移動の操作に時間がかかる場合、MAPI_DIALOG フラグを設定することにより、進行状況インジケーターの表示を要求する必要があります。 **IMAPIProgress**で、いずれかの操作をした場合の実装に、または**null**には、 _lpProgress_パラメーターを設定できます。 _LpProgress_が**null**の場合は、 **CopyTo**は MAPI が提供する既定の進行状況のインジケーターを使用します。 
  
MAPI_DIALOG フラグを設定しない、進行状況インジケーターの表示を抑制できます。 **CopyTo**は、 _ulUIParam_と_lpProgress_のパラメーターは無視され、インジケーターは表示されません。 
  
 **CopyTo**は、グローバルおよび個々 のエラーの場合、または 1 つまたは複数のプロパティを使用して発生したエラーを報告できます。 これらの個々 のエラーは、 **SPropProblemArray**構造体に格納されます。 **Null**、代わりに、プロパティの問題の配列構造体のパラメーターの有効なポインターを渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。 
  
エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。 **CopyTo**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。 **CopyTo**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。 代わりに、詳細なエラー情報を取得するために[IMAPIProp::GetLastError](imapiprop-getlasterror.md) 。 
  
**CopyTo**には、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。 
  
ソース オブジェクトの種類に固有のプロパティをコピーする場合、同じ種類の対象になるオブジェクトであるようにしてください。 **CopyTo**ができないから、通常、1 種類のオブジェクトの別の種類のオブジェクトに属するプロパティを関連付けることです。 変換先オブジェクトのプロパティをコピーすることの責任です。 などのアドレス帳コンテナーにメッセージのプロパティをコピーする必要がありますされません。 
  
同じ種類のオブジェクト間でコピーすることを確認するには、元とコピー先のオブジェクトが同じ型、オブジェクトのポインターを比較するか、 [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)を呼び出すことを確認してください。 ソース オブジェクトの標準的なインタ フェースを_lpInterface_が指すインターフェイスの識別子を設定します。 また、オブジェクト タイプまたは**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティは、2 つのオブジェクトに対して同じであることを確認してください。 たとえば、メッセージからコピーする場合は、IID_IMessage と MAPI_MESSAGE を両方のオブジェクトの**PR_OBJECT_TYPE**に_lpInterface_を設定します。 
  
場合は、 _lpDestObj_パラメーターに無効なポインターが渡されると、結果は予測できません。 
  
**CopyTo**の呼び出しでプロパティを除外できます。 などのいくつかのオブジェクトには、日付と時刻のメッセージの配信など、オブジェクトの単一のインスタンスに固有のプロパティがあります。 プロパティをコピーすると、メッセージを別のフォルダーに**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定するメッセージの配信時刻をコピーしないようにするのには、タグは、配列を除外します。 メッセージの受信者の一覧を除外するには、除外アレイに**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティを追加します。 メッセージの添付ファイルを除外するには、配列に**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティを追加します。
  
同様に、コピーまたは移動するフォルダーまたはアドレス帳コンテナーの階層構造または内容のテーブルを防ぐため、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([を含めることで、PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティのタグは配列を除外します。
  
除外するプロパティのコピーか移動の操作を_lpExcludeProps_パラメーターで、プロパティ タグが含まれます。 プロパティ タグ プロパティ タグ配列内の特定の識別子からを構築する**PROP_TAG**マクロの結果を渡すと、その識別子を持つすべてのプロパティは除外されます。 たとえば、プロパティ タグ配列内の次のエントリでは、種類に関係なく、除外する 0x8002 の識別子を持つすべてのプロパティが発生します。 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
_LpExcludeProps_アレイでは、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) のプロパティ タグを含めることができません。 
  
インタ フェースを除外するための**CopyTo**機能の有用性はおそらくプロパティを除外することの有用性としては明らかにします。 プロパティのグループの知識を持たないオブジェクトにコピーするときは、インタ フェースを除外できます。 などのプロパティをフォルダーから添付ファイルをコピーする場合、添付ファイルが使用できる唯一のプロパティ、 [IMAPIProp](imapipropiunknown.md)実装で利用可能な汎用的なプロパティです。 コピー操作から[IMAPIFolder](imapifolderimapicontainer.md)を除外することで添付ファイルを受信しません、特定のフォルダーのプロパティのいずれか。 
  
インタ フェースを除外するのには、 _rgiidExclude_パラメーターを使用する場合も、そのインターフェイスから派生するすべてのインタ フェースを除外します。 たとえば、 [IMAPIContainer](imapicontainerimapiprop.md)を除外すると、フォルダーまたはプロバイダーの種類によって、除外するアドレス帳のコンテナー。 非常に多くのインターフェイスは、それらから派生するために**IMAPIProp**または[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)を除外しません。 
  
MAPI_E_COMPUTED を無視して、 **SPropProblemArray**パラメーターに構造体の_lppProblems_でエラーが返されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI では、 [IMAPIMessageSite](imapimessagesiteiunknown.md)オブジェクトに .msg ファイルからプロパティをコピーするのには、 **IMAPIProp::CopyTo**メソッドを使用します。  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI では、 **IMAPIProp::CopyTo**メソッドを使用して、貼り付けの操作中に、対象のメッセージを送信元のメッセージからプロパティをコピーします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerContents の標準的なプロパティ](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy の標準的なプロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagMessageAttachments の標準的なプロパティ](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageDeliveryTime の標準的なプロパティ](pidtagmessagedeliverytime-canonical-property.md)
  
[PidTagMessageRecipients の標準的なプロパティ](pidtagmessagerecipients-canonical-property.md)
  
[PidTagObjectType の標準的なプロパティ](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

