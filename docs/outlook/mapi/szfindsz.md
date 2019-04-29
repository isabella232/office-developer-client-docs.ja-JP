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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435223"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
null で終わる部分文字列が、null で終了する文字列内で最初に見つかった部分を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> 順番検索する null で終わる文字列へのポインター。 _lpsz_パラメーターは、65536文字以下にする必要があります。 
    
 _lpszkey_
  
> 順番検索する null で終わるサブ文字列へのポインター。 _lpszkey_パラメーターは、65536文字を超えることはできません。 
    
## <a name="return-value"></a>戻り値

 **szfindsz**は、文字列内で最初に見つかった部分文字列の最初の文字へのポインターを返します。 substring_キー_が_lpsz_より大きい場合、またはいずれかのパラメーターが null の場合、文字列内の任意の場所にサブ文字列が含まれていない場合は、null 値が返されます。 
  
## <a name="remarks"></a>注釈

**szfindsz**関数は、完全一致のみを検索します。大文字と小文字は区別されます。 Unicode および DBCS 形式での検索はサポートされています。 両方のパラメーターの長さ制限は、文字である必要があり、必ずしもバイトではありません。 
  

