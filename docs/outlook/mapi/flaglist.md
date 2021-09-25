---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32789e57bebef3320e413fa67c6352dee43248ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614242"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前解決プロセス中のアドレス エントリの状態を示すために使用されるフラグの一覧が含まれる。
  
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
  
> リスト内の MAPI で定義されたフラグの数。
    
 **ulFlags**
  
> 受信者の名前解決操作の状態を提供するフラグの配列。 次のフラグを設定できます。
    
MAPI_AMBIGUOUS 
  
> 受信者は解決されましたが、一意のエントリ識別子には解決されません。 他のアドレス帳コンテナーは、この受信者の解決を試みる必要があります。 
    
MAPI_RESOLVED 
  
> 受信者が一意のエントリ識別子に解決されました。 他のアドレス帳コンテナーは、この受信者の解決を試みる必要があります。 
    
MAPI_UNRESOLVED 
  
> エントリが解決されていない。 他のアドレス帳コンテナーは、この受信者の解決を試みる必要があります。
    
## <a name="remarks"></a>注釈

**FLAGLIST 構造体** は [、IABContainer::ResolveNames のパラメーターとして使用されます](iabcontainer-resolvenames.md)。 解決する各受信者は [、ADRLIST 構造に含](adrlist.md) まれています。 アドレス帳コンテナーは、各受信者を解決しようとして **、FLAGLIST** 構造内の対応するエントリに適切なフラグを設定します。 **FLAGLIST** 構造体のすべてのエントリは **、ADRLIST** 構造体のエントリと同じ順序です。 これにより、フラグ設定を受信者に簡単に関連付けできます。 
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI の構造](mapi-structures.md)

