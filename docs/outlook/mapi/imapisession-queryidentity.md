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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800705"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**適用されます**: Outlook 
  
セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]プライマリ id を提供するオブジェクトのエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プライマリ id が正常に返されました。
    
MAPI_W_NO_SERVICE 
  
> 呼び出しが成功したが、セッションのプライマリ id がありません。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPISession::QueryIdentity**メソッドは、現在のセッションのプライマリ id を取得し、 _lppEntryID_パラメーターを使用して値を返します。 プライマリ id は、通常、メッセージング、ユーザー セッションのユーザーを表すオブジェクトです。  _lppEntryID_は、 [IMailUser](imailuserimapiprop.md)オブジェクトは、 [PidTagEntryID](pidtagentryid-canonical-property.md)プロパティも格納されているプライマリ id を返します。 [IMAPISession::OpenEntry](imapisession-openentry.md)を使用して**IMailUser**オブジェクトを開くには、 _lppEntryID_で返される値を使用できます。
  
複数のメッセージ サービスで多くのサービス プロバイダーは、セッションのプライマリ id を提供できます、ただし、MAPI は 1 つのサービス プロバイダーを指定します。 プライマリ id を提供するサービス プロバイダーは、次の項目を設定します。
  
- **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティに STATUS_PRIMARY_IDENTITY フラグです。
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) のプロパティです。
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) のプロパティです。
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) のプロパティです。
    
プライマリ id を提供するサービス プロバイダーに属する場合、メッセージ サービス、メッセージ サービスで、他のサービス ・ プロバイダーはまた PR_IDENTITY プロパティを設定します。 これらのプロパティは、セッションのステータス テーブルに発行されます。 
  
可能であれば、 **QueryIdentity**は、STATUS_PRIMARY_IDENTITY でタグ付けされた状態の行の**PR_IDENTITY_ENTRYID**プロパティの値を返します。 **PR_IDENTITY_ENTRYID**プロパティがプライマリ id の行に表示されない場合は、 **QueryIdentity**はその行の他の情報で作成された一時エントリ id を返します。 
  
STATUS_PRIMARY_IDENTITY フラグがすべてのステータス テーブルに**PR_RESOURCE_FLAG**列に表示されない場合は、 **QueryIdentity**は、検出された最初のエントリ id を返します。 取得する適切なエントリの識別子がない場合、 **QueryIdentity**は MAPI_W_NO_SERVICE の警告は成功し、 _lppEntryID_を指すハード コーディングされたエントリの識別子。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ サービスのセッションのプライマリ id を指定するタスクを割り当てるには[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)メソッドを呼び出すことができます。 
  
プライマリ id を取得する別の方法は、STATUS_PRIMARY_IDENTITY に**PR_RESOURCE_FLAGS**の列を持つ行のステータス テーブルを検索することによってです。 この id 情報を取得する別の方法の詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。
  
**QueryIdentity**によって返されるプライマリ id のエントリ id を使用してが完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出してメモリを解放します。 
  
識別情報の詳細については一般に、 [MAPI のプライマリ Id](mapi-primary-identity.md)を参照してください。 
  
MAPI セッションの id を取得の詳細については、[主に取得してプロバイダーの Id](retrieving-primary-and-provider-identity.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI では、 **IMAPISession::QueryIdentity**メソッドを使用して、セッションのプライマリ id のアドレス帳のエントリを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI のプライマリ Id](mapi-primary-identity.md)
  
[プライマリ デバイスとプロバイダーの Id を取得しています。](retrieving-primary-and-provider-identity.md)
  
[エラー処理のためのマクロを使用してください。](using-macros-for-error-handling.md)
  
[状態テーブルとオブジェクトの状態](status-table-and-status-objects.md)

