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
  
MAPI スプーラーをメッセージストアに記録します。
  
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
  
> 順番メッセージストアの MAPI サポートオブジェクトへのポインター。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 
    
 _lpszprofilename_
  
> 順番MAPI スプーラーログオンに使用されているプロファイルの名前を含む文字列へのポインター。 この文字列は、ダイアログボックスに表示したり、ログファイルに書き込んだたり、単に無視したりできます。 MAPI_UNICODE フラグが_ulflags_パラメーターで設定されている場合は、Unicode 形式である必要があります。 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。 
    
 _lて tryid_
  
> 順番メッセージストアのエントリ識別子へのポインター。 _lな tryid_パラメーターで NULL を渡すと、メッセージストアがまだ選択されていないことと、ユーザーがメッセージストアを選択できるようにするダイアログボックスが表示されることを示します。 
    
 _ulFlags_
  
> 順番ログオンの実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のオブジェクトが呼び出し側の実装で使用できない場合でも、呼び出しを成功させることができます。 オブジェクトが使用できない場合は、その後のオブジェクトの呼び出しでエラーが発生する可能性があります。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE が設定されていない場合、文字列は ANSI 形式になります。
    
MDB_NO_DIALOG 
  
> ログオンダイアログボックスを表示しないようにします。 このフラグが設定されている場合は、ログオンが失敗した場合にエラー値 MAPI_E_LOGON_FAILED が返されます。 このフラグが設定されていない場合、メッセージストアプロバイダーはユーザーに対して、名前またはパスワードを修正するか、ディスクを挿入するか、またはストアへの接続を確立するために必要なその他の操作を実行するように求めることができます。
    
MDB_WRITE 
  
> 読み取り/書き込みアクセス許可を要求します。
    
 _lpinterface_
  
> 順番ログオンするメッセージストアのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、メッセージストア ([IMsgStore](imsgstoreimapiprop.md)) の MAPI インターフェイスが返されます。 _lpinterface_パラメーターは、メッセージストアの適切なインターフェイスの識別子に設定することもできます (たとえば、IID_IUnknown または IID_IMAPIProp)。 
    
 _cbSpoolSecurity_
  
> 順番_lppbSpoolSecurity_パラメーターの検証データのサイズ (バイト単位) へのポインター。 
    
 _lpbSpoolSecurity_
  
> 順番検証データへのポインターへのポインター。 **SpoolerLogon**メソッドは、このデータを使用して、 [IMSProvider:: Logon](imsprovider-logon.md)メソッドを使用して、以前にログオンしたメッセージストアプロバイダーと同じストアに MAPI スプーラーを記録します。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む返された[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。 返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
 _lppmslogon_
  
> 読み上げMAPI がログオンするためのメッセージストアログオンオブジェクトへのポインターへのポインター。
    
 _lppmdb_
  
> 読み上げログオンする MAPI スプーラーおよびクライアントアプリケーションのメッセージストアオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNCONFIGURED 
  
> このプロファイルには、ログオンが完了するのに十分な情報が含まれていません。 この値が返されると、MAPI はメッセージストアプロバイダーのメッセージサービスエントリポイント関数を呼び出します。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、メッセージストアプロバイダーにエラー情報があります。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。 プロバイダーからエラー情報を取得するには、 [imapisession:: GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、 **IMSProvider:: SpoolerLogon**メソッドを呼び出して、メッセージストアにログオンします。 MAPI スプーラーは、ログオン時および_lppmdb_パラメーターのメッセージストアプロバイダーから返されるメッセージストアオブジェクトを使用する必要があります。 
  
[IMSProvider:: Logon](imsprovider-logon.md)メソッドとの一貫性を保つため、プロバイダーは_lppmslogon_パラメーターにメッセージストアのログオンオブジェクトも返します。 store オブジェクトと logon オブジェクトの使用方法は、通常のストアログオンの場合と同じです。これらのオブジェクトは、2つのインターフェイスを公開する1つのオブジェクトとして機能するように、ログオンオブジェクトと store オブジェクトの間に1対1で対応する必要があります。 2つのオブジェクトが一緒に作成され、一緒に解放されます。 
  
ストアプロバイダーは、返されたメッセージストアオブジェクトを内部的にマークして、ストアが MAPI スプーラーによって使用されていることを示す必要があります。 このストアオブジェクトのメソッドの動作は、クライアントアプリケーションに提供されるメッセージストアオブジェクトとは異なります。 この内部マークを保持することは、MAPI スプーラーに固有の動作をトリガーする最も一般的な方法です。
  
## <a name="see-also"></a>関連項目



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

