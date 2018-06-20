---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1040a0730c4b26b51d3c2b7763488502b2c5323c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800754"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**適用されます**: Outlook 
  
明確に除外されたプロパティを 1 つのオブジェクトのすべてのプロパティを別のオブジェクトを移動またはコピーします。
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> [in]コピーまたは移動するにはプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcObj_
  
> [in]コピーまたは移動するにはプロパティを持つオブジェクトへのポインター。
    
 _ciidExclude_
  
> [in]コピーまたはプロパティを移動する際に除外するインターフェイスの数。
    
 _rgiidExclude_
  
> [in]コピーまたは変換先オブジェクトに補足的な情報を移動するときに使用しないインターフェイスを示すインターフェイス識別子の配列。
    
 _lpExcludeProps_
  
> [in]コピーから除外する必要がありますまたは移動操作のプロパティ タグを識別するプロパティ タグ配列へのポインター。 _LpExcludeProps_パラメーターに NULL を渡すことでは、あるすべてのオブジェクトのプロパティがコピーまたは移動することを示します。 **DoCopyTo**は、MAPI_E_INVALID_PARAMETER、**あう**、 [SPropTagArray](sproptagarray.md)構造体のメンバーが_lpExcludeProps_で示される場合は 0 に設定を取得します。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpProgress_
  
> [in]進行状況インジケーターの実装へのポインター。 _LpProgress_パラメーターに NULL を渡した場合、MAPI は、進行状況の実装を提供します。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。 
    
 _lpDestInterface_
  
> [in]コピーまたは移動先のプロパティを表示するオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子へのポインター。
    
 _lpDestObj_
  
