---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800048"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**適用されます**: Outlook 
  
2 つの MAPI 名前付きプロパティが同じかどうかを判断します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parameters

 _lpName1_
  
> [in]最初の名前付きプロパティを記述する[MAPINAMEID](mapinameid.md)構造体へのポインター。 
    
 _lpName2_
  
> [in]2 番目の名前付きプロパティを記述する**MAPINAMEID**構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

TRUE 
  
> 2 つのプロパティ名は、同じです。 
    
FALSE 
  
> 2 つのプロパティ名が等しくないです。
    
## <a name="remarks"></a>備考

**FEqualNames**関数は、 **MAPINAMEID**構造体は[GUID](guid.md)が含まれていて、複数の方法でプロパティ名自体を表すことができますので便利です。 つまり、バイナリの簡単な方法で 2 つの構造体を比較することはできません。 
  
テスト プロセスは、プロパティ名の文字列の大文字小文字を区別します。 
  

