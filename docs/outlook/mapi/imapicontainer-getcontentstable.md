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
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800459"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**適用対象**: Outlook 
  
コンテナーの内容のテーブルへのポインターを返します。
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]コンテンツ テーブルを返す方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_ASSOCIATED 
  
> コンテナーの内容が関連付けられているテーブルは、標準的な内容のテーブルの代わりに返されます。 このフラグは、フォルダーでのみ使用されます。 コンテンツが関連付けられているテーブルに含まれるメッセージは、MAPI_ASSOCIATED フラグが設定されている[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドの呼び出しで作成されました。 クライアントは、フォーム、ビュー、およびその他の非表示のメッセージを取得するために通常関連付けられている内容のテーブルを使用します。 
    
ACLTABLE_FREEBUSY
  
> **PR_MEMBER_RIGHTS**で frightsFreeBusySimple と frightsFreeBusyDetailed の権限にアクセスを有効にします。
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable**が正常に完了可能性があります前にテーブルが使用可能な呼び出し元にします。 テーブルが使用できない場合は、テーブルのそれ以降の呼び出しを行うとエラーが発生します。 
    
MAPI_UNICODE 
  
> Unicode 形式で文字列データを含む列が返されるように要求します。 MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列が返されます。 
    
SHOW_SOFT_DELETES
  
> ソフトとしてマークされているアイテムの削除を示しています-は削除済みアイテムの保存に時間の段階です。
    
 _lppTable_
  
> [out]コンテンツ テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 内容のテーブルが正常に取得しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> コンテナーでは、内容がないので、内容のテーブルを提供することはできません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::GetContentsTable**メソッドは、コンテナーの内容のテーブルへのポインターを返します。 コンテンツ テーブルには、コンテナー内のオブジェクトについての概要情報が含まれています。 
  
テーブルの内容は、長い列のセットを持っています。 必須および省略可能なテーブルの列の内容の一覧は、[テーブルの内容](contents-tables.md)を参照してください。 
  
内容がないといくつかのコンテナーのことができます。 これらのコンテナーでは、 **GetContentsTable**の実装から MAPI_E_NO_SUPPORT を返します。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

コンテナーのコンテンツ テーブルをサポートする場合も、次の行う必要があります。
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のプロパティを開くには、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)のメソッドの呼び出しをサポートします。
    
- コンテナーの呼び出しへの応答として**PR_CONTAINER_CONTENTS**を返す 
    
    [IMAPIProp::GetProps](imapiprop-getprops.md)および[IMAPIProp::GetPropList](imapiprop-getproplist.md)の方法です。 
    
このメソッドをリモート トランスポート プロバイダーの実装へのポインターを返す必要があります、 [IMAPITable: IUnknown](imapitableiunknown.md) 、 **GetContentsTable**メソッドに渡される_ppTable_パラメーター内のインタ フェースです。 場合は、トランスポート プロバイダーは、既存のコンテンツ テーブルへのポインターを返すには十分です。 場合は、このメソッドが新規に作成する必要があります[IMAPITable: IUnknown](imapitableiunknown.md)オブジェクト、テーブルには、メッセージ ヘッダー (使用可能な場合)、および新しいテーブルへのポインターを返します。 [ITableData::HrGetView](itabledata-hrgetview.md)メソッドは、戻り値を生成して、 _ppTable_パラメーターでテーブルのポインターを格納するに便利です。 内容のテーブルは、少なくとも次のプロパティの列をサポートする必要があります。 
  
- **PR_ENTRYID**([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))
    
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

文字列とバイナリの内容のテーブルの列を切り捨てることができます。 通常、プロバイダーは、255 文字を返します。 テーブルには、切り捨てられた列が含まれて かどうか、あらかじめ知ることはできません、ため、列の長さが 255 であるか、510 バイトである場合、列が切り捨てられることを想定しています。 常にから取得できます、切り捨てられた列の最大の価値に応じて、直接オブジェクトを開くには、そのエントリの識別子を使用して、 **IMAPIProp::GetProps**メソッドを呼び出すことによって。 
  
プロバイダーの実装の制限や並べ替え操作によっては、文字列のすべてまたはその文字列の切り捨てられたバージョンを適用できます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |**CContentsTableDlg**クラスでは、 **GetContentsTable**を使用して、コンテンツ テーブル内のエントリを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

