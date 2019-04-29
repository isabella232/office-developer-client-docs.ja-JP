---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426920"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントを、オフラインオブジェクトのコールバックを受信するように登録します。
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
>  順番動作を変更するフラグです。 MAPIOFFLINE_ADVISE_DEFAULT の値のみがサポートされています。 
    
 _pAdviseInfo_
  
> 順番コールバックの種類、コールバックを受信するタイミング、発信者のコールバックインターフェイス、およびその他の詳細についての情報。 また、このメソッドには、クライアントの発信者に後続の通知コールバックを送信するために Outlook が使用するクライアントトークンも含まれています。
    
 _pulAdviseToken_
  
> 読み上げその後、オブジェクトのコールバックをキャンセルするためにクライアントの呼び出し元に返されるアドバイズトークン。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 呼び出しが正常になされました。
    
E_INVALIDARG
  
> 無効なパラメーターが指定されています。
    
E_NOINTERFACE
  
> *pAdviseInfo*で指定されているコールバックインターフェイスが無効です。 
    
## <a name="remarks"></a>注釈

**[hroIMAPIOfflineMgr offlineobj](hropenofflineobj.md)** を使用してオフラインオブジェクトを開くときに、クライアントは、 **** をサポートするオフラインオブジェクトを取得します。 クライアントは、 **[imapioffline:: getcapabilities](imapioffline-getcapabilities.md)** を使用して、オブジェクトでサポートされているコールバックの種類を確認できます。 クライアントは、必要なコールバックに関する種類とその他の詳細を判断し、 **IMAPIOfflineMgr:: アドバイズ**に登録して、オブジェクトに関するそのようなコールバックを受信することができます。 
  
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

