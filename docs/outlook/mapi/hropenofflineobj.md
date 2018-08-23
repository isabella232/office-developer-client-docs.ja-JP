---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc71974d841005785932cc9017d44c3c0614687d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563388"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
特定のプロファイルでオフラインのオブジェクトを開きます。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>パラメーター

 _ulReserved_
  
> [in]このパラメーターは使用されません。 0 である必要があります。
    
 _pwszProfileNameIn_
  
> [in]オフライン オブジェクトが適用されるプロファイルの名前です。 は、Unicode で表現する必要があります。 
    
 _pGUID_
  
> [in]オフラインの他のオブジェクトからこのオブジェクトを一意に識別に使用できる GUID へのポインター。 **GUID_GlobalState**である必要があります。
    
 _保持_
  
> [in]このパラメーターは使用されません。 **Null**である必要があります。
    
 _ppOfflineObj_
  
> [out]要求されたオフライン オブジェクトへのポインター。 呼び出し元がこのポインターを使ってアクセスするのには、 [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)インターフェイスをオブジェクトがサポートするコールバックを検索して、それ用のコールバックを設定します。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数の呼び出しが成功します。
    
MAPI_E_NOT_FOUND
  
- 関数呼び出しが失敗しました。
    
## <a name="remarks"></a>注釈

これは、クライアントでクライアントは、特定のプロファイルの接続状態の変更の通知を希望する場合は、最初の呼び出しです。 **HrOpenOfflineObj**を呼び出すと、時に、クライアントは、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。 クライアントを使用して[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md))、オブジェクトがサポートするコールバックの種類を確認し、コールバックを (を使用して設定[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md))。
  
Msmapi32.dll のこの関数のアドレスを検索するには、 [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)を使用して、プロシージャ名として**HrOpenOfflineObj@20**を指定します。 
  
 **HrOpenOfflineObj**は、COM アドインおよび Exchange クライアント拡張機能が Outlook のプロセス内で実行中の MAPI プロバイダーは、クライアントに対してのみ有効です。 それ以外の場合、 **HrOpenOfflineObj**は**MAPI_E_NOT_FOUND**を返します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)

