---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 464c6ed3ce2c56339d38ec21648922618d1a4ad9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619646"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
null 終端文字列内の null 終端部分文字列の最初に出現する部分文字列を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]検索する null 終端文字列へのポインター。 _lpsz パラメーター_ は、65536 文字を超えることはできません。 
    
 _lpszKey_
  
> [in]検索する null 終端部分文字列へのポインター。 _lpszKey パラメーター_ は、65536 文字を超えることはできません。 
    
## <a name="return-value"></a>戻り値

 **SzFindSz** は、文字列内の部分文字列の最初に出現する文字の最初の文字へのポインターを返します。 文字列内の任意の場所で部分文字列が発生しない場合  _、lpszKey_ が  _lpsz_ より大きい場合、またはいずれかのパラメーターが NULL の場合は、NULL の値が返されます。 
  
## <a name="remarks"></a>注釈

**SzFindSz** 関数は完全一致のみを検索します。大文字と小文字の違いには敏感です。 Unicode 形式と DBCS 形式の検索がサポートされています。 両方のパラメーターの長さの制限は文字で、必ずしもバイトではありません。 
  

