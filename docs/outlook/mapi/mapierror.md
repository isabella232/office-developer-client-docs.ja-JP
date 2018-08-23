---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bbf8e2eb2961a3d149010b876d2b4cb3d0c8abc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592529"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オペレーティング システム、MAPI、またはサービス プロバイダーによって生成される通常のエラーに関する詳細な情報を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a>Members

 **ulVersion**
  
> 構造体のバージョン番号です。 **UlVersion**メンバーは、将来の拡張に使用し、0 として現在定義されている、MAPI_ERROR_VERSION に設定する必要があります。 
    
 **lpszError**
  
> エラーを説明する文字列へのポインター。 _UlFlags_この構造体を使用するメソッド パラメーターが MAPI_UNICODE に設定されている場合、この文字列は Unicode 形式になります。 
    
 **lpszComponent**
  
> エラーを生成したコンポーネントを説明する文字列へのポインター。 _UlFlags_この構造体を使用するメソッド パラメーターが MAPI_UNICODE に設定されている場合、この文字列は Unicode 形式になります。 
    
 **ulLowLevelError**
  
> 返されるエラーは、低レベル時のみに使用される低レベルのエラー値です。
    
 **ulContext**
  
> エラーの発生場所を識別する**lpszComponent**のメンバーが指すコンポーネントの位置を表す値です。 
    
## <a name="remarks"></a>注釈

**MAPIERROR**構造体を使用して、エラー情報を記述します。 クライアントとサービス ・ プロバイダー、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドの_lppMAPIError_パラメーター内の**MAPIERROR**構造体へのポインターを渡します。 **GetLastError**は、前のオブジェクトに対して発生したエラーに関する情報を返します。 **GetLastError**の呼び出し元は、 [MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことによって、 **MAPIERROR**構造体のメモリを解放します。
  
**LpszComponent**メンバーは、いずれかが存在する場合、コンポーネントのヘルプ ファイルにマップする使用できます。 サービス プロバイダーは、ダイアログ ボックスで簡単に表示できるように、30 文字にコンポーネントの文字列のサイズを制限します。 **UlContext**メンバーは、一般的なエラーのオンライン ヘルプ トピックを参照してくださいにも使用できます。 
  
サービス プロバイダーの詳細なエラー情報を提供するために必要でないため、クライアントとは限りません有効なデータを格納する返された**MAPIERROR**構造体のメンバーのいずれかです。 ただし、最低限の MAPI で強くお勧めプロバイダーが**lpszComponent**と**ulContext**のメンバーの情報を指定することです。 
  
MAPI でのエラー処理の詳細については、[エラー処理](error-handling-in-mapi.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)
  
[IMSLogon::GetLastError](imslogon-getlasterror.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IProfAdmin::GetLastError](iprofadmin-getlasterror.md)
  
[IProviderAdmin::GetLastError](iprovideradmin-getlasterror.md)


[MAPI の構造](mapi-structures.md)

