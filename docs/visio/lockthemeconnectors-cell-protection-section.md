---
title: '[LockThemeConnectors] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: '[テーマのプロパティ] 行の [ConnectorsSchemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。'
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438408"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>[LockThemeConnectors] セル ([保護] セクション)

[**テーマのプロパティ**] 行の [**ConnectorsSchemeIndex**] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |シェイプシートを直接変更しない限り、[**ConnectorsSchemeIndex**] セルの現在の値は変更できません。  <br/> |
|FALSE  <br/> |[**ConnectorsSchemeIndex**] セルの現在の値は、UI を使用して変更できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeConnectors**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockthemeconnectors]  <br/> |
   
プログラムから、インデックスによって [**LockThemeConnectors**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeConnectors** <br/> |
   

