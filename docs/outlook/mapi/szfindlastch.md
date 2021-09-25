---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c8d18b39b417e7cf2b0df6e0e271dd432ba9348
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566340"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
null 終端文字列内の文字が最後に出現した文字列を検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh** は、文字列内の文字の最後の出現位置へのポインターを返します。 文字列内の任意の場所で文字が発生しない場合、または  _lpsz_ パラメーターが NULL の場合は、NULL の値が返されます。 
  
## <a name="remarks"></a>注釈

**SzFindLastCh** 関数は完全一致のみを検索します。大文字と小文字の違いには敏感です。 Unicode 形式と DBCS 形式の検索がサポートされています。 
  

