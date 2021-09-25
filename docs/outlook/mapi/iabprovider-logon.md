---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c502d3ba8b956a6c3c83bbed6e1e17d9f11fd97b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616895"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アクティブ なセッションへの接続を確立します。
  
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
  
> [in]アドレス帳プロバイダーのサポート オブジェクトへのポインター。
    
 _ulUIParam_
  
> [in]ログオン メソッドが表示されるログオン ダイアログ ボックスの親ウィンドウへのハンドル (許可されている場合)。 _ulUIParam_ パラメーターには [、MAPILogonEx](mapilogonex.md)関数の前の呼び出しで MAPI に渡された同じ名前のパラメーターの値が含まれる。 
    
 _lpszProfileName_
  
> [in]セッション プロファイルの名前へのポインター。
    
 _ulFlags_
  
> [in]ログオンの実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_NO_DIALOG 
  
> ログオン時に、プロバイダーがダイアログ ボックスを表示しなける必要があります。 このフラグが設定されていない場合、プロバイダーはダイアログ ボックスを表示して、不足している構成情報をユーザーに求めるメッセージを表示できます。
    
MAPI_DEFERRED_ERRORS 
  
> ログオン **プロセスが** 完了する前に、ログオンが正常に返される可能性があります。 
    
MAPI_UNICODE 
  
> すべての文字列は Unicode 形式である必要があります。 このフラグMAPI_UNICODE設定しない場合、文字列は ANSI 形式である必要があります。
    
 _lpulcbSecurity_
  
> [in, out]  _lppbSecurity_ パラメーターが指すセキュリティ資格情報構造のサイズ (バイト単位) へのポインター。 入力では、値は 0 以外である必要があります。出力の場合、値は 0 である必要があります。 どちらの場合も、ポインターは有効である必要があります。 
    
 _lppbSecurity_
  
> [in, out]セキュリティ資格情報へのポインター。 入力では、値は 0 以外である必要があります。出力の場合、値は 0 である必要があります。 どちらの場合も、ポインターは有効である必要があります。
    
 _lppMAPIError_
  
> [out]MAPIERROR 構造体へのポインターを [指す](mapierror.md) ポインター。 _戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。 
    
 _lppABLogon_
  
> [out]プロバイダーのログオン オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アクティブ なセッションへの接続が正常に確立されました。
    
MAPI_E_FAILONEPROVIDER 
  
> プロバイダーはログオンできませんが、MAPI は、プロバイダーが属するメッセージ サービス内の他のプロバイダーに引き続きログオンできます。 
    
MAPI_E_UNCONFIGURED 
  
> プロバイダーにログオンを完了する情報が不足しています。 MAPI は、プロバイダーのメッセージ サービス エントリ関数を呼び出します。
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコード ページをサポートするように構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするように構成されていません。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはログオン ダイアログ ボックスの [ **キャンセル** ] ボタンをクリックして操作をキャンセルしました。 
    
## <a name="remarks"></a>注釈

クライアントが [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) メソッドを呼び出す場合、セッション プロファイル内の各アドレス帳プロバイダーとの接続が確立されます。 **OpenAddressBook は、** 各プロバイダーの Logon メソッドを **呼び出** します。 
  
_lpszProfileName_ パラメーターが示すプロファイル名は _、ulFlags_ パラメーターの MAPI_UNICODE フラグの有無によって示される、ユーザーのクライアントの文字セットに表示されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

Logon メソッドの実装 **では**[、IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出して、一意の識別子 [(MAPIUID](mapiuid.md)構造) を登録します。 各オブジェクトには、この MAPIUID を含むエントリ **識別子が含まれます**。 MAPI は **MAPIUID を使用** して、オブジェクトをプロバイダーと一致します。 たとえば、クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md) メソッドを呼び出してメッセージング ユーザーを開く場合 **、OpenEntry** は、渡されたエントリ識別子の **MAPIUID** 部分を調べ、アドレス帳プロバイダーによって登録された **MAPIUID** と一致します。 
  
クライアントがプロバイダーに複数ログオンする場合は、ログオンごとに異なる **MAPIUID** を登録できます。 一意の **MAPIUID 構造体を登録** すると、MAPI は適切なプロバイダー インスタンスに要求を正しくルーティングできます。 ただし、すべてのログオン オブジェクトで 1 つの **MAPIUID を共有できます**。 この場合、MAPI に依存するのではなく、自分でルーティングを処理できる必要があります。 **MAPIUID** を作成する方法の詳細については、「Registering Service [Provider Unique IDENTIFIERs」を参照してください](registering-service-provider-unique-identifiers.md)。
  
MAPI が _lpMAPISup_ パラメーターの **Logon** メソッドに渡すサポート オブジェクトは [、IMAPISupport : IUnknown](imapisupportiunknown.md)インターフェイスに含まれる多くのメソッドにアクセスできます。 MAPI は、プロバイダーの種類に合わせてカスタマイズされたサポート オブジェクトを作成します。 たとえば、接続を確立するときに基になるメッセージング システムまたはディレクトリ サービスにログオンする必要がある場合は [、IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、この特定のログオン セッションのセキュリティ資格情報を取得できます。 
  
Logon **が** 成功した場合は、サポート オブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出して参照カウントを増やしてください。 これにより、プロバイダーは、セッションの残りの部分のサポート オブジェクト ポインターを保持できます。 この AddRef メソッドを呼 **び出していない** 場合、MAPI はプロバイダーをアンロードします。 
  
_lpszProfileName_ パラメーターで渡されたプロファイル名は、エラー ダイアログ ボックス、ログオン画面、または他のユーザー インターフェイスに含めできます。 プロファイル名を使用するには、割り当て済みストレージにコピーします。 
  
ログオン オブジェクトを作成し  _、lppABLogon_ パラメーターにポインターを返します。 MAPI では、このログオン オブジェクトを使用して [、IABLogon 実装内のメソッドを呼び出](iablogoniunknown.md) します。 
  
ログオン時にパスワードが必要な場合は、ログオン フラグが設定されていないAB_NO_DIALOGダイアログ ボックスを表示します。 ユーザーがログオン プロセスを取り消す場合は、通常、ダイアログ ボックスの [キャンセル] ボタンをクリックして、[ログオン] からMAPI_E_USER_CANCEL返 **します**。
  
通常、アドレス帳プロバイダーがログオンできない場合、MAPI は、障害が発生したプロバイダーが属するメッセージ サービス (つまり、MAPI はセッションの残りの期間、サービスに属する他のプロバイダーの接続を確立しようとしません) を無効にします。 ただし、プロバイダーが接続を確立できない場合に、サービス全体を無効にしない場合は、サービス全体をMAPI_E_FAILONEPROVIDERまたはMAPI_E_UNCONFIGURED。 MAPI では、プロバイダーが属するメッセージ サービスは無効にされません。 
  
メッセージ MAPI_E_FAILONEPROVIDERの他のプロバイダーが接続を確立できないほど重大ではないエラーが発生した場合は、このエラーを返します。 必要MAPI_E_UNCONFIGUREDプロファイルに必要な構成情報が見つからない場合に、ユーザーにメッセージを表示するダイアログ ボックスを表示できない場合は、このダイアログ ボックスを返します。 MAPI は、MSG_SERVICE_CONFIGURE を  _ulContext_ パラメーターとして設定したプロバイダーのメッセージ サービス エントリ ポイント関数を呼び出して、プログラムによって、またはプロパティ シートを使用してサービスを構成する機会を与えます。 メッセージ サービスエントリ ポイント関数が終了すると、MAPI はログオンを再試行します。 
  
## <a name="see-also"></a>関連項目



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

