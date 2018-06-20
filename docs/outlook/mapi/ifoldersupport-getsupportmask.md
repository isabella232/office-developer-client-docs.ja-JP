---
title: IFolderSupportGetSupportMask
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800436"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**適用されます**: Outlook 
  
共有フォルダーのサポートに関する情報を取得します。
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parameters

 _pdwSupportMask_
  
> [out]フォルダーが共有をサポートしているかを示すビットマスクです。
    
 **FS_NONE**
  
> フォルダーを共有するサポートしていないことを示します。
    
 **FS_SUPPORTS_SHARING**
  
> 共有フォルダーをサポートしていることを示します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが正常になされました。
    

