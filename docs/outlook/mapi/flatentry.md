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
  
[ENTRYID 構造体に、ENTRYID](entryid.md)構造体のサイズを指定するバイト数 **を加えた値を指定** します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[cbFLATENTRY](cbflatentry.md)、 [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> **abEntry メンバーのバイト数**。 
    
 **abEntry**
  
> フラグとバイナリ データの配列を含む完全なエントリ識別子。
    
## <a name="remarks"></a>注釈

**FLATENTRY 構造体は** [ENTRYID 構造に似](entryid.md)ている。 ただし、いくつかの違いがあります。 
  
- **FLATENTRY 構造体** は、エントリ識別子のサイズを格納します。**ENTRYID** は使用しない。 
    
- **FLATENTRY 構造体は**、残りのエントリ識別子と共にフラグ データを格納します。**ENTRYID は** それらを個別に格納します。 
    
- **FLATENTRY** 構造体は、エントリ識別子をファイルに格納したり、バイト ストリームで渡したりするために使用しますが **、ENTRYID** 構造体は [IMAPIProp](imapipropiunknown.md)インターフェイス メソッドと次の **OpenEntry** メソッドによって使用されます [。IABLogon::OpenEntry](iablogon-openentry.md) [、IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- **FLATENTRY 構造体は**、エントリ識別子をファイルに格納したり、バイト ストリームで渡したりするために使用されます。 ENTRYID **構造体は** 、エントリ識別子をディスクに格納するために使用されます。 
    
## <a name="see-also"></a>関連項目



[ENTRYID](entryid.md)


[MAPI の構造](mapi-structures.md)

