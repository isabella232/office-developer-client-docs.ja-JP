---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411681"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前付きプロパティについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a>メンバー

 **lpguid**
  
> 特定のプロパティセットを定義する[GUID](guid.md)構造体へのポインター。このメンバーを NULL にすることはできません。 有効な値は以下のとおりです。 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
クライアント定義の値
  
> 
    
 **ulkind**
  
> **Kind**メンバー内の値の種類を説明する値。 有効な値は以下のとおりです。 
    
MNID_ID 
  
> **Kind**メンバーには、プロパティ名を表す整数値が含まれています。 
    
MNID_STRING 
  
> **Kind**メンバーには、プロパティ名を表す Unicode 文字の文字列が含まれています。 
    
 **Kind**
  
> 名前付きプロパティの名前を説明する共用体。 この名前は、 **lID**に格納された整数値、または**lpwstrname**に格納されている Unicode 文字列のいずれかになります。
    
## <a name="remarks"></a>注釈

**mapinameid**構造は、0x8000 を超える識別子を持つ名前付きプロパティのプロパティを記述するために使用されます。 プロパティセットは、名前付きプロパティという重要な部分です。 たとえば、PS_PUBLIC_STRINGS や PS_ROUTING_ADDRTYPE は、MAPI によって定義されたプロパティセットです。 
  
名前付きプロパティを使用すると、クライアントは、MAPI で定義されたプロパティ識別子の範囲で利用できない、より大きな名前空間でカスタムプロパティを定義できます。 プロパティの名前を使用してプロパティの値を直接取得することはできません。最初に、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを使用して、プロパティ識別子にマップする必要があります。 メッセージなどの特定のオブジェクトの場合、MAPI はカスタムプロパティの一連のプロパティ識別子を予約します。 そのため、これらのオブジェクトの場合、クライアントは名前付きプロパティを使用する必要がなく、関連するオーバーヘッドを保存できます。 
  
名前付きプロパティの詳細については、「[名前付きプロパティ](mapi-named-properties.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI の構造](mapi-structures.md)

