---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eef2fef85e40340aa15dd3dc5a4ec2b4e1ac6d8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575877"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
選択したプロパティをコピーまたは移動します。 
  
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
  
> [in]コピーまたは移動するプロパティを指定するプロパティ タグ配列へのポインター。 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) を配列に含めません。 _lpIncludeProps_ パラメーターを null に **することはできません**。
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpProgress_
  
> [in]進行状況インジケーターの実装へのポインター。 _lpProgress_ パラメーターで null が渡された場合、MAPI 実装を使用して進行状況インジケーターが表示されます。  _lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpInterface_
  
> [in]  _lpDestObj_ パラメーターが指すオブジェクトにアクセスするために使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lpInterface パラメーター_ は null に **することはできません**。
    
 _lpDestObj_
  
> [in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DECLINE_OK 
  
> **CopyProps** が [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、代わりにエラー値 MAPI_E_DECLINE_COPY を使用して直ちに返す必要があります。 再MAPI_DECLINE_OKを制限するために、MAPI によってこのフラグが設定されます。 クライアントは、このフラグを設定しません。 
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。
    
MAPI_MOVE 
  
> **CopyProps は** 、コピー操作の代わりに移動操作を実行する必要があります。 このフラグを設定しない場合 **、CopyProps は** コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 移動先オブジェクト内の既存のプロパティは上書きしないでください。 このフラグを設定しない場合 **、CopyProps は既存** のプロパティを上書きします。 
    
 _lppProblems_
  
> [in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の **場合は、エラー** 情報が不要であることを示す null。 _lppProblems が_ 入力の有効なポインターである場合 **、CopyProps** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで定義されている同じ表示名を持つサブオブジェクトが、コピー先オブジェクトに既に存在している場合、サブオブジェクトをコピーできません。 
    
MAPI_E_DECLINE_COPY 
  
> サービス プロバイダーは、コピー操作を実装しない。
    
MAPI_E_FOLDER_CYCLE 
  
> コピーまたは移動操作を直接または間接的に実行するソース オブジェクトには、移動先オブジェクトが含まれる。 この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpInterface_ パラメーターで識別されるインターフェイスは、移動先オブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。 このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。
    
次の値は **、SPropProblemArray** 構造体で返されますが、CopyProps の戻り値として **返す値として返す必要があります**。 これらのエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され **、CopyProps** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **CopyProps** は Unicode のみをサポートします。 
    
MAPI_E_COMPUTED 
  
> プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの種類は、呼び出し元が予期する型ではありません。
    
## <a name="remarks"></a>注釈

**IMAPIProp::CopyProps** メソッドは、選択したプロパティを現在のオブジェクトから移動先オブジェクトにコピーまたは移動します。 **CopyProps は** 主に、元のメッセージのプロパティの一部だけが返信または転送されたコピーと一緒に移動するメッセージへの返信と転送に使用されます。 
  
[SPropTagArray](sproptagarray.md)構造体で示されるプロパティの使用に関係なく、ソース オブジェクト内のサブオブジェクトは自動的に操作に含まれてコピーまたは移動されます。 既定では **、CopyProps は** 、ソース オブジェクトのプロパティに一致するコピー先オブジェクトのプロパティを上書きします。 コピーまたは移動されたプロパティがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが  _ulFlags_ パラメーターに設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。 上書きされない移動先オブジェクト内の既存の情報はそのまま残ります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**CopyProps** の完全な実装を提供するか、MAPI がサポート オブジェクトで提供する実装に依存できます。 MAPI 実装を使用する場合は **、IMAPISupport::D oCopyProps メソッドを呼び出** します。 ただし **、DoCopyProps** に処理を委任し、MAPI_DECLINE_OK フラグを渡した場合は、サポート呼び出しを回避し、代わりにMAPI_E_DECLINE_COPY返します。 フォルダーをコピーするときに発生する可能性のある再帰を回避するために、MAPI によってこのフラグを使用して呼び出されます。 
  
コピー操作は長い場合がありますから、進行状況インジケーターを表示する必要があります。 [lpProgress パラメーター](imapiprogressiunknown.md)に渡される _IMAPIProgress 実装_(ある場合) を使用します。 _lpProgress が_ **null** の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出して MAPI 実装を使用します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

このフラグを設定MAPI_DECLINE_OKしない。これは、メッセージ ストア プロバイダー **CopyProps** 実装への呼び出しで MAPI によって使用されます。 
  
コピー操作と移動操作には時間がかかる場合があります。このフラグを設定して進行状況インジケーターの表示を要求MAPI_DIALOGです。 _lpProgress パラメーター_ を **IMAPIProgress** の実装 (ある場合)、または null に設定 **できます**。 _lpProgress が_ null の **場合****、CopyProps は MAPI** によって提供される既定の進行状況インジケーターを使用します。 
  
進行状況インジケーターの表示を抑制するには、進行状況フラグを設定MAPI_DIALOGできます。 **CopyProps は**  _ulUIParam_ パラメーターと  _lpProgress_ パラメーターを無視し、インジケーターの表示を回避します。 
  
 **CopyProps は** 、グローバル および個々のエラー、または 1 つ以上のプロパティで発生するエラーを報告できます。 これらの個々のエラーは **、SPropProblemArray 構造体に入** れ込まれています。 プロパティの問題配列構造パラメーターに対して、有効なポインターではなく **null** を渡して、プロパティ レベルでのエラー報告を抑制できます。 
  
エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。 **CopyProps が** プロパティを返S_OK、構造内の個々のプロパティで発生する可能性のあるエラーを確認します。 **CopyProps がエラー** を返す場合 **、SPropProblemArray 構造体には情報は返** されません。 代わりに [、IMAPIProp::GetLastError](imapiprop-getlasterror.md) メソッドを呼び出して、詳細なエラー情報を取得します。 
  
**CopyProps が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。 
  
ソース オブジェクトの種類に固有のプロパティをコピーする場合は、コピー先のオブジェクトが同じ型である必要があります。 **CopyProps** では、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けできない場合があります。 コピー先オブジェクトに合ったプロパティをコピーする必要があります。 たとえば、メッセージ のプロパティをアドレス帳コンテナーにコピーする必要があります。 
  
同じ型のオブジェクト間でコピーを行う場合は、オブジェクト ポインターを比較するか [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) メソッドを呼び出して、ソース オブジェクトとコピー先オブジェクトが同じ型である必要があります。 _lpInterface_ が指すインターフェイス識別子を、ソース オブジェクトの標準インターフェイスに設定します。 また、オブジェクトの種類またはプロパティ [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)PR_OBJECT_TYPE **プロパティが** 2 つのオブジェクトで同じであることを確認します。 たとえば、メッセージからコピーする場合は _、lpInterface_ を IID_IMessage に設定し、PR_OBJECT_TYPE両方のオブジェクトのMAPI_MESSAGE。 
  
_lpDestObj_ パラメーターに無効なポインターが渡された場合、結果は予測できません。 
  
メッセージの受信者リストをコピーするには、メッセージの **CopyProps** メソッドを呼び出し **、PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティをプロパティ タグ配列に含める必要があります。 メッセージの添付ファイルをコピーするには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含める必要があります。 
  
フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルをコピーするには、プロパティ タグ配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) プロパティまたは **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを含める必要があります。 フォルダーに関連付けられているコンテンツ テーブルを含めるには、配列に PR_FOLDER_ASSOCIATED_CONTENTS **(** [PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを含める必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI は **IMAPIProp::CopyProps** メソッドを使用して、名前付きプロパティをメッセージ間でコピーします。  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI は **IMAPIProp::CopyProps** メソッドを使用して、別のオブジェクトからコピーされたプロパティを貼り付けます。  <br/> |
   
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

