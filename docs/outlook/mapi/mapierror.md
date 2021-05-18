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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409147"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、オペレーティング システム、MAPI、またはサービス プロバイダーによって生成されるエラーに関する詳細情報を提供します。 
  
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
  
> 構造のバージョン番号。 **ulVersion メンバー** は将来の拡張に使用され、現在 0 として定義されている MAPI_ERROR_VERSIONに設定する必要があります。 
    
 **lpszError**
  
> エラーを表す文字列へのポインター。 この構造体を使用するメソッドの  _ulFlags_ パラメーターが次の値に設定されている場合、この文字列は Unicode 形式MAPI_UNICODE。 
    
 **lpszComponent**
  
> エラーを生成したコンポーネントを表す文字列へのポインター。 この構造体を使用するメソッドの  _ulFlags_ パラメーターが次の値に設定されている場合、この文字列は Unicode 形式MAPI_UNICODE。 
    
 **ulLowLevelError**
  
> 返されるエラーが低レベルの場合にのみ使用される低レベルのエラー値。
    
 **ulContext**
  
> エラーが発生した場所を識別する **lpszComponent** メンバーが指すコンポーネント内の場所を表す値。 
    
## <a name="remarks"></a>注釈

**MAPIERROR 構造体は**、エラー情報を記述するために使用されます。 クライアントとサービス プロバイダーは [、IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドの _lppMAPIError_ パラメーターで **MAPIERROR** 構造体へのポインターを渡します。 **GetLastError** は、オブジェクトに発生した以前のエラーに関する情報を返します。 **GetLastError の呼び出し元は**、MAPIFreeBuffer を呼び出すことによって **MAPIERROR** 構造体の [メモリを解放します](mapifreebuffer.md)。
  
**lpszComponent** メンバーを使用して、コンポーネントのヘルプ ファイル (存在する場合) をマップできます。 サービス プロバイダーは、ダイアログ ボックスに簡単に表示できるよう、コンポーネント文字列のサイズを 30 文字に制限する必要があります。 ulContext **メンバーは** 、一般的なエラーのオンライン ヘルプ トピックを参照するためにも使用できます。 
  
サービス プロバイダーは詳細なエラー情報を提供する必要はないので、クライアントは有効なデータを含む **MAPIERROR** 構造体のメンバーを期待しない必要があります。 ただし、少なくとも MAPI では、プロバイダーが **lpszComponent** メンバーと **ulContext** メンバーに情報を指定する必要があります。 
  
MAPI でのエラー処理の詳細については、「エラー処理」 [を参照してください](error-handling-in-mapi.md)。
  
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

