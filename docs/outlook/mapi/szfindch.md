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
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804074"
---
# <a name="szfindch"></a>SzFindCh
 
**適用対象**: Outlook 
  
Null で終わる文字列内の文字の最初の出現箇所を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>パラメーター

_lpsz_
  
> [in]検索する null で終わる文字列へのポインター。 
    
_ch_
  
> [in]検索する文字。
    
## <a name="return-value"></a>戻り値

**SzFindCh**は、最初に見つかった文字列の文字へのポインターを返します。 文字が、文字列のどこにでも発生しない場合、または_lpsz_パラメーターが NULL の場合は、NULL 値が返されます。 
  
## <a name="remarks"></a>注釈

**SzFindCh**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。 Unicode と DBCS の形式での検索がサポートされています。 
  

