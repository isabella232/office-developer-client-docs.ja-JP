---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8be044edc628143bc7f7a4a33caa1046f0a3e5e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561741"
---
# <a name="guid"></a>GUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
グローバル一意識別子 (GUID) について説明します。 
  
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

## <a name="members"></a>メンバー

 **Data1**
  
> 符号なし長整数データ値。
    
 **Data2**
  
> 符号なし短整数データ値。
    
 **Data3**
  
> 符号なし短整数データ値。
    
 **Data4**
  
> 符号なし文字の配列。
    
## <a name="remarks"></a>注釈

 **GUID** 構造は、次のように MAPI で使用されます。 
  
- サービス プロバイダーを一意に識別する [MAPIUID](mapiuid.md) 構造。 
    
- インターフェイス識別子の場合。
    
- プロパティで、名前付きプロパティの名前を設定します。 
    
メッセージ ストアとアドレス帳プロバイダーは **、MAPIUID** 構造で使用する **GUID 構造を生成** します。 結果の **MAPIUID** を [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)に渡して、これらのサービス プロバイダーは MAPI に一意の識別子を通知します。
  
また、Microsoft リモート プロシージャ 呼び出し (RPC) およびオブジェクト記述言語 (ODL) の実装でも使用されます。 これらの使用の詳細については *、「Microsoft RPC プログラマ* ガイドとリファレンス」、OLEプログラマリファレンス *、Inside OLE 、Second* Edition を *参照してください*。 
  
**GUID 構造** は *、Win32 プログラマリファレンスで定義されています*。 MAPI 内で **使用される GUID** 構造体の特定の値は、MAPI ヘッダー ファイル Mapiguid.h で定義されます。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)


[MAPI の構造](mapi-structures.md)

