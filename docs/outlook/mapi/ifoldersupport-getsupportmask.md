---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f337f93393766d6a456d5659b8f1cee13d23a299
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600961"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの共有のサポートに関する情報を取得します。
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>パラメーター

 _pdwSupportMask_
  
> [out]フォルダーが共有をサポートするかどうかを示すビットマスク。
    
 **FS_NONE**
  
> フォルダーが共有をサポートしていないかどうかを示します。
    
 **FS_SUPPORTS_SHARING**
  
> フォルダーが共有をサポートしています。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが正常になされました。
    

