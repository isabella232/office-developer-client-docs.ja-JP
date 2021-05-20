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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431107"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーのコンテンツ テーブルへのポインターを返します。
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]コンテンツ テーブルの返し方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_ASSOCIATED 
  
> コンテナーの関連付けられたコンテンツ テーブルは、標準のコンテンツ テーブルの代わりに返す必要があります。 このフラグはフォルダーでのみ使用されます。 関連付けられたコンテンツ テーブルに含まれるメッセージは [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドの呼び出しで設定MAPI_ASSOCIATEDフラグを設定して作成されました。 クライアントは通常、関連付けられたコンテンツ テーブルを使用して、フォーム、ビュー、その他の非表示メッセージを取得します。 
    
ACLTABLE_FREEBUSY
  
> frightsFreeBusySimple および frightsFreeBusyDetailed 権限へのアクセス **を** 有効PR_MEMBER_RIGHTS。
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable は** 、呼び出し元がテーブルを使用できる前に、正常に返すことができます。 テーブルが使用できない場合は、後続のテーブル呼び出しでエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 文字列データを含む列を Unicode 形式で返す要求。 このフラグMAPI_UNICODE設定しない場合は、ANSI 形式で文字列を返す必要があります。 
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムとしてマークされているアイテム、つまり削除済みアイテムの保持時間フェーズにあるアイテムを表示します。
    
 _lppTable_
  
> [out]目次テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> コンテンツ テーブルが正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> コンテナーにはコンテンツが含め、コンテンツ テーブルを提供できません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::GetContentsTable** メソッドは、コンテナーのコンテンツ テーブルへのポインターを返します。 コンテンツ テーブルには、コンテナー内のオブジェクトに関する概要情報が含まれています。 
  
コンテンツ テーブルには長い列セットがあります。 コンテンツ テーブルの必須列とオプション列の完全な一覧については、「コンテンツ テーブル」 [を参照してください](contents-tables.md)。 
  
一部のコンテナーにコンテンツがない場合があります。 これらのコンテナーは、MAPI_E_NO_SUPPORT実装の **GetContentsTable からデータを返します**。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

コンテナーのコンテンツ テーブルをサポートする場合は、次の操作も行う必要があります。
  
- コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドへの呼び出しをサポートして、PR_CONTAINER_CONTENTS **(** [PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを開きます。
    
- コンテナー **PR_CONTAINER_CONTENTS** 呼び出しに応答して、コンテナーの呼び出しを返します。 
    
    [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドと [IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッド。 
    
このメソッドのリモート トランスポート プロバイダーの実装では **、GetContentsTable** メソッドに渡される _ppTable_ パラメーターの [IMAPITable : IUnknown](imapitableiunknown.md)インターフェイスへのポインターを返す必要があります。 トランスポート プロバイダーに既存のコンテンツ テーブルがある場合は、そのテーブルへのポインターを返す必要があります。 指定しない場合、このメソッドは新しい [IMAPITable : IUnknown](imapitableiunknown.md) オブジェクトを作成し、メッセージ ヘッダーをテーブルに設定し (使用可能な場合)、新しいテーブルへのポインターを返す必要があります。 [ITableData::HrGetView](itabledata-hrgetview.md)メソッドは、戻り値を生成し、ppTable パラメーターにテーブル ポインターを格納 _する場合に便利_ です。 コンテンツ テーブルは、少なくとも次のプロパティ列をサポートする必要があります。 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>呼び出し側への注意

文字列およびバイナリコンテンツテーブルの列は切り捨て可能です。 通常、プロバイダーは 255 文字を返します。 テーブルに切り捨てられた列が含まれるかどうかは事前に分からないので、列の長さが 255 バイトまたは 510 バイトの場合は、列が切り捨てられると仮定します。 必要に応じて、切り捨てられた列の完全な値をオブジェクトから直接取得するには、そのエントリ識別子を使用して開き **、IMAPIProp::GetProps** メソッドを呼び出します。 
  
プロバイダーの実装に応じて、制限と並べ替え操作は、すべての文字列またはその文字列の切り捨てられたバージョンに適用できます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |**CContentsTableDlg** クラスは **、GetContentsTable** を使用してコンテンツ テーブル内のエントリを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerContents 標準プロパティ](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

