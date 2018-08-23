---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8cb7934919722139622b6caf3aac741c9b2e54c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582463"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アクティブなセッションへの接続を確立します。
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a>パラメーター

 _lpMAPISup_
  
> [in]アドレス帳プロバイダーのサポートのオブジェクトへのポインター。
    
 _ulUIParam_
  
> [in]許可されている場合、**ログオン**方法を表示する [ログオン] ダイアログ ボックスの親ウィンドウへのハンドル。 _UlUIParam_パラメーターには、MAPI [MAPILogonEx](mapilogonex.md)関数には、以前の呼び出しで渡された同じ名前のパラメーターの値が含まれています。 
    
 _lpszProfileName_
  
> [in]セッション ・ プロファイルの名前へのポインター。
    
 _ulFlags_
  
> [in]ログオンを実行する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
AB_NO_DIALOG 
  
> プロバイダーは、ログオン時にダイアログ ボックスを表示しない必要があります。 このフラグが設定されていない場合、プロバイダーは、構成情報が不足しているユーザーの入力を求めるダイアログ ボックスを表示できます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に完了可能性がありますログオン プロセスを完了する前に**ログオン**を有効にします。 
    
MAPI_UNICODE 
  
> すべての文字列は、Unicode 形式である必要があります。 MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列を引き起こすことがあります。
    
 _lpulcbSecurity_
  
> [で [チェック アウト]_LppbSecurity_パラメーターで指定されたセキュリティ資格情報の構造体のバイト単位のサイズへのポインター。 入力では、値を 0 以外にする必要があります。出力では、値は 0 にする必要があります。 どちらの場合も、ポインターが有効でなければなりません。 
    
 _lppbSecurity_
  
> [で [チェック アウト]セキュリティの資格情報へのポインターへのポインター。 入力では、値を 0 以外にする必要があります。出力では、値は 0 にする必要があります。 どちらの場合も、ポインターが有効でなければなりません。
    
 _lppMAPIError_
  
> [out][MAPIERROR](mapierror.md)構造体へのポインターへのポインター。 取得する**MAPIERROR**構造体がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
 _lppABLogon_
  
> [out]プロバイダーのログオン オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> アクティブなセッションへの接続が正常に確立しました。
    
MAPI_E_FAILONEPROVIDER 
  
> プロバイダーがログオンできないが、MAPI は、メッセージ サービス プロバイダーが所属するその他のプロバイダーにログインを続行できます。 
    
MAPI_E_UNCONFIGURED 
  
> プロバイダーには、ログオンを完了する十分な情報があります。 MAPI は、プロバイダーのメッセージ サービスのエントリ関数が呼び出されます。
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコード ページをサポートするために構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするために構成されていません。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常、[ログオン] ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

各アドレス帳プロバイダーには、クライアントが、 [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)メソッドを呼び出すと、セッション ・ プロファイルで接続を確立します。 **OpenAddressBook**は、各プロバイダーの**ログオン**メソッドを呼び出します。 
  
_UlFlags_パラメーターの MAPI_UNICODE フラグの有無によって示されているように、ユーザーのクライアントの文字セットでは、 _lpszProfileName_パラメーターで指定されたプロファイル名が表示されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**ログオン**メソッドの実装では、一意の識別子、または[MAPIUID](mapiuid.md)の構造体を登録するのには[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出します。 この**MAPIUID**を含むエントリの識別子をオブジェクトのがあります。 MAPI では、そのプロバイダーを使用してオブジェクトを一致するように**MAPIUID**を使用します。 たとえば、クライアントは、メッセージングのユーザーを開くには、 [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出すと、 **OpenEntry**を調べ、 **MAPIUID**の部分で渡されたしで登録されている**MAPIUID**の内容と一致するエントリの識別子をアドレス帳プロバイダー。 
  
クライアント ログオンした場合、プロバイダーを複数回、ログオンのたびに別の**MAPIUID**を登録することがあります。 独自の**MAPIUID**構造体を登録するには、適切なプロバイダーのインスタンスに要求を正しくルーティングするための MAPI が有効にします。 ただし、1 つの**MAPIUID**を共有するすべてのログオン オブジェクトが存在する可能性があります。 この例では、する必要があります、ルーティングを処理するために MAPI を使用する代わりに自分でします。 の**MAPIUID**を作成する方法の詳細については、[登録するサービス プロバイダー固有の識別子](registering-service-provider-unique-identifiers.md)を参照してください。
  
MAPI が_lpMAPISup_パラメーターで、**ログオン**のメソッドに渡されるサポート オブジェクトに含まれているメソッドの多くへのアクセスを提供する、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースです。 MAPI では、プロバイダーの種類に合わせてカスタマイズされたサポート オブジェクトを作成します。 などの接続を確立すると、基になるメッセージング システムやディレクトリ サービスへのログオンが必要な場合は、この特定のログオン セッションのセキュリティ資格情報を取得するために[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出すことができます。 
  
**ログオン**が成功した場合、参照カウントをインクリメントするサポート オブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)メソッドを呼び出すことを確認します。 これは、セッションの残りの部分のサポート オブジェクトへのポインターを保持するのには、プロバイダーを使用できます。 この**AddRef**メソッドを呼び出していないと、MAPI は、プロバイダーをアンロードします。 
  
エラー] ダイアログ ボックス、ログオン画面、または他のユーザー インターフェイス内の_lpszProfileName_パラメーターで渡されたプロファイルの名前を含めることができます。 プロファイル名を使用するに割り当てた記憶域にコピーします。 
  
ログオン オブジェクトを作成し、 _lppABLogon_パラメーターで、それへのポインターを返します。 MAPI では、このログオン オブジェクトを使用して、 [IABLogon](iablogoniunknown.md)実装では、メソッドへの呼び出しを加えます。 
  
ログオン時にパスワードを必要とする場合は、AB_NO_DIALOG フラグが設定されていない場合にのみ、[ログオン] ダイアログ ボックスを表示します。 ユーザーは、ログオン プロセスをキャンセルした場合通常、ダイアログ ボックスで [**キャンセル**] ボタンをクリックすると、MAPI_E_USER_CANCEL から返す**ログオン**します。
  
通常、アドレス帳プロバイダーはログオンできません、MAPI が無効になります、メッセージ サービスが障害のあるプロバイダーが所属する、つまり、MAPI しようとしてのいずれかのセッションの残りの部分のサービスに属している他のプロバイダーの接続を確立有効期間です。 ただし、プロバイダーは接続を確立できませんし、全体のサービスを無効にしない場合は、MAPI_E_FAILONEPROVIDER または MAPI_E_UNCONFIGURED のいずれかを返します。 MAPI には、プロバイダーが所属するメッセージ サービスは無効にされます。 
  
MAPI_E_FAILONEPROVIDER エラーが発生する場合の戻り値は、メッセージ サービスで他のプロバイダーが接続を確立することを防止するほど深刻ではありません。 プロファイルから必要な構成情報が見つからない場合、戻り値の MAPI_E_UNCONFIGURED は、ユーザー入力を求めるダイアログ ボックスを表示できません。 MAPI は、MSG_SERVICE_CONFIGURE セットを使用して、プロバイダーのメッセージ サービス エントリ ポイント関数を設定する機会自体、か、プログラムを使用してサービスを提供する_ulContext_パラメーターとして呼び出しまたはプロパティ シートを使用して応答します。 メッセージ サービスのエントリ ポイント関数が完了、MAPI ログオンを再試行します。 
  
## <a name="see-also"></a>関連項目



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

