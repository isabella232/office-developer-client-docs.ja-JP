---
title: '[LockVariation] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: eac661fd88e53fa42999ba5e1e23af8bc113e4bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573923"
---
# <a name="lockvariation-cell-protection-section"></a>[LockVariation] セル ([保護] セクション)

ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。
  
|||
|:-----|:-----|
|TRUE  <br/> |ページまたは図形に適用された現在のバリエーションは変更できません。  <br/> |
|FALSE  <br/> |ページまたは図形のバリエーションは変更できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockVariation**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockVariation  <br/> |
   
プログラムから、インデックスによって [**LockVariation**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockVariation** <br/> |
   

