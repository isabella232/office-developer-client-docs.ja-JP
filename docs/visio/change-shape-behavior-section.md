---
title: '[図形の動作の変更] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: 置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[図形の動作の変更] セクションのセルの値は、図形の置換操作時に読み込まれます。
ms.openlocfilehash: 4bc87c7ab77568b06ced5456c74f96c151322761
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577998"
---
# <a name="change-shape-behavior-section"></a>[図形の動作の変更] セクション

置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[**図形の動作の変更**] セクションのセルの値は、図形の置換操作時に読み込まれます。 
  
## <a name="remarks"></a>注釈

[**図形の動作の変更**] セクションのセルを設定することで、図形の置換操作時に、置換後の図形の一定のプロパティが変更されないようにできます。保護されていないプロパティは、この操作時に古い図形のローカルな図形値で更新されます。 
  
マスター シェイプの置換動作設定を変更するには、マスター シェイプを編集します ([シェイプ] ウィンドウで図形を右クリックし、[マスター シェイプの編集] をポイントし、[マスター シェイプの編集] をクリックします)、マスター シェイプシートの[ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md) [、ReplaceLockFormat、ReplaceLockShapeData、](replacelockformat-cell-change-shape-behavior-section.md)[および ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md)セルの値を変更します。  [](replacelockshapedata-cell-change-shape-behavior-section.md) 
  
> [!NOTE]
> Microsoft Visio 2013 の組み込みのステンシルに含まれる図形の図形置換動作を変更することはできません。 組み込みの Visio図形の図形置換動作を変更するには、新しいステンシルを作成し、変更する図形を新しいステンシルに追加します。 
  

