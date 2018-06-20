---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801511"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**適用されます**: Outlook 
  
この構造体は、 [HrCreateOfflineObj](hrcreateofflineobj.md)で使用されます。
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a>メンバー

 **ulSize**
  
> 構造体のサイズです。
    
 **ulCreateFlags**
  
> 0 である必要があります。
    
 **pwszProfileName**
  
> プロファイルの名前を指定します。
    
 **ulCapabilities**
  
> 以下の機能フラグのビット マスクです。
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |オフライン オブジェクトはオフラインになることができます。  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |オフラインのオブジェクトでは、オンラインのことができます。  <br/> |
   
 **pGUID**
  
> この種類の他のオフラインのオブジェクトからオフラインのオブジェクトを一意に識別するために使用する GUID へのポインター。 GUID_GlobalState は、親オブジェクトとしてオブジェクトを使用するグローバル オブジェクトを参照します。
    
 **pInstance**
  
> このオフラインのオブジェクトを一意に識別する GUID へのポインター。 このオフラインの他のオブジェクトからオブジェクトを明確に使用されます。
    
 **pParent**
  
> オフライン オブジェクトと元の親であるオフラインのオブジェクトへのポインターはこのオフラインのオブジェクトの継承を変更します。
    
 **pMAPISupport**
  
>  MAPI サポート オブジェクトがこのオブジェクトを使用することを識別します。 などのオフライン オブジェクトはオフラインで使用ストアの変更を追跡すると、オンラインの状態にし、これは、ストアは、オブジェクトをサポートします。 ただし、サポート オブジェクトを持たないオブジェクトのオフライン オブジェクトは、この場合、その NULL でもかまいません。 
    
 **pAggregateInfo**
  
> MAPIOFFLINE_AGGREGATEINFO 構造体へのポインター。 詳細については、 [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)を参照してください。
    
 **pConnectInfo**
  
> Null にする必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

