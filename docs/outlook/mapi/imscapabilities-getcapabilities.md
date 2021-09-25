---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b4f0b47aa1c8f79db886a0eba5f146404fd9031b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630538"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したセレクターに基づいてストアでサポートできる機能に関する情報を取得します。
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>パラメーター

 *mscapSelector* 
  
> [in]返す機能を示すセレクター。
    
## <a name="return-value"></a>戻り値

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> 既定以外のストアでのフォルダーのホームページのサポート。 これは *、mscapSelector* **で** MSCAP_SEL_FOLDER指定されている場合に返されます。 
    
MSCAP_RES_ANNOTATION
  
> 制限に無効なプロパティなどの無効な引数が含まれている場合、ストアは無効な引数を無視し、有効な引数のみを処理します。 これは、mscapSelector **MSCAP_SEL_RESTRICTION指定** されている場合  *に返されます*  。 
    
NULL
  
> ストアでは、指定されたセレクターに基づく機能はサポートされていません。
    

