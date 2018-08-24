---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590107"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
汎用名前付け規則 (UNC) パスに対応する指定されたローカル パスを検索します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>パラメーター

 _szLocal_
  
> [in]パスの形式で [_ドライブ:_]\[ _のパス_] ファイルまたはディレクトリの。
    
 _szUNC_
  
> [out]形式のパス\\[_サーバー_]\[ _を共有_]\[ _パス_] の同じファイルまたはディレクトリの場合、 _szLocal_パラメーターとします。 
    
 _cchUNC_
  
> [in]出力文字列のバッファーのサイズです。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> UNC パスに対応するでは、正常に配置されました。
    
MAPI_E_INVALID_PARAMETER
  
> 1 つ以上のパラメーターが無効です。
    
MAPI_E_TOO_BIG
  
>  _szUNC_は、結果を保持するのに十分な大きさでした。 
    
S_FALSE
  
> ローカル パスは、UNC 文字列では既にいました。
    
## <a name="see-also"></a>関連項目



[ScLocalPathFromUNC](sclocalpathfromunc.md)

