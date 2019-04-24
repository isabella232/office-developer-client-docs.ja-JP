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
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347748"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のプロファイルに基づいてオフラインオブジェクトを開きます。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |msmapi32  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
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

 _ulreserved_
  
> 順番このパラメーターは使用されません。 0である必要があります。
    
 _pwszProfileNameIn_
  
> 順番オフラインオブジェクトのプロファイルの名前を指定します。 Unicode で表されている必要があります。 
    
 _pguid_
  
> 順番他のオフラインオブジェクトからこのオブジェクトを一意に識別するために使用できる GUID へのポインター。 **GUID_GlobalState**である必要があります。
    
 _保持され_
  
> 順番このパラメーターは使用されません。 **null**である必要があります。
    
 _ppofflineobj_
  
> 読み上げ要求されたオフラインオブジェクトへのポインター。 発信者はこのポインターを使用して[IMAPIOfflineMgr: imapioffline](imapiofflinemgrimapioffline.md)インターフェイスにアクセスし、このオブジェクトでサポートされているコールバックを検索し、そのためのコールバックを設定できます。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数呼び出しが成功しました。
    
MAPI_E_NOT_FOUND
  
- 関数の呼び出しに失敗しました。
    
## <a name="remarks"></a>解説

これは、クライアントが特定のプロファイルの接続状態変更を通知する際にクライアントが行う最初の呼び出しです。 **hroIMAPIOfflineMgr offlineobj**を呼び出すと、クライアントは**** をサポートするオフラインオブジェクトを取得します。 クライアントは、( [imapioffline:: getcapabilities](imapioffline-getcapabilities.md)を使用して) オブジェクトでサポートされているコールバックの種類を確認し、そのためのコールバックを設定します ( [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)を使用)。
  
[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)を使用して msmapi32 でこの関数のアドレスを検索する場合は、手順名として**hrolook offlineobj @ 20**を指定します。 
  
 **hroare offlineobj**は、Outlook プロセス内で実行されている MAPI プロバイダー、COM アドイン、および Exchange クライアント拡張機能であるクライアントに対してのみ機能します。 それ以外の場合、 **hroMAPI_E_NOT_FOUND offlineobj**は**** を返します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI 定数](mapi-constants.md)

