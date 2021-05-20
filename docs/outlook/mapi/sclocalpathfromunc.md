---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432234"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定された汎用名前付け規則 (UNC) パスに対応するローカル パスを検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>パラメーター

 _szUNC_
  
> [in]ファイルまたはディレクトリの \\ _[server_] \[ _share_] \[ _パス_] 形式のパス。
    
 _szLocal_
  
> [out]szUNC パラメーターと同じファイルまたはディレクトリの形式 [ _drive:_] path ] の \[ パス。  
    
 _cchLocal_
  
> [in]出力文字列のバッファーのサイズ。
    
## <a name="return-value"></a>戻り値

S_OK
  
> ローカル パスが正常に見つからされました。
    
MAPI_E_TOO_BIG
  
>  _szLocal は_ 、結果を保持するのに十分な大きさではなかった。 
    
S_FALSE
  
> UNC 文字列は既にローカル パスでした。
    
MAPI_E_NOT_FOUND
  
> ローカル パスが見つかりませんでした。
    
## <a name="see-also"></a>関連項目



[ScUNCFromLocalPath](scuncfromlocalpath.md)

