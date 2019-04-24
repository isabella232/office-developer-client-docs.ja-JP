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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348784"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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
  
> 順番アドレス帳プロバイダーのサポートオブジェクトへのポインター。
    
 _uluiparam_
  
> 順番**ログオン**方法が表示されるログオンダイアログボックスの親ウィンドウへのハンドル (許可されている場合)。 _uluiparam_パラメーターには、前の[MAPILogonEx](mapilogonex.md)関数の呼び出しで MAPI に渡された名前のパラメーターの値が含まれています。 
    
 _lpszprofilename_
  
> 順番セッションプロファイルの名前へのポインター。
    
 _ulFlags_
  
> 順番ログオンの実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_NO_DIALOG 
  
> プロバイダーは、ログオン時にダイアログボックスを表示しないようにします。 このフラグが設定されていない場合、プロバイダーはユーザーに構成情報が不足していることを確認するダイアログボックスを表示することができます。
    
MAPI_DEFERRED_ERRORS 
  
> ログオン処理が完了する前に、**ログオン**が正常に返されるようにします。 
    
MAPI_UNICODE 
  
> すべての文字列は Unicode 形式である必要があります。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式である必要があります。
    
 _lアウト cbsecurity_
  
> [入力]_lppbsecurity_パラメーターによって示されるセキュリティ資格情報構造のサイズ (バイト単位) へのポインター。 入力の場合、値は0以外の値である必要があります。出力では、この値は0である必要があります。 どちらの場合も、ポインターが有効である必要があります。 
    
 _lppbsecurity_
  
> [入力]セキュリティ資格情報へのポインターへのポインター。 入力の場合、値は0以外の値である必要があります。出力では、この値は0である必要があります。 どちらの場合も、ポインターが有効である必要があります。
    
 _lppMAPIError_
  
> 読み上げ[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。 返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
 _lppablogon_
  
> 読み上げプロバイダーのログオンオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アクティブなセッションへの接続が正常に確立されました。
    
MAPI_E_FAILONEPROVIDER 
  
> プロバイダーはログオンできませんが、MAPI は、プロバイダーが属しているメッセージサービスの他のプロバイダーに引き続きログオンできます。 
    
MAPI_E_UNCONFIGURED 
  
> プロバイダーに、ログオンを完了するための十分な情報がありません。 MAPI は、プロバイダーのメッセージサービスのエントリ関数を呼び出します。
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコードページをサポートするように構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするように構成されていません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ログオンダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>解説

クライアントが[imapisession:: OpenAddressBook](imapisession-openaddressbook.md)メソッドを呼び出すと、セッションプロファイル内の各アドレス帳プロバイダーとの接続が確立されます。 **OpenAddressBook**は、各プロバイダーの**ログオン**方法を呼び出します。 
  
_lpszprofilename_パラメーターで指定されているプロファイル名が、 _ulflags_パラメーターの MAPI_UNICODE フラグのプレゼンスまたは欠落によって示されるユーザーのクライアントの文字セットに表示されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**ログオン**方法の実装で、 [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出して、一意の識別子または[MAPIUID](mapiuid.md)構造体を登録します。 各オブジェクトには、この**MAPIUID**を含むエントリ識別子があります。 MAPI では、 **MAPIUID**を使用してオブジェクトをプロバイダーに一致させます。 たとえば、クライアントが[imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出してメッセージングユーザーを開くと、 **openentry**は、渡されたエントリ識別子の**MAPIUID**部分を調べ、それと一致する**MAPIUID**を使用して登録したアドレス帳プロバイダー。 
  
クライアントがプロバイダーに複数回ログオンしている場合は、ログオンごとに異なる**MAPIUID**を登録する必要があります。 一意の**MAPIUID**構造を登録すると、MAPI が適切なプロバイダーインスタンスに要求を正しくルーティングできるようになります。 ただし、すべてのログオンオブジェクトで1つの**MAPIUID**を共有する必要がある場合があります。 この場合は、MAPI に依存するのではなく、自分でルーティングを処理できる必要があります。 **MAPIUID**の作成方法の詳細については、「[サービスプロバイダーの一意識別子の登録](registering-service-provider-unique-identifiers.md)」を参照してください。
  
MAPI が_lpMAPISup_パラメーターで**ログオン**方法に渡すサポートオブジェクトは、 [imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスに含まれる多くのメソッドへのアクセスを提供します。 MAPI は、プロバイダーの種類に合わせてカスタマイズされたサポートオブジェクトを作成します。 たとえば、接続を確立するときに、基になるメッセージングシステムまたはディレクトリサービスにログオンする必要がある場合は、 [imapisupport:: openapiaddressmethod](imapisupport-openprofilesection.md)を呼び出して、この特定のログオンセッションのセキュリティ資格情報を取得することができます。 
  
正常に**ログオン**できた場合は、サポートオブジェクトの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して、参照カウントをインクリメントするようにしてください。 これにより、プロバイダーは、セッションの残りの部分に対して support オブジェクトポインターを保持できます。 この**AddRef**メソッドを呼び出さない場合、MAPI はプロバイダーをアンロードします。 
  
エラーダイアログボックス、ログオン画面、またはその他のユーザーインターフェイスで、 _lpszprofilename_パラメーターに渡されたプロファイル名を含めることができます。 プロファイル名を使用するには、割り当てた記憶域にプロファイル名をコピーします。 
  
ログオンオブジェクトを作成し、 _lppablogon_パラメーターでそのオブジェクトへのポインターを返します。 MAPI は、このログオンオブジェクトを使用して、 [IABLogon](iablogoniunknown.md)の実装内のメソッドを呼び出します。 
  
ログオン時にパスワードが必要な場合は、AB_NO_DIALOG フラグが設定されていない場合にのみ、ログオンダイアログボックスを表示します。 ユーザーがログオンプロセスをキャンセルした場合 (通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックすることによって、**ログオン**から MAPI_E_USER_CANCEL を返します。
  
通常、アドレス帳プロバイダーがログオンできない場合、mapi はエラーが発生しているプロバイダーが属しているメッセージサービスを無効にします。つまり、mapi は、セッションの残りの部分では、そのサービスに属している他のすべてのプロバイダーの接続を確立しようとしません。時間. ただし、プロバイダーが接続を確立できず、サービス全体を無効にしない場合は、MAPI_E_FAILONEPROVIDER または MAPI_E_UNCONFIGURED のいずれかを返します。 MAPI は、プロバイダーが属しているメッセージサービスを無効にしません。 
  
メッセージサービス内の他のプロバイダーが接続を確立できないほど深刻でないエラーが発生した場合は、MAPI_E_FAILONEPROVIDER を返します。 必要な構成情報がプロファイルに欠落していて、ユーザーに入力を求めるダイアログボックスを表示できない場合は、MAPI_E_UNCONFIGURED を返します。 MAPI は、MSG_SERVICE_CONFIGURE を_ulcontext_パラメーターとして設定し、プロバイダーのメッセージサービスエントリポイント関数を呼び出して応答することによって、プログラムまたはプロパティシートを使用してサービスを自ら構成する機会を提供します。 メッセージサービスエントリポイント関数が終了すると、MAPI はログオンを再試行します。 
  
## <a name="see-also"></a>関連項目



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

