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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800986"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**適用されます**: Outlook 
  
ストアのサポートに関する情報を取得は、指定されたセレクターに基づいています。
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parameters

 *mscapSelector* 
  
> [in]セレクターを取得する機能を示します。
    
## <a name="return-value"></a>�߂�l

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> 既定以外のストア内のフォルダーのホーム ページをサポートします。 これは*mscapSelector*で**MSCAP_SEL_FOLDER**が指定されている場合に返されます。 
    
MSCAP_RES_ANNOTATION
  
> 制限に無効なプロパティなどのすべての無効な引数が含まれている場合、ストアは無効な引数を無視し、有効な引数だけを処理します。 これは*mscapSelector*で**MSCAP_SEL_RESTRICTION**が指定されている場合に返されます。 
    
NULL
  
> ストアは、指定されたセレクターに基づくすべての機能をサポートしていません。
    

