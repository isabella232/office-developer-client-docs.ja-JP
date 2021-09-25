---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4cb47ae7f880985c625e61a4ca6fc02ba1477441
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591193"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定されたローカル パスに対応する汎用名前付け規則 (UNC) パスを検索します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>パラメーター

 _szLocal_
  
> [in]ファイルまたはディレクトリの形式 [ _drive:_] \[ _path_] のパス。
    
 _szUNC_
  
> [out]szLocal パラメーターと同じファイルまたはディレクトリの [サーバー ] 共有 ] パス \\ の形式 \[  \[ _のパス_。 
    
 _cchUNC_
  
> [in]出力文字列のバッファーのサイズ。
    
## <a name="return-value"></a>戻り値

S_OK
  
> UNC パスの対応するパスが正常に見つからされました。
    
MAPI_E_INVALID_PARAMETER
  
> 1 つ以上のパラメーターが無効です。
    
MAPI_E_TOO_BIG
  
>  _szUNC_ は、結果を保持するのに十分な大きさではなかった。 
    
S_FALSE
  
> ローカル パスは既に UNC 文字列でした。
    
## <a name="see-also"></a>関連項目



[ScLocalPathFromUNC](sclocalpathfromunc.md)

