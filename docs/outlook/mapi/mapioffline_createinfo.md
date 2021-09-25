---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e31e4c1f81541bcc04bfc41209f2ac5f8ea4f42
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592103"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造は [、HrCreateOfflineObj で使用されます](hrcreateofflineobj.md)。
  
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
  
> 構造体のサイズ。
    
 **ulCreateFlags**
  
> 0 である必要があります。
    
 **pwszProfileName**
  
> プロファイルの名前を指定します。
    
 **ulCapabilities**
  
> 次の機能フラグのビット マスク。
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |オフライン オブジェクトはオフラインにできます。  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |オフライン オブジェクトはオンラインにできます。  <br/> |
   
 **pGUID**
  
> 他のオフライン オブジェクトからこの種類のオフライン オブジェクトを一意に識別するために使用される GUID へのポインター。 GUID_GlobalStateは、オブジェクトが親オブジェクトとして使用できるグローバル オフライン オブジェクトを参照します。
    
 **pInstance**
  
> このオフライン オブジェクトを一意に識別する GUID へのポインター。 このオフライン オブジェクトを他のオブジェクトからあいまいに解除するために使用されます。
    
 **pParent**
  
> このオフライン オブジェクトの親であり、このオフライン オブジェクトが継承する変更を持つオフライン オブジェクトへのポインター。
    
 **pMAPISupport**
  
>  このオフライン オブジェクトを使用する MAPI サポート オブジェクトを識別します。 たとえば、このオフライン オブジェクトを使用してストアのオフライン状態とオンライン状態を追跡する場合、これが stores サポート オブジェクトです。 ただし、サポート オブジェクトがないオブジェクトのオフライン オブジェクトの場合は、NULL を指定できます。 
    
 **pAggregateInfo**
  
> 構造体へのポインター MAPIOFFLINE_AGGREGATEINFOします。 詳細については、「MAPIOFFLINE_AGGREGATEINFO」 [を参照してください](mapioffline_aggregateinfo.md)。
    
 **pConnectInfo**
  
> null である必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

