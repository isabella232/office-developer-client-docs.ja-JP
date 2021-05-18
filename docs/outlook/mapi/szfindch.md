---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421943"
---
# <a name="szfindch"></a>SzFindCh
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
null 終端文字列内の文字の最初の出現箇所を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>パラメーター

_lpsz_
  
> [in]検索する null 終端文字列へのポインター。 
    
_ch_
  
> [in]検索する文字。
    
## <a name="return-value"></a>戻り値

**SzFindCh** は、文字列内の文字の最初の出現位置へのポインターを返します。 文字列内の任意の場所で文字が発生しない場合、または  _lpsz_ パラメーターが NULL の場合は、NULL の値が返されます。 
  
## <a name="remarks"></a>注釈

**SzFindCh** 関数は完全一致のみを検索します。大文字と小文字の違いには敏感です。 Unicode 形式と DBCS 形式の検索がサポートされています。 
  

