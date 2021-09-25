---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 17d3bd9edb392db85ba8b5845a396fbf41af4525
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596184"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン オブジェクトでコールバックを受信するクライアントを登録します。
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
>  [in]動作を変更するフラグ。 サポートされている値MAPIOFFLINE_ADVISE_DEFAULT指定します。 
    
 _pAdviseInfo_
  
> [in]コールバックの種類、コールバックを受信する場合、呼び出し元のコールバック インターフェイス、その他の詳細に関する情報。 また、後続の通知コールバックをクライアントの呼びOutlookに送信する場合に使用するクライアント トークンも含まれます。
    
 _pulAdviseToken_
  
> [out]その後、オブジェクトのコールバックをキャンセルするためにクライアントの呼び出し元に返されるアドバイス トークン。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 呼び出しが正常になされました。
    
E_INVALIDARG
  
> 無効なパラメーターが指定されています。
    
E_NOINTERFACE
  
> *pAdviseInfo* で指定されたコールバック インターフェイスが無効です。 
    
## <a name="remarks"></a>注釈

**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフライン オブジェクトを開く場合、クライアントは **IMAPIOfflineMgr** をサポートするオフライン オブジェクトを取得します。 クライアントは **[、IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用して、オブジェクトでサポートされるコールバックの種類を確認できます。 クライアントは、必要なコールバックの種類と他の詳細を特定し **、IMAPIOfflineMgr::Advise** を呼び出して、オブジェクトに関するそのようなコールバックを受け取る登録を行います。 
  
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

