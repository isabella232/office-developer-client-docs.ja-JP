---
title: '[Layer Membership] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2080
ms.localizationpriority: medium
ms.assetid: 7fb1d8a1-8892-f489-2f58-0008b5b750f5
description: 図形が割り当てられる各レイヤーを一覧表示する行を格納します。
ms.openlocfilehash: eed980a8a901ca66251ef7d326272404b3047933
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554495"
---
# <a name="layer-membership-section"></a>[Layer Membership] セクション

図形が割り当てられる各レイヤーを一覧表示する行を格納します。
  
## <a name="remarks"></a>注釈

レイヤーの割り当ては、ページ上にあるレイヤーの一覧のインデックスとして表示されます。レイヤーのインデックスは、[**レイヤー プロパティ**] ダイアログ ボックスに表示されるレイヤーの順番に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。ダイアログ ボックスの最初の名前は、layer 0 です。2 番目は layer 1 で、以降続きます。
  
図形が複数のレイヤーに割り当てられている場合、各レイヤーのインデックスは、[Layer Membership] セルに、セミコロンで区切られて表示されます。
  
数式の [Layer Membership] セルの値を参照するには、LayerMember という名前 **を使用します**。
  