> [in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> 進行状況のインジケーターが表示されます。 
    
MAPI_MOVE 
  
> **DoCopyTo**は、コピー操作ではなく移動操作を実行する必要があります。 このフラグが設定されていない場合、 **DoCopyTo**は、コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> コピー先オブジェクトの既存のプロパティを上書きしてはなりません。 このフラグが設定されていない場合、 **DoCopyTo**には、既存のプロパティが上書きされます。 
    
 _lppProblems_
  
> [out][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL、エラー情報の必要性を示すしません。 _LppProblems_が入力時に有効なポインターである場合は、 **DoCopyTo**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティは、正常にコピーまたは移動されています。
    
MAPI_E_COLLISION 
  
> 先のオブジェクトのプロパティをコピーまたは移動を既にが存在して MAPI_NOREPLACE フラグを設定します。 
    
MAPI_E_FOLDER_CYCLE 
  
> ソース オブジェクトには直接または間接的に目的のオブジェクトが含まれています。 重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _LpSrcObj_が指すオブジェクトでは、 _lpSrcInterface_パラメーターで指定されたインターフェイスはサポートされていない、または_の lpDestObj が指すオブジェクトでは、 _lpDestInterface_パラメーターで指定されたインターフェイスはサポートされていません_. 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。 目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。
    
MAPI_E_INVALID_PARAMETER 
  
> _LpSrcInterface_パラメーターは、NULL です。 
    
次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**DoCopyTo**。 これらのエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された**DoCopyTo**は、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**DoCopyTo**は、Unicode だけをサポートしています。 
    
MAPI_E_COMPUTED 
  
> コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。 このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの型が正しくありません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元の型ではありません。
    
## <a name="remarks"></a>備考

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::DoCopyTo**メソッドを実装します。 メッセージ ストア プロバイダーは、そのフォルダーとメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを実装するために**DoCopyTo**を呼び出すことができます。 
  
既定では、 **DoCopyTo**にコピーまたはすべて 1 つのオブジェクトのプロパティの別のオブジェクトを移動します。 ソース オブジェクトのサブオブジェクトに自動的に操作に含まれているとコピーまたは移動の全体です。 
  
コピー先オブジェクトにコピーまたは移動先のプロパティのいずれかの場合、 _ulFlags_パラメーターに MAPI_NOREPLACE フラグが設定されていない限り、既存のプロパティが新しいプロパティによって上書きされます。 変更は上書きされず、変換先オブジェクトの既存の情報は行われないです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

除外するプロパティのコピーか移動の操作を_lpExcludeProps_パラメーターで、プロパティ タグが含まれます。 プロパティ タグ プロパティ タグ配列内の特定の識別子からを構築する[PROP_TAG](prop_tag.md)マクロを使用する場合の結果を渡すと、その識別子を持つすべてのプロパティは除外されます。 たとえば、プロパティ タグ配列内の次のエントリでは、種類に関係なく、除外する 0x8002 の識別子を持つすべてのプロパティが発生します。 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
プロパティをコピーすると、メッセージを別のフォルダーに**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定するメッセージの配信時刻をコピーしないようにするのには、タグは、配列を除外します。 メッセージの受信者の一覧を除外するには、除外アレイに**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティを追加します。 メッセージの添付ファイルを除外するには、配列に**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティを追加します。
  
同様に、コピーまたはフォルダー、アドレス帳コンテナーの階層、または内容のテーブルの移動を防ぐためには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティのタグは配列を除外します。
  
MAPI_E_COMPUTED を無視して、 **SPropProblemArray**パラメーターに構造体の_lppProblems_でエラーが返されます。 
  
_LpSrcInterface_ポイントは、通常、インターフェイス識別子と同じを_lpDestInterface_が指すインターフェイスの識別子です。 
  
_LpDestInterface_で受け入れ可能なインタ フェース識別子が_lpDestObj_に無効なポインターを渡す場合、結果は予測できません。 ほとんどの場合、プロバイダーは失敗になります。 
  
逆に、コピーまたは移動する必要がありますはない補足的な情報に注意してください場合は、 _rgiidExclude_パラメーターに渡される配列に除外するインターフェイスのインターフェイス識別子を追加します。 たとえば、コピーする場合は、メッセージが、メッセージの添付ファイルのいずれかのない、 _rgiidExclude_配列の IID_IMessage を渡します。 **DoCopyTo**では、認識されない_rgiidExclude_に記載されているすべてのインタ フェースを無視します。 
  
インタ フェースを除外するのには、 _rgiidExclude_パラメーターを使用する場合も、そのインターフェイスから派生するすべてのインタ フェースを除外します。 などの[IMAPIContainer](imapicontainerimapiprop.md)インタ フェースを除外すると、フォルダーまたはプロバイダーの種類によって、除外するアドレス帳のコンテナー。 非常に多くのインターフェイスは、それらから派生するために[IMAPIProp](imapipropiunknown.md)または[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)を除外しません。 
  
 **DoCopyTo**では、全体として操作に適用されるグローバル エラーと個々 のプロパティに適用される個々 のエラーを報告します。 これらの個々 のエラーは、 **SPropProblemArray**構造体に配置されます。 プロパティ問題配列構造体パラメーターに有効なポインターではなく NULL を渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。 
  
エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。 **DoCopyTo**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。 **DoCopyTo**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。 代わりに、詳細なエラー情報を取得するために[IMAPISupport::GetLastError](imapisupport-getlasterror.md)メソッドを呼び出します。 
  
**DoCopyTo**では、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。 
  
**DoCopyTo**の呼び出しでは、グローバル エラーが発生する場合を使用したりしないで、 **SPropProblemArray**構造体を解放します。 プロバイダーは、 **DoCopyTo**によって返された**SPropProblemArray**構造体の_ulIndex_メンバーを無視してください。
  
## <a name="see-also"></a>関連項目



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[PidTagContainerContents の標準的なプロパティ](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy の標準的なプロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagMessageAttachments の標準的なプロパティ](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageDeliveryTime の標準的なプロパティ](pidtagmessagedeliverytime-canonical-property.md)
  
[PidTagMessageRecipients の標準的なプロパティ](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

