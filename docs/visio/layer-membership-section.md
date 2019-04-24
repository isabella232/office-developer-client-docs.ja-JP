---
title: '[Layer Membership] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2080
localization_priority: Normal
ms.assetid: 7fb1d8a1-8892-f489-2f58-0008b5b750f5
description: 図形が割り当てられる各レイヤーを一覧表示する行を格納します。
ms.openlocfilehash: e7e07ba14147abc8cdfd8b8544e4ee8f34b2be06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359011"
---
# <a name="layer-membership-section"></a>[Layer Membership] セクション

図形が割り当てられる各レイヤーを一覧表示する行を格納します。
  
## <a name="remarks"></a>解説

レイヤーの割り当ては、ページ上にあるレイヤーの一覧のインデックスとして表示されます。レイヤーのインデックスは、[**レイヤー プロパティ**] ダイアログ ボックスに表示されるレイヤーの順番に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。ダイアログ ボックスの最初の名前は、layer 0 です。2 番目は layer 1 で、以降続きます。
  
図形が複数のレイヤーに割り当てられている場合、各レイヤーのインデックスは、[Layer Membership] セルに、セミコロンで区切られて表示されます。
  
数式で [Layer Membership] セルの値を参照するには、名前**layer member**を使用します。
  

