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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336940"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前解決プロセス中にアドレスエントリの状態を示すために使用されるフラグの一覧が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Members

 **cFlags**
  
> リスト内の MAPI 定義フラグの数。
    
 **ulFlags**
  
> 受信者の名前解決操作の状態を提供するフラグの配列。 次のフラグを設定できます。
    
MAPI_AMBIGUOUS 
  
> 受信者は解決されましたが、一意のエントリ識別子には対応していません。 他のアドレス帳コンテナーは、この受信者の解決を試みてはなりません。 
    
MAPI_RESOLVED 
  
> 受信者が一意のエントリ識別子に解決されました。 他のアドレス帳コンテナーは、この受信者の解決を試みてはなりません。 
    
MAPI_UNRESOLVED 
  
> エントリは解決されていません。 他のアドレス帳コンテナーは、この受信者の解決を試みます。
    
## <a name="remarks"></a>解説

**flaglist**構造体は、 [IABContainer:: ResolveNames](iabcontainer-resolvenames.md)のパラメーターとして使用されます。 解決される各受信者は、 [adrlist](adrlist.md)構造に含まれています。 アドレス帳コンテナーは各受信者の解決を試みたときに、 **flaglist**構造の対応するエントリに適切なフラグを設定します。 **flaglist**構造体のすべてのエントリは、 **adrlist**構造内のエントリと同じ順序になっています。 これにより、フラグ設定を受信者に簡単に関連付けることができます。 
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI の構造](mapi-structures.md)

