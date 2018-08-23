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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 53fa6bd49190bb88daeb0438dc0112e34322383e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800625"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**適用対象**: Outlook 
  
オフライン オブジェクトに対してコールバックを受信するようにクライアントを登録します。
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
>  [in]動作を変更するフラグです。 MAPIOFFLINE_ADVISE_DEFAULT の値のみがサポートされています。 
    
 _pAdviseInfo_
  
> [in]コールバックの種類に関する情報やその他の詳細については、呼び出し元、コールバック、コールバック インターフェイスを表示する場合。 クライアントの呼び出し元にコールバックの後続の通知を送信することで Outlook を使用するクライアントのトークンも含まれています。
    
 _pulAdviseToken_
  
> [out]その後、オブジェクトのコールバックをキャンセルするクライアントの呼び出し元に返されるアドバイスのトークンです。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 呼び出しが正常になされました。
    
E_INVALIDARG
  
> 無効なパラメーターが指定されています。
    
E_NOINTERFACE
  
> *PAdviseInfo*で指定されたコールバック インターフェイスが有効ではありません。 
    
## <a name="remarks"></a>注釈

**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフラインのオブジェクトを開くには、クライアントは、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。 クライアントは、 **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用して、オブジェクトがサポートするコールバックの種類を確認できます。 クライアントには、型とその他の詳細が、そのオブジェクトについては、このようなコールバックを受信するように登録するのには**IMAPIOfflineMgr::Advise**を呼び出し、コールバックを決定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

