---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299518"
---
# <a name="guid"></a>GUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
グローバル一意識別子 (GUID) を記述します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiguid. .h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

 **Data1**
  
> 符号なしの長整数型 (long) のデータ値。
    
 **Data2**
  
> 符号なし short 整数型のデータ値。
    
 **Data3**
  
> 符号なし short 整数型のデータ値。
    
 **Data4**
  
> 符号なしの文字の配列。
    
## <a name="remarks"></a>解説

 **GUID**構造は、次のように MAPI で使用されます。 
  
- [MAPIUID](mapiuid.md)構造で、サービスプロバイダーを一意に識別します。 
    
- インターフェイス識別子の場合。
    
- プロパティの名前付きプロパティのセット。 
    
メッセージストアプロバイダーとアドレス帳プロバイダーは、 **MAPIUID**構造で使用する**GUID**構造を生成します。 結果の**MAPIUID**を[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)に渡すことにより、これらのサービスプロバイダーは、一意の識別子を MAPI に通知します。
  
また、Microsoft リモートプロシージャコール (RPC) およびオブジェクト記述言語 (ODL) の実装でも使用されます。 これらの使用の詳細については、「 *Microsoft RPC プログラマーズガイドとリファレンス*」、「 *ole プログラマーズリファレンス*」、および「 *ole*、 *Second Edition* 」を参照してください。 
  
**GUID**構造は、 *Win32 プログラマーズリファレンス*で定義されています。 mapi 内で使用される**GUID**構造の特定の値は、mapi ヘッダーファイルの mapiguid で定義されます。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)


[MAPI の構造](mapi-structures.md)

