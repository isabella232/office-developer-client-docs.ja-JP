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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345242"
---
# <a name="szfindch"></a>SzFindCh
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
null で終了する文字列内で最初に見つかった文字を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>パラメーター

_lpsz_
  
> 順番検索する null で終わる文字列へのポインター。 
    
_焦げ_
  
> 順番検索する文字を指定します。
    
## <a name="return-value"></a>戻り値

**szfindch**は、文字列内で最初に見つかった文字へのポインターを返します。 文字が文字列の任意の場所に出現しない場合、または_lpsz_パラメーターが null の場合は、null 値が返されます。 
  
## <a name="remarks"></a>解説

**szfindch**関数は、完全一致のみを検索します。大文字と小文字は区別されます。 Unicode および DBCS 形式での検索がサポートされています。 
  

