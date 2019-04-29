---
title: imapisessionqueryidentity
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
  
セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpcbEntryID_
  
> 読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。 
    
 _lppentryid_
  
> 読み上げプライマリ id を提供するオブジェクトのエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プライマリ id が正常に返されました。
    
MAPI_W_NO_SERVICE 
  
> 呼び出しは成功しましたが、セッションのプライマリ id がありません。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>注釈

**imapisession:: queryidentity**メソッドは、現在のセッションのプライマリ id を取得し、 _lppentryid_パラメーターを使用して値を返します。 プライマリ id は、通常、セッションのユーザーを表す、オブジェクト (通常はメッセージングユーザー) です。  _lppentryid_は、 [PidTagEntryID](pidtagentryid-canonical-property.md)プロパティとしても格納されている[imailuser](imailuserimapiprop.md)オブジェクトのプライマリ id を返します。 _lppentryid_で返された値を使用して、 [imapisession:: openentry](imapisession-openentry.md)を使用して**imailuser**オブジェクトを開くことができます。
  
複数のメッセージサービスのサービスプロバイダーの多くは、セッションのプライマリ id を提供していますが、MAPI は1つのサービスプロバイダーを指定します。 プライマリ id を提供するサービスプロバイダーは、次の項目を設定します。
  
- **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティの STATUS_PRIMARY_IDENTITY フラグ。
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) プロパティ。
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) プロパティ。
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) プロパティ。
    
プライマリ id を提供するサービスプロバイダーがメッセージサービスに属している場合、メッセージサービス内の他のサービスプロバイダーも PR_IDENTITY プロパティを設定します。 これらのプロパティは、セッションの状態テーブルで公開されます。 
  
可能であれば、 **queryidentity**は、STATUS_PRIMARY_IDENTITY でタグ付けされた状態行から**PR_IDENTITY_ENTRYID**プロパティの値を返します。 **PR_IDENTITY_ENTRYID**プロパティがプライマリ id 行にない場合、 **queryidentity**はその行から他の情報で構築された、1回限りのエントリ識別子を返します。 
  
STATUS_PRIMARY_IDENTITY フラグが状態テーブル内のすべての**PR_RESOURCE_FLAG**列から欠落している場合、 **queryidentity**は、検出された最初のエントリ識別子を返します。 返される適切なエントリ識別子が存在しない場合、 **queryidentity**は警告 MAPI_W_NO_SERVICE で成功し、 _lppentryid_はハードコードされたエントリ識別子になります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)メソッドを呼び出して、メッセージサービスにセッションのプライマリ id を指定するタスクを割り当てることができます。 
  
プライマリ id を取得するもう1つの方法は、 **PR_RESOURCE_FLAGS**列が STATUS_PRIMARY_IDENTITY に設定されている行の状態テーブルを検索することです。 この代替方法によって id 情報を取得する方法の詳細については、「 [status Table and status Objects](status-table-and-status-objects.md)」を参照してください。
  
**queryidentity**から返されるプライマリ id のエントリ識別子の使用を終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、そのメモリを解放します。 
  
一般的な id の詳細については、「 [MAPI プライマリ id](mapi-primary-identity.md)」を参照してください。 
  
MAPI セッション id の取得の詳細については、「[プライマリおよびプロバイダー id を取得](retrieving-primary-and-provider-identity.md)する」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onqueryidentity  <br/> |mfcmapi は、 **imapisession:: queryidentity**メソッドを使用して、セッションのプライマリ id のアドレス帳エントリを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI プライマリ id](mapi-primary-identity.md)
  
[プライマリとプロバイダー id の取得](retrieving-primary-and-provider-identity.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)
  
[状態テーブルと状態オブジェクト](status-table-and-status-objects.md)

