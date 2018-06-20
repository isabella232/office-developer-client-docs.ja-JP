---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a1530443600df7cb73ff27d5cfbeab46f81bc53c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803923"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**適用されます**: Outlook 
  
タブ付きページのコントロール、指定した長さのラベル、ヘルプ ファイルのエントリを指定された長さの記述するため[DTBLPAGE](dtblpage.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> [ページ] タブのラベルの長さです。
    
_n1_
  
> タブ ページ コントロールを使用するヘルプ ファイルを識別する、Mapisvc.inf ファイルに表示されるエントリの長さです。
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>備考

**SizedDtblPage**マクロを使用して、ヘルプ ファイルのエントリと関連付けられているラベルの文字数がわかっている場合は、タブ付きページのコントロールを定義できます。 新しい構造体は、次のメンバーで作成されます。 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

**DTBLPAGE**構造体のポインターとして、 **SizedDtblPage**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>関連項目

- [DTBLPAGE](dtblpage.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

