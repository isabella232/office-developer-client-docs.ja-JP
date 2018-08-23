---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804076"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**適用対象**: Outlook 
  
最後に出現する、null で終わる文字列内の文字を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh**は、最後に見つかった文字列の文字へのポインターを返します。 文字が、文字列のどこにでも発生しない場合、または_lpsz_パラメーターが NULL の場合は、NULL 値が返されます。 
  
## <a name="remarks"></a>注釈

**SzFindLastCh**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。 Unicode と DBCS の形式での検索がサポートされています。 
  

