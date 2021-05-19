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
  
特定の除外プロパティを除く、1 つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。
  
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

 _lpSrcInterface_
  
> [in]コピーまたは移動するプロパティを持つオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcObj_
  
> [in]コピーまたは移動するプロパティを持つオブジェクトへのポインター。
    
 _ciidExclude_
  
> [in]プロパティをコピーまたは移動するときに除外するインターフェイスの数。
    
 _rgiidExclude_
  
> [in]補足情報をコピーまたは移動先オブジェクトに移動するときに使用しないインターフェイスを示すインターフェイス識別子の配列。
    
 _lpExcludeProps_
  
> [in]コピーまたは移動操作から除外する必要があるプロパティ タグを識別するプロパティ タグ配列へのポインター。 _lpExcludeProps_ パラメーターに NULL を渡す場合は、オブジェクトのすべてのプロパティをコピーまたは移動する必要があります。 **DoCopyTo** は **、lpExcludeProps** MAPI_E_INVALID_PARAMETER示す [SPropTagArray](sproptagarray.md) 構造体の  _cValues_ メンバーが 0 に設定されている場合に、この値を返します。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 
    
 _lpProgress_
  
> [in]進行状況インジケーターの実装へのポインター。 _lpProgress_ パラメーターで NULL が渡された場合、MAPI は進行状況の実装を提供します。 _lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpDestInterface_
  
> [in]コピーまたは移動されたプロパティを受け取るオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子へのポインター。
    
 _lpDestObj_
  
> [in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 進行状況インジケーターを表示します。 
    
MAPI_MOVE 
  
> **DoCopyTo は** 、コピー操作の代わりに移動操作を実行する必要があります。 このフラグが設定されていない場合 **、DoCopyTo は** コピー操作を実行します。 
    
MAPI_NOREPLACE 
  
> 移動先オブジェクト内の既存のプロパティは上書きしないでください。 このフラグを設定しない場合 **、DoCopyTo は** 既存のプロパティを上書きします。 
    
 _lppProblems_
  
> [out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報を必要としない NULL を指定します。 _lppProblems が_ 入力の有効なポインターである場合 **、DoCopyTo** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> コピーまたは移動するプロパティは、コピー先オブジェクトに既に存在し、MAPI_NOREPLACEフラグが設定されます。 
    
MAPI_E_FOLDER_CYCLE 
  
> ソース オブジェクトには、直接または間接的に移動先オブジェクトが含まれる。 この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> _lpSrcInterface_ パラメーターで識別されるインターフェイスは _、lpSrcObj_ によって指されるオブジェクトではサポートされていません。または _lpDestInterface_ パラメーターで識別されるインターフェイスは _、lpDestObj_ によって指されるオブジェクトではサポートされていません。 
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。 このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。
    
MAPI_E_INVALID_PARAMETER 
  
> _lpSrcInterface パラメーター_ は NULL です。 
    
次の値は **、SPropProblemArray** 構造体で返されますが、DoCopyTo の戻り値 **として返す値として返す必要があります**。 これらのエラーは、1 つのプロパティに適用されます。
  
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され **、DoCopyTo** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **DoCopyTo** は Unicode のみをサポートします。 
    
MAPI_E_COMPUTED 
  
> プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。 このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの種類は、呼び出し元が予期する型ではありません。
    
## <a name="remarks"></a>注釈

**IMAPISupport::D oCopyTo** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは **、DoCopyTo** を呼び出して、フォルダーとメッセージ [の IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを実装できます。 
  
既定では **、DoCopyTo は** 1 つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。 ソース オブジェクト内のサブオブジェクトは、自動的に操作に含まれてコピーまたは移動されます。 
  
コピーまたは移動されたプロパティがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが  _ulFlags_ パラメーターに設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。 上書きされない移動先オブジェクト内の既存の情報はそのまま残ります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

コピーまたは移動操作からプロパティを除外するには、プロパティ タグを  _lpExcludeProps パラメーターに含_ める必要があります。 [PROP_TAG](prop_tag.md)マクロを使用してプロパティ タグ配列内の特定の識別子からプロパティ タグを作成した結果を渡した場合、その識別子を持つすべてのプロパティは除外されます。 たとえば、プロパティ タグ配列の次のエントリでは、型に関係なく、識別子を持つすべてのプロパティ0x8002除外されます。 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
メッセージを別のフォルダーにコピーするときにメッセージの配信時間をコピーしないようにするには、プロパティ タグ exclude 配列に **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。 メッセージの受信者リストを除外するには、PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。 メッセージの添付ファイルを除外するには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。
  
同様に、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルのコピーまたは移動を防止するには、プロパティ タグの除外配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含める必要があります。
  
_lppProblems_ パラメーター MAPI_E_COMPUTED **SPropProblemArray** 構造体で返されるエラーを無視します。 
  
_lpSrcInterface_ がポイントするインターフェイス識別子は、通常 _、lpDestInterface_ がポイントするインターフェイス識別子と同じです。 
  
_lpDestInterface_ で許容可能なインターフェイス識別子を渡し _、lpDestObj_ で無効なポインターを渡した場合、結果は予測できません。 ほとんどの場合、これはプロバイダーが失敗する原因になります。 
  
逆に、コピーまたは移動しない補足情報を認識している場合は  _、rgiidExclude_ パラメーターで渡された配列で除外するインターフェイスのインターフェイス識別子を追加します。 たとえば、メッセージをコピーするが、メッセージ添付ファイルをコピーしない場合は  _、rgiidExclude_ 配列IID_IMessageを渡します。 **DoCopyTo** は  _、rgiidExclude_ で認識されないインターフェイスを無視します。 
  
_rgiidExclude_ パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したインターフェイスもすべて除外されます。 たとえば [、IMAPIContainer](imapicontainerimapiprop.md) インターフェイスを除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。 [IMAPIProp](imapipropiunknown.md)または[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)は、多くのインターフェイスから派生しますので、除外しません。 
  
 **DoCopyTo は** 、操作全体に適用されるグローバル エラーと、個々のプロパティに適用される個々のエラーを報告します。 これらの個々のエラーは **、SPropProblemArray 構造体に入** れ込まれています。 プロパティの問題配列構造パラメーターに対して、有効なポインターではなく NULL を渡して、プロパティ レベルでエラー報告を抑制できます。 
  
エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。 **DoCopyTo が** プロパティを返S_OK、構造内の個々のプロパティで発生する可能性のあるエラーを確認します。 **DoCopyTo が** エラーを返す場合 **、SPropProblemArray 構造体には情報は返** されません。 代わりに [、IMAPISupport::GetLastError](imapisupport-getlasterror.md) メソッドを呼び出して、詳細なエラー情報を取得します。 
  
**DoCopyTo が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。 
  
**DoCopyTo** 呼び出しでグローバル エラーが発生した場合は **、SPropProblemArray** 構造体を使用したり解放したりしません。 プロバイダーは  _、DoCopyTo_ によって返される **SPropProblemArray** 構造体の **ulIndex メンバーを無視する必要があります**。
  
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

