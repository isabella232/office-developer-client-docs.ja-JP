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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405584"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの 1 つ以上のプロパティを別のオブジェクトにコピーまたは移動します。
  
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
  
> [in]コピーまたは移動するプロパティを持つオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcObj_
  
> [in]コピーまたは移動するプロパティを含むオブジェクトへのポインター。
    
 _lpIncludeProps_
  
> [in]コピーまたは移動するプロパティを示すプロパティ タグのカウントされた配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 _lpIncludeProps_ パラメーターを NULL にすることはできません。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。
    
 _lpProgress_
  
> [in]進行状況インジケーターの実装へのポインター。 _lpProgress_ パラメーターで NULL が渡された場合、MAPI 実装を使用して進行状況インジケーターが表示されます。 _lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpDestInterface_
  
> [in]オブジェクトにアクセスして、コピーまたは移動されるプロパティを受け取るインターフェイスを表すインターフェイス識別子へのポインター。
    
 _lpDestObj_
  
> [in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。
    
MAPI_MOVE 
  
> **DoCopyProps は、** コピー操作の代わりに移動操作を実行する必要があります。 このフラグを設定しない場合 **、DoCopyProps は** コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 移動先オブジェクト内の既存のプロパティは上書きしないでください。 このフラグを設定しない場合 **、DoCopyProps は既存** のプロパティを上書きします。 
    
 _lppProblems_
  
> [in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報を必要としない NULL を指定します。 _lppProblems が_ 入力の有効なポインターである場合 **、DoCopyProps** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> コピーまたは移動するプロパティは、コピー先オブジェクトに既に存在し、MAPI_NOREPLACEフラグが設定されます。 
    
MAPI_E_FOLDER_CYCLE 
  
> ソース オブジェクトには、直接または間接的に移動先オブジェクトが含まれる。 この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpSrcInterface_ パラメーターで識別されるインターフェイスは、ソース オブジェクトでサポートされていないか _、lpDestInterface_ パラメーターで識別されるインターフェイスは、移動先オブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。 このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。
    
次の値は **、SPropProblemArray** 構造体で返されますが **、DoCopyProps の戻り値として返す値として返す必要があります**。 これらのエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され **、DoCopyProps** が Unicode をサポートしていないか、または MAPI_UNICODEが設定されていないと **DoCopyProps** は Unicode のみをサポートします。 
    
MAPI_E_COMPUTED 
  
> プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの種類は、呼び出し元が期待する型ではありません。
    
## <a name="remarks"></a>注釈

**IMAPISupport::D oCopyProps** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは **、DoCopyProps** を呼び出して、フォルダーとメッセージの [IMAPIProp::CopyProps](imapiprop-copyprops.md) メソッドを実装できます。 **DoCopyProps** は  _、lpIncludeProps_ が指すプロパティ タグ配列で識別され  _、lpSrcObj_ が指すオブジェクトに存在するプロパティをコピーまたは移動します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

2 つのメッセージなど、同じ種類のオブジェクト間でプロパティをコピーする場合  _、lpSrcInterface_ パラメーターと  _lpDestInterface_ パラメーターには同じインターフェイス識別子が含まれている必要があります。  _また、lpSrcObj_ パラメーターと  _lpDestObj_ パラメーターは、同じ種類のオブジェクトを指している必要があります。 _lpDestInterface が_ NULL に設定されている場合 **、DoCopyProps は** 値をMAPI_E_INVALID_PARAMETER。 _lpDestInterface_ を許容可能なインターフェイス識別子に設定し _、lpDestObj_ を無効なポインターに設定すると、結果は予測できません。 ほとんどの場合、プロバイダーは失敗します。 
  
宛先オブジェクトMAPI_NOREPLACEプロパティを上書きしない場合は、このフラグを設定します。 ソース オブジェクトに存在し、上書きされないコピー先オブジェクトのプロパティは削除または変更されません。
  
メッセージの受信者リストをコピーするには _、lpIncludeProps_ パラメーターが指すプロパティ タグ配列に **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを含める必要があります。 メッセージの添付ファイルをコピーするには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含める必要があります。 
  
フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルをコピーするには、プロパティ タグ配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含める必要があります。 フォルダーに関連付けられているコンテンツ テーブルを含めるには、配列に PR_FOLDER_ASSOCIATED_CONTENTS **(** [PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを含める必要があります。
  
サブフォルダーがコピーまたは移動された場合 **、SPropTagArray** 構造で示されるプロパティの使用に関係なく、その内容はコピーまたは移動されます。 
  
 **DoCopyProps は** 、操作全体で発生するグローバル エラーと、1 つ以上のプロパティで発生する個々のエラーを報告します。 これらの個々のエラーは **、SPropProblemArray 構造体に入** れ込まれています。 プロパティの問題配列構造パラメーターに対して、有効なポインターではなく NULL を渡して、プロパティ レベルでエラー報告を抑制できます。 
  
エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。 **DoCopyProps は**、S_OKを返す場合は、構造体内の個々のプロパティで発生する可能性のあるエラーを確認します。 **DoCopyProps が** エラーを返す場合 **、SPropProblemArray** 構造体に情報は返されません。 代わりに [、IMAPISupport::GetLastError](imapisupport-getlasterror.md) メソッドを呼び出して、詳細なエラー情報を取得します。 
  
**DoCopyProps が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。 
  
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

