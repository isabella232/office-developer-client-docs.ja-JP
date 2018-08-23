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
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567854"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
共有フォルダーのサポートに関する情報を取得します。
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>パラメーター

 _pdwSupportMask_
  
> [out]フォルダーが共有をサポートしているかを示すビットマスクです。
    
 **FS_NONE**
  
> フォルダーを共有するサポートしていないことを示します。
    
 **FS_SUPPORTS_SHARING**
  
> 共有フォルダーをサポートしていることを示します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが正常になされました。
    

