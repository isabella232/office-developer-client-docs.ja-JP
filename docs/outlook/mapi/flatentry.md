---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407243"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
entryid [](entryid.md)構造に加えて、 **entryid**構造体のサイズを指定するバイト数を指定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[cbFLATENTRY](cbflatentry.md)、 [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>メンバー

 **cb**
  
> **abentry**メンバーのバイト数。 
    
 **abentry**
  
> フラグとバイナリデータの配列を含む完全なエントリ識別子。
    
## <a name="remarks"></a>注釈

**FLATENTRY**構造体は、 [ENTRYID](entryid.md)構造に似ています。 ただし、次のような違いがあります。 
  
- **FLATENTRY**構造体は、エントリ識別子のサイズを格納します。**ENTRYID**は無効です。 
    
- **FLATENTRY**構造体は、フラグデータをエントリ id の残りの部分と一緒に格納します。**ENTRYID**は個別に格納します。 
    
- **FLATENTRY**構造体は、エントリ id をファイルに格納したり、バイトのストリームに渡したりするために使用されます。 **ENTRYID**構造は、 [imapiprop](imapipropiunknown.md)のインターフェイスメソッドと、次の**openentry**メソッドで使用されます。 IABLogon は次のようになります。 [: openentry](iablogon-openentry.md)、 [IAddrBook:: openentry](iaddrbook-openentry.md)、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)、 [imapisession:: openentry](imapisession-openentry.md)、 [imapisession:: openentry](imapisupport-openentry.md)、 [IMsgStore:: openentry](imsgstore-openentry.md)、 [IMSLogon:: openentry](imslogon-openentry.md)
    
- **FLATENTRY**構造体は、エントリ id をファイルに格納したり、バイトのストリームに渡したりするために使用されます。 **ENTRYID**構造体は、ディスクにエントリ識別子を格納するために使用されます。 
    
## <a name="see-also"></a>関連項目



[ENTRYID](entryid.md)


[MAPI の構造](mapi-structures.md)

