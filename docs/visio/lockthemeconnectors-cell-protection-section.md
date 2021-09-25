---
title: '[LockThemeConnectors] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: '[テーマのプロパティ] 行の [ConnectorsSchemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。'
ms.openlocfilehash: 3e1fd7571795bb5fea7cb4d0a5f8da091b5b7783
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554398"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>[LockThemeConnectors] セル ([保護] セクション)

[**テーマのプロパティ**] 行の [**ConnectorsSchemeIndex**] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |シェイプシートを直接変更しない限り、[**ConnectorsSchemeIndex**] セルの現在の値は変更できません。  <br/> |
|FALSE  <br/> |[**ConnectorsSchemeIndex**] セルの現在の値は、UI を使用して変更できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeConnectors**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockThemeConnectors  <br/> |
   
プログラムから、インデックスによって [**LockThemeConnectors**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeConnectors** <br/> |
   

