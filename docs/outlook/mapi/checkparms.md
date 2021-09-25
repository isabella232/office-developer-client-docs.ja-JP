---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c7fc3875abc26e642b6ae1e5bf4c96c3c017aad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556862"
---
# <a name="checkparms"></a>CheckParms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI によって呼び出されるサービス プロバイダー メソッドのデバッグ パラメーターを検証する内部関数を呼び出します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _eMethod_
  
> [in]列挙で検証するメソッドを指定します。 
    
 _First_
  
> [in]スタックの最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

[ValidateParms](validateparms.md)マクロと [UlValidateParms](ulvalidateparms.md)マクロとは対照的に **、CheckParms** マクロは完全なパラメーター検証を実行しません。 MAPI とサービス プロバイダーの間で渡されるパラメーターは正しいと見なされます。 **そのため、CheckParms は** デバッグ検証のみを実行します。 
  

