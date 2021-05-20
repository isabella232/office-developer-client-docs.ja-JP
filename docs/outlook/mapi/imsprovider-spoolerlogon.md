---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430575"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーをメッセージ ストアにログに記録します。
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>パラメーター

 _lpMAPISup_
  
> [in]メッセージ ストアの MAPI サポート オブジェクトへのポインター。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 
    
 _lpszProfileName_
  
> [in]MAPI スプーラー ログオンに使用されているプロファイルの名前を含む文字列へのポインター。 この文字列は、ダイアログ ボックスに表示したり、ログ ファイルに書き出したり、単に無視することができます。 _ulFlags_ パラメーターでフラグを設定MAPI_UNICODE Unicode 形式である必要があります。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。 
    
 _lpEntryID_
  
> [in]メッセージ ストアのエントリ識別子へのポインター。 _lpEntryID_ パラメーターに NULL を渡す場合は、メッセージ ストアがまだ選択されていないと、ユーザーがメッセージ ストアを選択できるダイアログ ボックスを表示できます。 
    
 _ulFlags_
  
> [in]ログオンの実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のオブジェクトが呼び出し元の実装で使用できない場合でも、呼び出しは成功できます。 オブジェクトが使用できない場合は、そのオブジェクトに対する後続の呼び出しでエラーが発生する可能性があります。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このMAPI_UNICODE設定されていない場合、文字列は ANSI 形式です。
    
MDB_NO_DIALOG 
  
> ログオン ダイアログ ボックスの表示を防止します。 このフラグを設定すると、ログオンが失敗MAPI_E_LOGON_FAILEDエラー値が返されます。 このフラグが設定されていない場合、メッセージ ストア プロバイダーは、名前またはパスワードの修正、ディスクの挿入、またはストアへの接続を確立するために必要なその他のアクションを実行するようユーザーに求めできます。
    
MDB_WRITE 
  
> 読み取り/書き込みアクセス許可を要求します。
    
 _lpInterface_
  
> [in]ログオンするメッセージ ストアのインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、メッセージ ストア[(IMsgStore)](imsgstoreimapiprop.md)の MAPI インターフェイスが返されます。 _lpInterface パラメーター_ は、メッセージ ストアの適切なインターフェイスの識別子 (たとえば、IID_IUnknown または IID_IMAPIProp) に設定することもできます。 
    
 _cbSpoolSecurity_
  
> [in]  _lppbSpoolSecurity_ パラメーター内の検証データのサイズ (バイト単位) へのポインター。 
    
 _lpbSpoolSecurity_
  
> [in]検証データへのポインターを指すポインター。 **SpoolerLogon** メソッドは、このデータを使用して [、IMSProvider::Logon](imsprovider-logon.md)メソッドを使用して以前にログオンしたメッセージ ストア プロバイダーと同じストアに MAPI スプーラーをログオンします。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される [MAPIERROR](mapierror.md) 構造体へのポインター (該当する場合) へのポインター。 _戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。 
    
 _lppMSLogon_
  
> [out]MAPI がログオンするメッセージ ストア ログオン オブジェクトへのポインターを指すポインター。
    
 _lppMDB_
  
> [out]MAPI スプーラーおよびクライアント アプリケーションがログオンするメッセージ ストア オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNCONFIGURED 
  
> プロファイルには、ログオンが完了するのに十分な情報が含まれている必要があります。 この値が返された場合、MAPI はメッセージ ストア プロバイダーのメッセージ サービス エントリ ポイント関数を呼び出します。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、メッセージ ストア プロバイダーにエラー情報が表示されます。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。 プロバイダーからエラー情報を取得するには [、IMAPISession::GetLastError メソッドを呼び出](imapisession-getlasterror.md) します。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IMSProvider::SpoolerLogon** メソッドを呼び出して、メッセージ ストアにログオンします。 MAPI スプーラーは、ログオン中とログオン後に  _lppMDB_ パラメーター内のメッセージ ストア プロバイダーによって返されるメッセージ ストア オブジェクトを使用する必要があります。 
  
[IMSProvider::Logon](imsprovider-logon.md)メソッドとの整合性を保つには、プロバイダーは _lppMSLogon_ パラメーターにメッセージ ストア ログオン オブジェクトも返します。 ストア オブジェクトとログオン オブジェクトの使用は、通常のストア ログオンと同じです。オブジェクトが 2 つのインターフェイスを公開する 1 つのオブジェクトである場合と同様に、ログオン オブジェクトとストア オブジェクトの間には 1 対 1 の対応が必要です。 2 つのオブジェクトは一緒に作成され、一緒に解放されます。 
  
ストア プロバイダーは、MAPI スプーラーによってストアが使用されているかどうかを示すために、返されるメッセージ ストア オブジェクトを内部的にマークする必要があります。 このストア オブジェクトの一部のメソッドは、クライアント アプリケーションに提供されるメッセージ ストア オブジェクトとは異なる動作をします。 この内部マークを保持すると、MAPI スプーラーに固有の動作をトリガーする最も一般的な方法です。
  
## <a name="see-also"></a>関連項目



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

