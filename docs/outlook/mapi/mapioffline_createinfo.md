---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429566"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造体は、 [hrcreateofflineobj](hrcreateofflineobj.md)と組み合わせて使用されます。
  
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

 **ulsize**
  
> 構造体のサイズ。
    
 **ulcreateflags**
  
> 0である必要があります。
    
 **pwszProfileName**
  
> プロファイルの名前を指定します。
    
 **ulcapabilities**
  
> 次の機能フラグのビットマスク。
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |オフラインオブジェクトがオフラインになることができる。  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |オフラインオブジェクトがオンラインになることができる。  <br/> |
   
 **pguid**
  
> 他のオフラインオブジェクトからこの種類のオフラインオブジェクトを一意に識別するために使用される GUID へのポインター。 GUID_GlobalState は、オブジェクトが親オブジェクトとして使用できるグローバルオフラインオブジェクトを参照します。
    
 **pinstance**
  
> このオフラインオブジェクトを一意に識別する GUID へのポインター。 これは、このオフラインオブジェクトを他のオブジェクトからあいまいにするために使用されます。
    
 **pparent**
  
> このオフラインオブジェクトの親であるオフラインオブジェクトへのポインター。このオフラインオブジェクトの変更内容が継承されます。
    
 **pMAPISupport**
  
>  このオフラインオブジェクトを使用する MAPI サポートオブジェクトを識別します。 たとえば、このオフラインオブジェクトを使用してストアのオフラインとオンラインの状態を追跡している場合は、ストアのサポートオブジェクトです。 ただし、これがサポートオブジェクトのないオブジェクトのオフラインオブジェクトである場合は、NULL にすることができます。 
    
 **pAggregateInfo**
  
> MAPIOFFLINE_AGGREGATEINFO 構造体へのポインター。 詳細については、「 [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)」を参照してください。
    
 **pconnectinfo**
  
> null である必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

