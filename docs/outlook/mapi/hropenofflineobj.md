---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 89b9f53c6677b61c9e61ae6cb77fe6451e786e85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610784"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロファイルに基づいてオフライン オブジェクトを開きます。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
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
  
> [in]オフライン オブジェクトのプロファイルの名前。 Unicode で表す必要があります。 
    
 _pGUID_
  
> [in]他のオフライン オブジェクトからこのオブジェクトを一意に識別するために使用できる GUID へのポインター。 これは **、次の** GUID_GlobalState。
    
 _pReserved_
  
> [in]このパラメーターは使用されません。 null である **必要があります**。
    
 _ppOfflineObj_
  
> [out]要求されたオフライン オブジェクトへのポインター。 呼び出し元は、このポインターを使用して [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) インターフェイスにアクセスして、このオブジェクトがサポートするコールバックを検索し、コールバックを設定できます。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数呼び出しが成功しました。
    
MAPI_E_NOT_FOUND
  
- 関数呼び出しが失敗しました。
    
## <a name="remarks"></a>注釈

これは、クライアントが特定のプロファイルの接続状態の変更を通知する場合にクライアントが行う最初の呼び出しです。 **HrOpenOfflineObj を呼び** 出す際に、クライアントは **IMAPIOfflineMgr** をサポートするオフライン オブジェクトを取得します。 クライアントは [、(IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)を使用して) オブジェクトでサポートされるコールバックの種類を確認し [、(IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)を使用して) コールバックを設定できます。
  
[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)を使用してこの関数のアドレスを検索する場合は、プロシージャmsmapi32.dllとして **HrOpenOfflineObj@20を指定** します。 
  
 **HrOpenOfflineObj** は、MAPI プロバイダー、COM アドイン、および Exchange プロセス内で実行されているクライアントOutlook機能します。 それ以外の **場合、HrOpenOfflineObj** は **次MAPI_E_NOT_FOUNDします**。 
  
## <a name="see-also"></a>関連項目



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI 定数](mapi-constants.md)

