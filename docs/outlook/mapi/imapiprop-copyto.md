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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356393"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の除外プロパティを除くすべてのプロパティをコピーまたは移動します。
  
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
  
> [in]プロパティをコピーまたは移動するときに除外するインターフェイスの数。
    
 _rgiidExclude_
  
> [in]補足情報をコピーまたは移動先オブジェクトに移動するときに使用しないインターフェイスを指定するインターフェイス識別子 (IID) の配列。
    
 _lpExcludeProps_
  
> [in]コピーまたは移動操作から除外する必要があるプロパティ タグを識別するプロパティ タグ配列へのポインター。 _lpExcludeProps_ パラメーターに null を渡す場合は、オブジェクトのすべてのプロパティをコピーまたは移動する必要があります。  **CopyTo** は _、lpExcludeProps_ MAPI_E_INVALID_PARAMETER示す [SPropProblemArray](spropproblemarray.md)構造体の **cValues** メンバーが 0 に設定されている場合に、この値を返します。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpProgress_
  
> [in]進行状況インジケーターの実装へのポインター。 _lpProgress_ パラメーターで null が渡された場合、MAPI は進行状況の実装を提供します。  _lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpInterface_
  
> [in]  _lpDestObj_ パラメーターが指すオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lpInterface パラメーター_ は null に **することはできません**。
    
 _lpDestObj_
  
