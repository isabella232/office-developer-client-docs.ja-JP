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
ms.openlocfilehash: eeeff110e5de592d491865079adfa187e5dfa194
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570878"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  

