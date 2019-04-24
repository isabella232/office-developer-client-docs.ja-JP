---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317438"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したセレクターに基づいてストアがサポートできる内容に関する情報を取得します。
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>パラメーター

 *getcapabilities* 
  
> 順番返す機能を示すセレクター。
    
## <a name="return-value"></a>戻り値

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> 既定以外のストアでのフォルダー homepages のサポート。 これは、 **MSCAP_SEL_FOLDER**が*getcapabilities*で指定されている場合に返されることがあります。 
    
MSCAP_RES_ANNOTATION
  
> 無効なプロパティなどの無効な引数が制限に含まれている場合、ストアは無効な引数を無視し、有効な引数のみを処理します。 これは、 **MSCAP_SEL_RESTRICTION**が*getcapabilities*で指定されている場合に返されることがあります。 
    
NULL
  
> ストアは、指定されたセレクターに基づく機能をサポートしていません。
    

