---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799988"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**適用対象**: Outlook 
  
ディスプレイ テーブルから組み込まれているダイアログ ボックスに表示される複数値の一覧について説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> 予約されています。0 にする必要があります。
    
 **ulMVPropTag**
  
> PT_MV_TSTRING の種類の複数値を持つプロパティのプロパティ タグです。
    
## <a name="remarks"></a>注釈

**DTBLMVLISTBOX**構造体では、項目の読み取り専用リストを持つ標準的な複数値を持つリストについて説明します。 標準的な複数値リストを使用すると、すぐに値が表示されます。 
  
データが表示される**ulMVPropTag**のメンバーで識別されるプロパティに由来します。 ディスプレイ テーブルに関連付けられているプロパティのインターフェイスから参照する必要はありません。 また、ユーザーがこれらの種類のリストから項目を選択することができないため、データはプロパティのインターフェイスに書き込まれません。 
  
複数値リストの複数値を持つ文字列のプロパティだけがサポートされて他の複数値を持つプロパティの型はサポートされていません。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

