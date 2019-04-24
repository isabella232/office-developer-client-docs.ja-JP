---
title: ifoldersupportgetsupportmask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350835"
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
  
> 読み上げフォルダーが共有をサポートしているかどうかを示すビットマスク。
    
 **FS_NONE**
  
> フォルダーが共有をサポートしていないことを示します。
    
 **FS_SUPPORTS_SHARING**
  
> フォルダーが共有をサポートしていることを示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが正常になされました。
    

