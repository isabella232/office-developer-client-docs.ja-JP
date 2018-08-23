---
title: IMAPISupportDoCopyProps
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800732"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**適用対象**: Outlook 
  
オブジェクトの 1 つまたは複数のプロパティを別のオブジェクトを移動またはコピーします。
  
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

 _lpSrcInterface_
  
> [in]コピーまたは移動するプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcObj_
  
> [in]コピーまたは移動するにはプロパティを格納しているオブジェクトへのポインター。
    
 _lpIncludeProps_
  
> [in]コピーまたは移動するにはプロパティを指定するプロパティ タグのカウント済み配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _LpIncludeProps_パラメーターは、NULL にすることはできません。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。
    
 _lpProgress_
  
> [in]進行状況のインジケーターの実装へのポインター。 _LpProgress_パラメーターに NULL が渡されると、MAPI 実装を使用して進行状況のインジケーターが表示されます。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。 
    
 _lpDestInterface_
  
> [in]プロパティをコピーまたは移動を受信するオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子へのポインター。
    
 _lpDestObj_
  
> [in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作の実行方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> 進行状況のインジケーターが表示されます。
    
MAPI_MOVE 
  
> **DoCopyProps**は、コピー操作ではなく移動操作を実行する必要があります。 このフラグが設定されていない場合、 **DoCopyProps**は、コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> コピー先オブジェクトの既存のプロパティを上書きしてはなりません。 このフラグが設定されていない場合、 **DoCopyProps**には、既存のプロパティが上書きされます。 
    
 _lppProblems_
  
> [で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL、エラー情報の必要性を示すしません。 _LppProblems_が入力時に有効なポインターである場合は、 **DoCopyProps**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティは、コピーまたは移動されて正常にします。
    
MAPI_E_COLLISION 
  
> 先のオブジェクトのプロパティをコピーまたは移動を既にが存在して MAPI_NOREPLACE フラグを設定します。 
    
MAPI_E_FOLDER_CYCLE 
  
> ソース オブジェクトには直接または間接的に目的のオブジェクトが含まれています。 重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> ソース オブジェクトでは、 _lpSrcInterface_パラメーターで指定されたインターフェイスはサポートされていないか、先のオブジェクトでは、 _lpDestInterface_パラメーターで指定されたインターフェイスはサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。 目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。
    
次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**DoCopyProps**。 これらのエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された**DoCopyProps**は、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**DoCopyProps**は、Unicode だけをサポートしています。 
    
MAPI_E_COMPUTED 
  
> コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。 このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの型が正しくありません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元が要求する型ではありません。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::DoCopyProps**メソッドを実装します。 メッセージ ストア プロバイダーは、そのフォルダーとメッセージの[IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドを実装するために**DoCopyProps**を呼び出すことができます。 **DoCopyProps**にコピーまたは移動のプロパティで_lpIncludeProps_で指定されたプロパティ タグ配列を識別し、 _lpSrcObj_が指すオブジェクトに存在します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LpSrcInterface_および_lpDestInterface_パラメーターが同じインターフェイス識別子、および、 _lpSrcObj_および_lpDestObj_パラメーターを含める必要があります、2 つのメッセージなど、同じ種類のオブジェクト間でプロパティをコピーすると、同じ種類のオブジェクトをポイントする必要があります。 _LpDestInterface_は、NULL に設定されている場合、 **DoCopyProps**は MAPI_E_INVALID_PARAMETER を返します。 許容可能なインタ フェース識別子は無効なポインターをセット_lpDestObj_に_lpDestInterface_を設定した場合、結果は予測できません。 ほとんどの場合、プロバイダーは失敗します。 
  
上書き先のオブジェクトのプロパティのいずれかしない場合は、MAPI_NOREPLACE フラグを設定します。 ソース オブジェクト内に存在し、上書きされないプロパティを目的のオブジェクトには、削除したり、変更するはありません。
  
メッセージの受信者のリストをコピーするのには、 _lpIncludeProps_パラメーターで指定されたプロパティ タグ配列の**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティが含まれます。 メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティが含まれます。 
  
フォルダーまたはアドレス帳コンテナーの階層構造または内容のテーブルをコピーするには、プロパティ タグ配列の**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含めます。 フォルダーの内容を関連するテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) のプロパティを配列に指定します。
  
サブフォルダーは、コピーまたは移動は場合、その内容がコピーまたは、 **SPropTagArray**構造体で示されているプロパティの使用に関係なく、完全に移動します。 
  
 **DoCopyProps**は、グローバル エラーの全体としての操作で発生して、プロパティのいずれかで発生する個々 のエラーを報告します。 これらの個々 のエラーは、 **SPropProblemArray**構造体に配置されます。 プロパティ問題配列構造体パラメーターに有効なポインターではなく NULL を渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。 
  
エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。 **DoCopyProps**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。 **DoCopyProps**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。 代わりに、詳細なエラー情報を取得するために[IMAPISupport::GetLastError](imapisupport-getlasterror.md)メソッドを呼び出します。 
  
**DoCopyProps**では、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。 
  
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

