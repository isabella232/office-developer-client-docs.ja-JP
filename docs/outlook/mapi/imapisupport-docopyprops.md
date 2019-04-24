---
title: imapisupportdocopyprops
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322366"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの1つまたは複数のプロパティを別のオブジェクトにコピーまたは移動します。
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
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
  
> 順番コピーまたは移動するプロパティを含むオブジェクトへのポインターを指定します。
    
 _lpincludeprops_
  
> 順番コピーまたは移動するプロパティを示す、カウントされたプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _lpincludeprops_パラメーターを NULL にすることはできません。 
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。
    
 _lpprogress_
  
> 順番進行状況インジケーターの実装へのポインター。 _lpprogress_パラメーターで NULL が渡された場合は、MAPI 実装を使用して進行状況インジケーターが表示されます。 MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。 
    
 _lpdestinterface_
  
> 順番コピーまたは移動されるプロパティを受け取るためのオブジェクトへのアクセスに使用されるインターフェイスを表すインターフェイス識別子へのポインター。
    
 _lpdestobj_
  
> 順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> 順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。
    
MAPI_MOVE 
  
> **docopyprops**は、コピー操作ではなく、移動操作を実行する必要があります。 このフラグが設定されていない場合、 **docopyprops**はコピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。 このフラグが設定されていない場合、 **docopyprops**は既存のプロパティを上書きします。 
    
 _lppproblems 問題_
  
> [入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は、エラー情報を必要としないことを示す NULL。 _lppproblems_が入力の有効なポインターである場合、 **docopyprops**は、1つ以上のプロパティをコピーする際のエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> コピーまたは移動されるプロパティは、対象オブジェクトに既に存在し、MAPI_NOREPLACE フラグが設定されています。 
    
MAPI_E_FOLDER_CYCLE 
  
> source オブジェクトは、直接または間接的に対象のオブジェクトを含みます。 この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpsrcinterface_パラメーターによって識別されるインターフェイスは、source オブジェクトではサポートされていません。また、 _lpsrcinterface_パラメーターで指定されたインターフェイスは、destination オブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。 destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。
    
次の値は、 **spropの配列**構造で返すことができますが、 **docopyprops**の戻り値としては返されません。 これらのエラーは、1つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されており、 **docopyprops**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **docopyprops**が unicode のみをサポートしています。 
    
MAPI_E_COMPUTED 
  
> このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型が、呼び出し元が想定している型ではありません。
    
## <a name="remarks"></a>解説

**imapisupport::D ocopyprops**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは、 **docopyprops**を呼び出して、フォルダーとメッセージに[imapiprop:: copyprops](imapiprop-copyprops.md)メソッドを実装できます。 **docopyprops**は、 _lpincludeprops_が指すプロパティタグ配列で指定されているプロパティをコピーまたは移動します。これは、 _lpsrcobj_が指すオブジェクトに存在します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

2つのメッセージなど、同じ種類のオブジェクト間でプロパティをコピーする場合、 _lpsrcinterface_パラメーターと_lpsrcinterface_パラメーターには同じインターフェイス識別子を含める必要があります。 _lpsrcobj_パラメーターと lpsrcinterface パラメーターは同じである必要があります。 __ 同じ種類のオブジェクトをポイントする必要があります。 _lpdestinterface_が NULL に設定されている場合、 **docopyprops**は MAPI_E_INVALID_PARAMETER を返します。 _lpdestinterface_を受け入れ可能なインターフェイス識別子に設定しても、 _lpdestinterface_を無効なポインターに設定した場合、結果は予測できません。 多くの場合、プロバイダーは失敗します。 
  
変換先オブジェクトのプロパティを上書きする必要がない場合は、MAPI_NOREPLACE フラグを設定します。 コピー元のオブジェクトに存在し、上書きされていない対象のオブジェクトのプロパティは、削除または変更されません。
  
メッセージの宛先リストをコピーするには、 _lpincludeprops_パラメーターで指定されたプロパティタグ配列に**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを含めます。 メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含めます。 
  
フォルダーまたはアドレス帳コンテナーの階層またはコンテンツテーブルをコピーするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) をプロパティタグ配列に含めます。 フォルダーに関連付けられたコンテンツテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを配列に含めます。
  
サブフォルダーをコピーまたは移動すると、 **SPropTagArray**構造で指定されているプロパティの使用に関係なく、その内容がコピーまたは移動されます。 
  
 **docopyprops**は、操作が全体として発生するグローバルエラーと、1つ以上のプロパティで発生する個々のエラーを報告します。 これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。 プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく NULL を渡すことにより、プロパティレベルでエラー報告を抑制することができます。 
  
エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。 **docopyprops**が S_OK を返す場合、構造内の各プロパティにエラーがあるかどうかを確認します。 **docopyprops**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。 代わりに、 [imapisupport:: GetLastError](imapisupport-getlasterror.md)メソッドを呼び出して詳細なエラー情報を取得します。 
  
**docopyprops**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagFolderAssociatedContents 標準プロパティ](pidtagfolderassociatedcontents-canonical-property.md)
  
[PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

