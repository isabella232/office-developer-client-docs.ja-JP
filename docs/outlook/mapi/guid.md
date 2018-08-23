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
ms.openlocfilehash: 94bafdf0ca84fa31a7df2f022265d5d5d1a99a37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577696"
---
# <a name="guid"></a>GUID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
グローバル一意識別子 (GUID) をについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiguid.h  <br/> |
   
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
  
> 符号なし長整数型のデータの値の場合です。
    
 **Data2**
  
> 符号なし短整数データの値。
    
 **Data3**
  
> 符号なし短整数データの値。
    
 **Data4**
  
> 符号なしの文字の配列。
    
## <a name="remarks"></a>注釈

 **GUID**構造体は、次のようの MAPI で使用されます。 
  
- [MAPIUID](mapiuid.md)構造体でサービス プロバイダーを一意に識別します。 
    
- インターフェイス識別子です。
    
- プロパティには、名前付きプロパティの名前を設定します。 
    
メッセージ ストアとアドレス帳プロバイダーは、 **MAPIUID**構造体で使用する**GUID**構造体を生成します。 結果として得られる**MAPIUID**を[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)に渡すことによっては、これらのサービス プロバイダーは、その一意の識別子の MAPI を通知します。
  
また、Microsoft リモート プロシージャ コール (RPC) およびオブジェクトの説明言語 (ODL) の実装に使用されます。 これらの使用の詳細については、の*Microsoft RPC プログラマーズ ガイドと参照*、 *OLE プログラマ リファレンス*、および*内部 OLE*、*第 2 版*を参照してください。 
  
**GUID**構造体は、 *Win32 プログラマーズ リファレンス*で定義されます。 MAPI ヘッダー ファイル Mapiguid.h には、MAPI 内で使用する**GUID**構造体の特定の値が定義されています。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)


[MAPI の構造](mapi-structures.md)

