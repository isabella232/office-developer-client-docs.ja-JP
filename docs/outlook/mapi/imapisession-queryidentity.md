---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428222"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションのプライマリ ID を提供するオブジェクトのエントリ識別子を返します。
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpcbEntryID_
  
> [out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppEntryID_
  
> [out]プライマリ ID を提供するオブジェクトのエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プライマリ ID が正常に返されました。
    
MAPI_W_NO_SERVICE 
  
> 呼び出しは成功しましたが、セッションのプライマリ ID はありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPISession::QueryIdentity** メソッドは、現在のセッションのプライマリ ID を取得し _、lppEntryID_ パラメーターを使用して値を返します。 プライマリ ID は、セッションのユーザーを表すオブジェクト (通常はメッセージング ユーザー) です。  _lppEntryID_ は [、PidTagEntryID](pidtagentryid-canonical-property.md)プロパティとして格納される [IMailUser](imailuserimapiprop.md)オブジェクトのプライマリ ID を返します。 _lppEntryID_ で返される値を使用して [、IMAPISession::OpenEntry](imapisession-openentry.md)を使用して **IMailUser** オブジェクトを開きます。
  
複数のメッセージ サービス内の多くのサービス プロバイダーは、セッションのプライマリ ID を提供することができますが、MAPI は 1 つのサービス プロバイダーを指定します。 プライマリ ID を提供するサービス プロバイダーは、次の項目を設定します。
  
- プロパティSTATUS_PRIMARY_IDENTITY **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティPR_RESOURCE_FLAGSフラグを指定します。
    
- プロパティ **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) プロパティです。
    
- プロパティ **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) プロパティです。
    
- プロパティ **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) プロパティです。
    
プライマリ ID を提供するサービス プロバイダーがメッセージ サービスに属している場合は、メッセージ サービス内の他のサービス プロバイダーも PR_IDENTITYプロパティを設定します。 これらのプロパティは、セッションの状態テーブルに公開されます。 
  
可能な場合 **、QueryIdentity** は、PR_IDENTITY_ENTRYIDプロパティにタグ付けされた状態行の値をSTATUS_PRIMARY_IDENTITY。 プライマリ ID **行PR_IDENTITY_ENTRYID** プロパティが見つからない場合 **、QueryIdentity** は、その行の他の情報を含む 1 回のエントリ識別子を返します。 
  
状態テーブルSTATUS_PRIMARY_IDENTITYのすべての PR_RESOURCE_FLAG 列に対して、STATUS_PRIMARY_IDENTITYフラグが見つからない場合 **、QueryIdentity** は最初に見つけたエントリ識別子を返します。 返す適切なエントリ識別子がない場合 **、QueryIdentity** は警告 MAPI_W_NO_SERVICE で成功し  _、lppEntryID_ をハードコードされたエントリ識別子にポイントします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)メソッドを呼び出して、セッションのプライマリ ID を指定するタスクをメッセージ サービスに割り当てできます。 
  
プライマリ ID を取得するもう 1 つの方法は、行の状態テーブルを検索し、列のPR_RESOURCE_FLAGSに設定STATUS_PRIMARY_IDENTITY。 ID 情報を取得するこの代替方法の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。
  
**QueryIdentity** によって返されるプライマリ ID のエントリ識別子の使用が完了したら [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出してメモリを解放します。 
  
一般的な ID の詳細については [、「MAPI プライマリ ID」を参照してください](mapi-primary-identity.md)。 
  
MAPI セッション ID の取得の詳細については、「プライマリ ID とプロバイダー ID の取得 [」を参照してください](retrieving-primary-and-provider-identity.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI は **IMAPISession::QueryIdentity** メソッドを使用して、セッションのプライマリ ID のアドレス帳エントリを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI プライマリ ID](mapi-primary-identity.md)
  
[プライマリ ID とプロバイダー ID の取得](retrieving-primary-and-provider-identity.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)
  
[Status Table オブジェクトと Status オブジェクト](status-table-and-status-objects.md)

