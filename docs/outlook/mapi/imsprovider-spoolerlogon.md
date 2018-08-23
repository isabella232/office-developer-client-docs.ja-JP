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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586418"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストアに、MAPI スプーラーをログに記録します。
  
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
  
> [in]MAPI へのポインターは、メッセージ ・ ストアのオブジェクトをサポートします。
    
 _ulUIParam_
  
> [in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。 
    
 _lpszProfileName_
  
> [in]MAPI スプーラーのログオンに使用されているプロファイルの名前を含む文字列へのポインター。 この文字列のダイアログ ボックスに表示される、ログ ファイルに書き出されます。 または単に無視されます。 _UlFlags_パラメーターに MAPI_UNICODE フラグが設定されている場合は、Unicode 形式である必要があります。 
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。 
    
 _lpEntryID_
  
> [in]メッセージ ・ ストアのエントリの識別子へのポインター。 _LpEntryID_パラメーターに NULL を渡すことは、メッセージ ストアが選択されていないと、メッセージ ストアを選択するユーザーを有効にする] ダイアログ ボックスを表示できることを示します。 
    
 _ulFlags_
  
> [in]ログオンを実行する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出しは、基になるオブジェクトが呼び出し元の実装に使用可能でない場合でも、成功するために許可されています。 オブジェクトが使用できない場合は、オブジェクトへの後続の呼び出しはエラーを発生させる可能性があります。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE が設定されていない場合は、ANSI 形式の文字列です。
    
MDB_NO_DIALOG 
  
> ログオン ダイアログ ボックスが表示できないようにします。 このフラグが設定されている場合、ログオンが成功しない場合、エラー値 MAPI_E_LOGON_FAILED が返されます。 このフラグが設定されていない場合、メッセージ ストア プロバイダーはユーザー名またはパスワード、またはストアへの接続を確立するために必要な処理を実行するディスクを挿入するのにを修正するを求めることができます。
    
MDB_WRITE 
  
> 要求の読み取り/書き込みのアクセス許可
    
 _lpInterface_
  
> [in]メッセージ ・ ストアへのログオン用のインターフェイス id (IID) へのポインター。 NULL を渡すには、メッセージ ・ ストア ([IMsgStore](imsgstoreimapiprop.md)) の MAPI インターフェイスが返されることを示します。 などに対する (IID_IMAPIProp) は、メッセージ ストアの適切なインターフェイスの識別子を_lpInterface_パラメーターを設定することもできます。 
    
 _cbSpoolSecurity_
  
> [in]_LppbSpoolSecurity_パラメーターの検証データのバイト単位のサイズへのポインター。 
    
 _lpbSpoolSecurity_
  
> [in]検証データへのポインターへのポインター。 **SpoolerLogon**メソッドでは、このデータを使用して、メッセージ ストア プロバイダーの[IMSProvider::Logon](imsprovider-logon.md)メソッドを使用してログオンするのに以前と同じストアに、MAPI スプーラーをログに記録します。 
    
 _lppMAPIError_
  
> [out]返された[MAPIERROR](mapierror.md)構造体、存在する場合エラーが発生するバージョン、コンポーネント、およびコンテキストの情報が含まれているへのポインターへのポインター。 取得する**MAPIERROR**構造体がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
 _lppMSLogon_
  
> [out]メッセージへのポインターへのポインターでは、MAPI にログオンするためのログオン オブジェクトを格納します。
    
 _lppMDB_
  
> [out]メッセージへのポインターへのポインターでは、MAPI スプーラーとクライアント アプリケーションにログオンするためのオブジェクトを格納します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNCONFIGURED 
  
> プロファイルにログオンを完了するのに十分な情報が含まれていません。 この値が返された場合は、MAPI メッセージ ストア プロバイダーのメッセージ サービスのエントリ ポイント関数を呼び出します。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しが成功したが、メッセージ ストア プロバイダーが使用可能なエラー情報を持ちます。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。 プロバイダーからエラー情報を取得するには、 [IMAPISession::GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーでは、メッセージ ストアにログオンするための**IMSProvider::SpoolerLogon**メソッドを呼び出します。 MAPI スプーラーは、中に、ログオンした後に、 _lppMDB_パラメーターでは、メッセージ ストア プロバイダーによって返されるメッセージのストア オブジェクトを使用してください。 
  
[IMSProvider::Logon](imsprovider-logon.md)メソッドを使用して、一貫性のプロバイダーは、 _lppMSLogon_パラメーターにもデータのメッセージ ストア ログオン オブジェクトを返します。 ストア オブジェクトとログオン オブジェクトの使用は同一の一般的なストア ログオンします。オブジェクトが 2 つのインターフェイスを公開する 1 つのオブジェクトであるかのように動作するよう、ログオン オブジェクトとストア オブジェクトとの間の 1 対 1 対応がかかることがあります。 2 つのオブジェクトは、同時解放と連携して作成されます。 
  
ストア プロバイダーは、ストアを MAPI スプーラーで使用されていることを示すために返されるメッセージのストア オブジェクトを内部的にマーク必要があります。 このストア オブジェクトのメソッドのいくつかがメッセージをクライアント アプリケーションに提供するオブジェクトを格納するいるとは異なる動作します。 この内部のマークを保持することは、MAPI スプーラーに固有の動作をトリガーする最も一般的な方法です。
  
## <a name="see-also"></a>関連項目



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

