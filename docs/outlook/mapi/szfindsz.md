---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804078"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**適用対象**: Outlook 
  
Null で終わる文字列で、null で終わる文字列の最初に見つかった位置を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]検索する null で終わる文字列へのポインター。 _Lpsz_パラメーターは、65536 文字を超えない必要があります。 
    
 _lpszKey_
  
> [in]検索する null で終わる文字列へのポインター。 _LpszKey_パラメーターは、65536 文字を超えない必要があります。 
    
## <a name="return-value"></a>戻り値

 **SzFindSz**は、最初に見つかった文字列の部分文字列の最初の文字へのポインターを返します。 部分文字列が発生しない場合任意の場所で、文字列_lpsz_より大きい場合は_lpszKey_またはどちらかのパラメーターが NULL の場合、NULL 値が返されます。 
  
## <a name="remarks"></a>注釈

**SzFindSz**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。 Unicode と DBCS の形式での検索がサポートされています。 両方のパラメーターの長さの制限は、文字数、バイト数ではありませんが。 
  

