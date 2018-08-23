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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2f5f4d50b085c437d1caab5f70dcb741afe090bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800069"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**適用対象**: Outlook 
  
[エントリ ID](entryid.md)の構造体と構造体**エントリ ID**のサイズを指定するバイト数です。 
  
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
  
> **AbEntry**メンバーのバイト数をカウントします。 
    
 **abEntry**
  
> フラグ、およびバイナリ データの配列を含む完全なエントリの識別子です。
    
## <a name="remarks"></a>注釈

**FLATENTRY**構造体では、[エントリ ID](entryid.md)の構造が似ています。 ただし、これにはいくつか相違点があります。 
  
- エントリ識別子のサイズを格納する**FLATENTRY**構造体**エントリ ID**はありません。 
    
- **FLATENTRY**構造体は、エントリの識別子の残りの部分と一緒にフラグ データを格納します。**エントリ ID**を格納するとは別にします。 
    
- エントリ識別子をファイルに保存またはバイトのストリームに渡すことが、**エントリ ID**の構造体は、 [IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドと次の**OpenEntry**メソッドで使用する**FLATENTRY**構造体が使用される: [IABLogon:: OpenEntry](iablogon-openentry.md)、[アドレス帳コンテナー](iaddrbook-openentry.md)、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、 [IMAPISession::OpenEntry](imapisession-openentry.md)、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、 [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- エントリ識別子をファイルに格納するバイトのストリームに渡すことは、 **FLATENTRY**構造体が使用されます。 **エントリ ID**の構造体を使用すると、ディスク上のエントリ id を格納します。 
    
## <a name="see-also"></a>関連項目



[エントリ ID](entryid.md)


[MAPI の構造](mapi-structures.md)

