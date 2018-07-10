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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801498"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**適用されます**: Outlook 
  
名前付きプロパティをについて説明します。 
  
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
  
> 特定のプロパティを定義する[GUID](guid.md)構造体へのポインターを設定します。このメンバーは NULL にできません。 有効な値は以下のとおりです。 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
クライアント定義の値
  
> 
    
 **ulKind**
  
> **種類**のメンバーの値の種類を示す数値です。 有効な値は以下のとおりです。 
    
MNID_ID 
  
> **種類**のメンバーには、プロパティ名を表す整数値が含まれています。 
    
MNID_STRING 
  
> **種類**のメンバーには、プロパティ名を表す Unicode 文字の文字列が含まれています。 
    
 **種類**
  
> 共用体の名前付きプロパティの名前を記述します。 名前は**カバー**に格納されている整数値、または**lpwstrName**に格納されている Unicode 文字の文字列のいずれかにできます。
    
## <a name="remarks"></a>備考

**MAPINAMEID**構造体を使用して、0x8000 以上の識別子を持つ名前付きプロパティのプロパティを記述します。 プロパティ セットは、重要な部分の名前付きプロパティです。 たとえば PS_PUBLIC_STRINGS または PS_ROUTING_ADDRTYPE は、MAPI によって定義されているプロパティのセットです。 
  
名前付きプロパティは、MAPI 定義のプロパティの識別子の範囲で利用できるよりも大規模な名前空間のカスタム プロパティを定義するのにはクライアントを有効にします。 プロパティの値を直接取得するプロパティ名を使用することはできません。最初にマップされるプロパティ識別子[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用します。 メッセージなど、特定のオブジェクトには、MAPI は、カスタム プロパティのプロパティ id の範囲を予約します。 したがって、これらのオブジェクトのクライアント名前付きプロパティを使用することはありません、できれば、それに関連付けられたオーバーヘッドです。 
  
名前付きプロパティの詳細については、[名前付きプロパティ](mapi-named-properties.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI の構造](mapi-structures.md)
