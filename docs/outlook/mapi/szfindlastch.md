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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421257"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
null で終了する文字列内の文字が最後に出現する箇所を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **szfindlastch**は、文字列内の文字が最後に出現する位置へのポインターを返します。 文字が文字列の任意の場所に出現しない場合、または_lpsz_パラメーターが null の場合は、null 値が返されます。 
  
## <a name="remarks"></a>注釈

**szfindlastch**関数は、完全一致のみを検索します。大文字と小文字は区別されます。 Unicode および DBCS 形式での検索がサポートされています。 
  

