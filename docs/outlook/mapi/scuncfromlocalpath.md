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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803849"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

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

