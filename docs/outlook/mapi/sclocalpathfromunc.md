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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803833"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**適用されます**: Outlook 
  
特定の汎用名前付け規則 (UNC) パスをローカル パスに対応するを検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Parameters

 _szUNC_
  
> [in]形式のパス\\[_サーバー_]\[ _を共有_]\[ _のパス_] ファイルまたはディレクトリの。
    
 _szLocal_
  
> [out]形式でパス [_ドライブ:_]\[ _のパス_] の同じファイルまたはディレクトリの場合、 _szUNC_パラメーターとします。 
    
 _cchLocal_
  
> [in]出力文字列のバッファーのサイズです。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> ローカル パスでは、正常に配置されました。
    
MAPI_E_TOO_BIG
  
>  _szLocal_は、結果を保持するのに十分な大きさでした。 
    
S_FALSE
  
> UNC 文字列は、ローカル パスでは既にいました。
    
MAPI_E_NOT_FOUND
  
> ローカル パスが見つかりませんでした。
    
## <a name="see-also"></a>関連項目



[ScUNCFromLocalPath](scuncfromlocalpath.md)

