---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349288"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの contents テーブルへのポインターを返します。
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番コンテンツテーブルがどのように返されるかを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_ASSOCIATED 
  
> コンテナーの関連する contents テーブルは、標準の contents テーブルの代わりに返される必要があります。 このフラグは、フォルダーでのみ使用されます。 MAPI_ASSOCIATED フラグが[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドの呼び出しで設定された状態で、関連付けられたコンテンツテーブルに含まれているメッセージが作成されました。 通常、クライアントは関連付けられた contents テーブルを使用して、フォーム、ビュー、およびその他の非表示のメッセージを取得します。 
    
ACLTABLE_FREEBUSY
  
> **PR_MEMBER_RIGHTS**の frightsFreeBusySimple および frightsFreeBusyDetailed 権限へのアクセスを有効にします。
    
MAPI_DEFERRED_ERRORS 
  
> **getcontentstable**は、呼び出し元がテーブルを使用できるようになる前に、正常に返すことができます。 テーブルが使用できない場合は、次のテーブル呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 文字列データを含む列が Unicode 形式で返されるように要求します。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式で返されます。 
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムの保存期間の段階にあるとマークされているアイテムを表示します。
    
 _lpptable_
  
> 読み上げcontents テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> コンテンツテーブルが正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_NO_SUPPORT 
  
> コンテナーには内容が含まれていないため、目次表を提供することはできません。
    
## <a name="remarks"></a>解説

**IMAPIContainer:: getcontentstable**メソッドは、コンテナーの contents テーブルへのポインターを返します。 contents テーブルには、コンテナー内のオブジェクトに関する概要情報が含まれています。 
  
目次テーブルに長い列セットがあります。 目次表の必須およびオプションの列の完全な一覧については、「 [contents tables](contents-tables.md)」を参照してください。 
  
一部のコンテナーには内容が含まれていない可能性があります。 これらのコンテナーは、 **getcontentstable**の実装から MAPI_E_NO_SUPPORT を返します。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

コンテナーの contents テーブルをサポートしている場合は、次の操作も実行する必要があります。
  
- コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドへの呼び出しをサポートして、 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを開きます。
    
- コンテナーの呼び出しに対する応答として**PR_CONTAINER_CONTENTS**を返します。 
    
    [imapiprop:: GetProps](imapiprop-getprops.md)および[imapiprop:: getproplist](imapiprop-getproplist.md)メソッド。 
    
リモートトランスポートプロバイダーのこのメソッドの実装では、 **getcontentstable**メソッドに渡された_pptable_パラメーターの[IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスへのポインターを返す必要があります。 トランスポートプロバイダーに既存のコンテンツテーブルがある場合は、そのテーブルへのポインターを返すだけで十分です。 含まれていない場合、このメソッドは新しい[IMAPITable: IUnknown](imapitableiunknown.md)オブジェクトを作成し、メッセージヘッダーを (使用可能な場合は) テーブルに設定して、新しいテーブルへのポインターを返します。 [itabledata:: hrgetview](itabledata-hrgetview.md)メソッドは、戻り値を生成し、テーブルポインターを_pptable_パラメーターに格納するのに便利です。 contents テーブルは、少なくとも次のプロパティ列をサポートしている必要があります。 
  
- **PR_ENTRYID**([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH**([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>呼び出し側への注意

文字列およびバイナリコンテンツの表の列を切り捨てられます。 通常、プロバイダーは255文字を返します。 テーブルに切り捨てられた列が含まれているかどうかを事前に知ることはできないため、列の長さが255または510バイトの場合は、列が切り捨てられていると仮定します。 必要に応じて、エントリ id を使用して、切り捨てられた列の完全な値をオブジェクトから直接取得して、 **imapiprop:: GetProps**メソッドを呼び出すことができます。 
  
プロバイダーの実装に応じて、制限および並べ替え操作は、すべての文字列またはその文字列の切り捨てられたバージョンに適用できます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableDialog  <br/> |CContentsTableDlg:: CContentsTableDlg  <br/> |**CContentsTableDlg**クラスは、 **getcontentstable**を使用して、contents テーブル内のエントリを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

