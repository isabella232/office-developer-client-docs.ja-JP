---
title: imapisupportdocopyto
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331809"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
明示的に除外されたプロパティを除き、1つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。
  
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

## <a name="parameters"></a>パラメーター

 _lpsrcinterface_
  
> 順番コピーまたは移動するプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpsrcobj_
  
> 順番コピーまたは移動するプロパティを持つオブジェクトへのポインター。
    
 _ciidExclude_
  
> 順番プロパティをコピーまたは移動するときに除外するインターフェイスの数。
    
 _rgiidExclude_
  
> 順番ターゲットオブジェクトに補足情報をコピーまたは移動するときに使用しないインターフェイスを示すインターフェイス識別子の配列。
    
 _lpexcludeprops_
  
> 順番コピー操作または移動操作から除外する必要があるプロパティタグを識別するプロパティタグ配列へのポインター。 _lpexcludeprops_パラメーターで NULL を渡すことは、オブジェクトのすべてのプロパティをコピーまたは移動する必要があることを示します。 _lpexcludeprops_によって参照される[SPropTagArray](sproptagarray.md)構造の**cvalues**メンバが0に設定されている場合、 **docopyto**は MAPI_E_INVALID_PARAMETER を返します。 
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpprogress_
  
> 順番進行状況インジケーターの実装へのポインター。 _lpprogress_パラメーターで NULL が渡された場合、MAPI は進行状況の実装を提供します。 MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。 
    
 _lpdestinterface_
  
> 順番コピーまたは移動したプロパティを受け取るためのオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子へのポインター。
    
 _lpdestobj_
  
> 順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> 順番コピー操作または移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。 
    
MAPI_MOVE 
  
> **docopyto**はコピー操作ではなく移動操作を実行する必要があります。 このフラグが設定されて**** いない場合は、コピー操作が実行されます。 
    
MAPI_NOREPLACE 
  
> 対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。 このフラグが設定されていない場合、 **docopyto**は既存のプロパティを上書きします。 
    
 _lppproblems 問題_
  
> 読み上げinput の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は、エラー情報を必要としないことを示す NULL。 _lppproblems_が入力の有効なポインターである場合、 **docopyto**は、1つ以上のプロパティをコピーする際のエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> コピーまたは移動されるプロパティは、対象オブジェクトに既に存在し、MAPI_NOREPLACE フラグが設定されています。 
    
MAPI_E_FOLDER_CYCLE 
  
> source オブジェクトは、直接または間接的に対象のオブジェクトを含みます。 この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpsrcinterface_パラメーターで指定されたインターフェイスは、 _lpsrcobj_が指すオブジェクトではサポートされていません。 __ lpsrcinterface パラメーターによって識別されるインターフェイスは、lpsrcinterface が指すオブジェクトではサポートされていません。 __. 
    
MAPI_E_NO_ACCESS 
  
> 発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。 destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。
    
MAPI_E_INVALID_PARAMETER 
  
> _lpsrcinterface_パラメーターが NULL です。 
    
次の値は、 **spropの配列**構造で返すことができますが、 **docopyto**の戻り値として返すことはできません。 これらのエラーは、1つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されており、 **docopyto**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **docopyto**で unicode のみがサポートされています。 
    
MAPI_E_COMPUTED 
  
> このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元が想定した型ではありません。
    
## <a name="remarks"></a>解説

**imapisupport::D ocopyto**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは、 **docopyto**を呼び出して、フォルダーとメッセージに[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを実装できます。 
  
既定では、 **docopyto**は、1つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。 source オブジェクト内のすべてのサブオブジェクトは、自動的に操作に含まれ、全体でコピーまたは移動されます。 
  
コピーまたは移動されたプロパティのいずれかがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが_ulflags_パラメーターで設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。 上書きされていない対象のオブジェクト内の既存の情報は、そのまま残ります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

コピー操作または移動操作からプロパティを除外するには、そのプロパティタグを_lpexcludeprops_パラメーターに含めます。 [PROP_TAG](prop_tag.md)マクロを使用した結果を渡して、プロパティタグ配列の特定の識別子からプロパティタグを作成すると、その識別子を持つすべてのプロパティが除外されます。 たとえば、次のエントリをプロパティタグ配列に配置すると、型に関係なく、0x8002 の識別子が含まれるすべてのプロパティが除外されます。 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
メッセージを別のフォルダーにコピーしたときにメッセージの配信時刻がコピーされないようにするには、property タグの除外配列で**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。 メッセージの宛先リストを除外するには、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。 メッセージの添付ファイルを除外するには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。
  
同様に、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツテーブルをコピーまたは移動できないようにするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティタグの除外配列。
  
_lppproblems_パラメーターの**sprop問題の配列**構造で返された MAPI_E_COMPUTED エラーを無視します。 
  
_lpsrcinterface_が指すインターフェイス識別子は、通常、 _lpsrcinterface_が指すインターフェイス識別子と同じです。 
  
_lpdestinterface_で受け入れ可能なインターフェイス識別子が渡され、 _lpdestinterface_に無効なポインターが渡された場合、結果は予測できません。 ほとんどの場合、プロバイダーが失敗する可能性があります。 
  
反対に、コピーまたは移動してはならない補足情報を認識している場合は、 _rgiidExclude_パラメーターで渡された配列で除外されるインターフェイスのインターフェイス識別子を追加します。 たとえば、メッセージをコピーするが、メッセージの添付ファイルをコピーしない場合は、 _rgiidExclude_配列に IID_IMessage を渡します。 **** _rgiidExclude_に一覧表示されているインターフェイスは無視されます。 
  
_rgiidExclude_パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したすべてのインターフェイスも除外されます。 たとえば、 [IMAPIContainer](imapicontainerimapiprop.md)インターフェイスを除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。 [imapiprop](imapipropiunknown.md)または[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から派生しているインターフェイスが多いため、これを除外しないでください。 
  
 **docopyto**は、操作全体に適用されるグローバルエラーと、個々のプロパティに適用される個々のエラーを報告します。 これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。 プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく NULL を渡すことにより、プロパティレベルでエラー報告を抑制することができます。 
  
エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。 **docopyto**が S_OK を返す場合、構造内の個々のプロパティにエラーがあるかどうかを確認します。 **docopyto**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。 代わりに、 [imapisupport:: GetLastError](imapisupport-getlasterror.md)メソッドを呼び出して詳細なエラー情報を取得します。 
  
**docopyto**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。 
  
**docopyto**呼び出しでグローバルエラーが発生した場合は、sprop問題の**配列**構造を使用または解放しないでください。 プロバイダーは、 **docopyto**によって返される**spropの配列**構造で_ulindex_メンバーを無視する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageDeliveryTime 標準プロパティ](pidtagmessagedeliverytime-canonical-property.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

