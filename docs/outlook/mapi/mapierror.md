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
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345779"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、オペレーティングシステム、MAPI、またはサービスプロバイダーによって生成されるエラーに関する詳細情報を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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

 **ulversion**
  
> 構造のバージョン番号。 **ulversion**メンバーは将来の拡張に使用され、現在はゼロとして定義されている MAPI_ERROR_VERSION に設定する必要があります。 
    
 **lpszerror**
  
> エラーを説明する文字列へのポインター。 この構造体が使用されているメソッドの_ulflags_パラメーターが MAPI_UNICODE に設定されている場合、この文字列は Unicode 形式になります。 
    
 **lpszcomponent**
  
> エラーを生成したコンポーネントを説明する文字列へのポインター。 この構造体が使用されているメソッドの_ulflags_パラメーターが MAPI_UNICODE に設定されている場合、この文字列は Unicode 形式になります。 
    
 **ullowlevelerror**
  
> 返されるエラーが低レベルである場合にのみ使用される低レベルのエラー値。
    
 **ulcontext**
  
> エラーが発生した場所を識別する、 **lpszcomponent**メンバによって参照されているコンポーネント内の場所を表す値です。 
    
## <a name="remarks"></a>解説

**MAPIERROR**構造体は、エラー情報を記述するために使用されます。 クライアントおよびサービスプロバイダーは、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドの_lppMAPIError_パラメーターで、 **MAPIERROR**構造体へのポインターを渡します。 **GetLastError**は、オブジェクトに対して発生した前のエラーに関する情報を返します。 **GetLastError**の発信者は、 [MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことにより、 **MAPIERROR**構造体のメモリを解放します。
  
コンポーネントのヘルプファイルがある場合は、そのヘルプファイルをマップするために、 **lpszcomponent**メンバーを使用できます。 サービスプロバイダーは、コンポーネントの文字列のサイズを30文字に制限して、ダイアログボックスに簡単に表示できるようにする必要があります。 **ulcontext**メンバーを使用して、一般的なエラーのオンラインヘルプトピックを参照することもできます。 
  
サービスプロバイダーは詳細なエラー情報を提供する必要がないため、クライアントは、返される**MAPIERROR**構造のメンバーに、有効なデータが含まれていることを想定してはなりません。 ただし、少なくとも MAPI では、プロバイダーが**lpszcomponent**および**ulcontext**メンバーで情報を指定することを強くお勧めします。 
  
MAPI でのエラー処理の詳細については、「[エラー処理](error-handling-in-mapi.md)」を参照してください。
  
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

