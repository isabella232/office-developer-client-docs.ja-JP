---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68dbae7a6d2e7cc458b3b7ed71ddd06bab7fb1f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584094"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前付きプロパティについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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
  
> 特定のプロパティ セットを定義する [GUID](guid.md) 構造へのポインター。このメンバーを NULL にすることはできません。 有効な値は以下のとおりです。 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
クライアント定義の値
  
> 
    
 **ulKind**
  
> Kind メンバーの値の種類を表 **す** 値。 有効な値は以下のとおりです。 
    
MNID_ID 
  
> **Kind メンバー** には、プロパティ名を表す整数値が含まれる。 
    
MNID_STRING 
  
> **Kind メンバーには**、プロパティ名を表す Unicode 文字文字列が含まれます。 
    
 **Kind**
  
> 名前付きプロパティの名前を表す共用体。 名前には **、lID** に格納された整数値、または **lpwstrName** に格納された Unicode 文字文字列のいずれかを指定できます。
    
## <a name="remarks"></a>注釈

**MAPINAMEID 構造体は**、名前の付いたプロパティを記述するために使用されます。このプロパティの識別子は、0x8000。 プロパティ セットは、名前付きプロパティの重要な部分です。 たとえば、mapi PS_PUBLIC_STRINGSまたはPS_ROUTING_ADDRTYPEプロパティ セットを指定します。 
  
名前付きプロパティを使用すると、MAPI で定義されたプロパティ識別子の範囲よりも大きな名前空間でカスタム プロパティを定義できます。 プロパティ名を使用してプロパティ値を直接取得することはできません。まず [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを使用してプロパティ識別子にマップする必要があります。 メッセージなどの特定のオブジェクトに対して、MAPI はカスタム プロパティのプロパティ識別子の範囲を予約します。 したがって、これらのオブジェクトの場合、クライアントは名前付きプロパティを使用する必要はありません。関連するオーバーヘッドを保存できます。 
  
名前付きプロパティの詳細については、「名前付きプロパティ [」を参照してください](mapi-named-properties.md)。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI の構造](mapi-structures.md)