> [in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DECLINE_OK 
  
> **CopyTo が** [IMAPISupport::D oCopyTo](imapisupport-docopyto.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、代わりにエラー値 MAPI_E_DECLINE_COPY を使用して直ちに返す必要があります。 再MAPI_DECLINE_OKを制限するために、MAPI によってこのフラグが設定されます。 クライアントは、このフラグを設定しません。 
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。
    
MAPI_MOVE 
  
> **CopyTo** は、コピー操作の代わりに移動操作を実行する必要があります。 このフラグが設定されていない場合 **、CopyTo は** コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 移動先オブジェクト内の既存のプロパティは上書きしないでください。 このフラグを設定しない場合 **、CopyTo は** 既存のプロパティを上書きします。 
    
 _lppProblems_
  
> [in, out]入力時に **、SPropProblemArray** 構造体へのポインターを指すポインター。それ以外の場合 **は null**、エラー情報は不要であることを示します。 _lppProblems が_ 入力の有効なポインターである場合 **、CopyTo** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで指定された同じ表示名を持つサブオブジェクトが、コピー先オブジェクトに既に存在する場合、サブオブジェクトをコピーできません。 
    
MAPI_E_DECLINE_COPY 
  
> サービス プロバイダーは、コピー操作を実装しない。
    
MAPI_E_FOLDER_CYCLE 
  
> コピーまたは移動操作を直接または間接的に実行するソース オブジェクトには、移動先オブジェクトが含まれる。 この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpInterface_ パラメーターで識別されるインターフェイスは、移動先オブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。 このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。
    
次の値は **、SPropProblemArray** 構造体で返されますが、CopyTo の戻り値として **返す値として返す必要があります**。 次のエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され **、CopyTo** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **CopyTo** は Unicode のみをサポートします。 
    
MAPI_E_COMPUTED 
  
> プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの種類は、呼び出し元が予期する型ではありません。
    
## <a name="remarks"></a>注釈

既定では **、IMAPIProp::CopyTo** メソッドは、現在のオブジェクトのすべてのプロパティをコピーまたは移動先オブジェクトに移動します。 **CopyTo** は、オブジェクトを正確にコピーまたは移動する必要がある場合に使用され、そのプロパティのすべてまたは大部分はそのまま使用されます。 
  
ソース オブジェクト内のサブオブジェクトは、自動的に操作に含まれてコピーまたは移動されます。 既定では **、CopyTo** は、ソース オブジェクトのプロパティに一致するコピー先オブジェクトのプロパティを上書きします。 コピーまたは移動されたプロパティがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが  _ulFlags_ パラメーターに設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。 上書きされない移動先オブジェクト内の既存の情報はそのまま残ります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

CopyTo の完全な実装を提供するか **、MAPI** がサポート オブジェクトで提供する実装に依存できます。 MAPI 実装を使用する場合は **、IMAPISupport::D oCopyTo を呼び出します**。 ただし **、DoCopyTo** に処理を委任し、MAPI_DECLINE_OK フラグが渡された場合は、サポート呼び出しを回避し、代わりにMAPI_E_DECLINE_COPY返します。 MAPI は、フォルダーをコピーするときに発生する可能性のある再帰を回避するために、このフラグを使用して呼び出します。 
  
コピー操作は長い場合がありますから、進行状況インジケーターを表示する必要があります。 [lpProgress パラメーター](imapiprogressiunknown.md)に渡される _IMAPIProgress 実装_ がある場合は、その実装を使用します。 _lpProgress が_ **null** の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出して MAPI 実装を使用します。 
  
宛先オブジェクトで既知の読み取り専用プロパティを設定しようとはしない。代わりにMAPI_E_NO_ACCESSを返します。
  
ソース オブジェクトと移動先オブジェクトは、同じインターフェイスを使用する必要があります。 _lpInterface MAPI_E_INVALID_PARAMETER設定されていない場合は、この値_ を返します。 
  
既知MAPI_E_INTERFACE_NOT_SUPPORTEDが除外されている場合は、この値を返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

このフラグを設定MAPI_DECLINE_OKしない。MAPI は、メッセージ ストア プロバイダーの CopyTo 実装への **呼び出しで** 使用します。 
  
コピー操作と移動操作には時間がかかる場合があります。このフラグを設定して進行状況インジケーターの表示をMAPI_DIALOGがあります。 _lpProgress パラメーター_ を **IMAPIProgress** の実装 (ある場合)、または null に設定 **できます**。 _lpProgress が_ null の **場合****、CopyTo は MAPI** が提供する既定の進行状況インジケーターを使用します。 
  
進行状況インジケーターの表示を抑制するには、進行状況フラグを設定MAPI_DIALOGできます。 **CopyTo** は  _ulUIParam パラメーター_ と  _lpProgress_ パラメーターを無視し、インジケーターは表示されません。 
  
 **CopyTo** は、グローバルおよび個々のエラー、または 1 つ以上のプロパティで発生するエラーを報告できます。 これらの個々のエラーは **、SPropProblemArray 構造体に配置** されます。 プロパティの問題配列構造パラメーターに対して、有効なポインターではなく **null** を渡して、プロパティ レベルでのエラー報告を抑制できます。 
  
エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。 **CopyTo が** プロパティを返S_OK、構造内の個々のプロパティで発生する可能性のあるエラーを確認します。 **CopyTo が** エラーを返す場合 **、SPropProblemArray** 構造体に情報は返されません。 代わりに [、IMAPIProp::GetLastError](imapiprop-getlasterror.md) を呼び出して、詳細なエラー情報を取得します。 
  
**CopyTo が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。 
  
ソース オブジェクトの種類に固有のプロパティをコピーする場合は、コピー先オブジェクトの種類が同じことを確認する必要があります。 **CopyTo** を使用しても、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けることができます。 コピー先オブジェクトに合ったプロパティをコピーする必要があります。 たとえば、メッセージ のプロパティをアドレス帳コンテナーにコピーする必要があります。 
  
同じ型のオブジェクト間でコピーを行う場合は、オブジェクト ポインターを比較するか [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出すことによって、ソース オブジェクトと移動先オブジェクトが同じ型である必要があります。 _lpInterface_ が指すインターフェイス識別子を、ソース オブジェクトの標準インターフェイスに設定します。 また、オブジェクトの種類またはプロパティ [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)PR_OBJECT_TYPE **プロパティが** 2 つのオブジェクトで同じであることを確認します。 たとえば、メッセージからコピーする場合は _、lpInterface_ を [IID_IMessage] に設定しPR_OBJECT_TYPE両方のオブジェクトMAPI_MESSAGE。 
  
_lpDestObj_ パラメーターに無効なポインターが渡された場合、結果は予測できません。 
  
CopyTo 呼び出し **のプロパティを** 除外すると便利です。 たとえば、一部のオブジェクトには、メッセージ配信の日時など、オブジェクトの 1 つのインスタンスに固有のプロパティがあります。 メッセージを別のフォルダーにコピーするときにメッセージの配信時間をコピーしないようにするには、プロパティ タグ exclude 配列に **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。 メッセージの受信者リストを除外するには、PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。 メッセージの添付ファイルを除外するには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。
  
同様に、プロパティ タグの除外配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含めて、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルのコピーまたは移動を防止します。
  
コピーまたは移動操作からプロパティを除外するには、プロパティ タグを  _lpExcludeProps パラメーターに含_ める必要があります。 PROP_TAG マクロ **の結果** を渡して、プロパティ タグ配列内の特定の識別子からプロパティ タグを作成すると、その識別子を持つすべてのプロパティが除外されます。 たとえば、プロパティ タグ配列の次のエントリでは、型に関係なく、識別子を持つすべてのプロパティ0x8002除外されます。 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
プロパティ **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティ タグは  _、lpExcludeProps 配列に含_ めません。 
  
インターフェイスを除外する **CopyTo** 機能の使い方は、プロパティを除外する場合の便利さほど明らかではありません。 プロパティのグループに関する知識がないオブジェクトにコピーする場合は、インターフェイスを除外できます。 たとえば、フォルダーから添付ファイルにプロパティをコピーする場合、添付ファイルで使用できるプロパティは [、IMAPIProp](imapipropiunknown.md) 実装で使用できる汎用プロパティのみです。 [IMAPIFolder をコピー](imapifolderimapicontainer.md)操作から除外すると、添付ファイルは、より具体的なフォルダー プロパティを受け取る必要がなされます。 
  
_rgiidExclude_ パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したインターフェイスもすべて除外されます。 たとえば [、IMAPIContainer を](imapicontainerimapiprop.md) 除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。 **IMAPIProp** または [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)は、多くのインターフェイスから派生しますので、除外しません。 
  
_lppProblems_ パラメーター MAPI_E_COMPUTED **SPropProblemArray** 構造体で返されるエラーを無視します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI は **IMAPIProp::CopyTo** メソッドを使用して、.msg ファイルから [IMAPIMessageSite](imapimessagesiteiunknown.md) オブジェクトにプロパティをコピーします。  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI では **、IMAPIProp::CopyTo** メソッドを使用して、貼り付け操作中にソース メッセージからターゲット メッセージにプロパティをコピーします。  <br/> |
   
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

