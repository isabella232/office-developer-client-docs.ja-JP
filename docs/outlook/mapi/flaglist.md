---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800074"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**適用されます**: Outlook 
  
名前解決の処理中にアドレス エントリのステータスを示すために使用されるフラグの一覧が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>メンバー

 **cFlags**
  
> MAPI 定義のフラグを一覧の数です。
    
 **ulFlags**
  
> 受信者の名前解決操作のステータスを提供するフラグの配列。 次のフラグを設定することができます。
    
MAPI_AMBIGUOUS 
  
> 受信者が解決されていませんが、エントリの一意の識別子です。 他のアドレス帳コンテナーは、この受信者を解決するのにはいけません。 
    
MAPI_RESOLVED 
  
> 受信者は、エントリの一意の識別子に解決されました。 他のアドレス帳コンテナーは、この受信者を解決するのにはいけません。 
    
MAPI_UNRESOLVED 
  
> エントリは解決されていません。 他のアドレス帳コンテナーは、この受信者を解決するようにしてください。
    
## <a name="remarks"></a>備考

**FLAGLIST**構造体は、 [IABContainer::ResolveNames](iabcontainer-resolvenames.md)のパラメーターとして使用されます。 各受信者を解決するのには、 [ADRLIST](adrlist.md)構造体に含まれます。 アドレス帳コンテナーは、各受信者を解決しようとすると、 **FLAGLIST**構造体に対応するエントリに適切なフラグを設定します。 **ADRLIST**構造体のエントリと同じ順序では、 **FLAGLIST**構造体のエントリのすべてです。 これにより、フラグの設定を受信者に関連付けるには簡単です。 
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI の構造](mapi-structures.md)

