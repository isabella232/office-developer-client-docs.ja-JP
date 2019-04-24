---
title: '[User-defined Cells] 行 ([User-defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: ソリューションでのユーザー定義のセルに関する、値と説明プロンプトを格納します。図形には、ユーザー定義の [Value]/[Prompt] セルの各組み合わせに対して 1 つの [User-defined Cells] 行があります。
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337185"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>[User-defined Cells] 行 ([User-defined Cells] セクション)

ソリューションでのユーザー定義のセルに関する、値と説明プロンプトを格納します。図形には、ユーザー定義の [Value]/[Prompt] セルの各組み合わせに対して 1 つの [User-defined Cells] 行があります。
  
[User-defined Cells] 行の名前は User. 次のセルに*名前*とが含まれます。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[値](value-cell-user-defined-cells-section.md) <br/> |対応するユーザー定義のセルの値を指定します。  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。  <br/> |
   
## <a name="remarks"></a>解説

ユーザー定義のセルは、他のセルやアドオンによって参照される、数式または定数の入力に使用できます。ユーザー定義のセルの値には可搬性があります。たとえば、ある図形が持つユーザー定義のセルを別の図形が参照していて、その図形を、同じユーザー定義のセルを持たない図形にコピーした場合、ユーザー定義のセルがコピー先の図形に追加されます。
  
 必要に応じて [User.  必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。 既存の [User-defined Cells] セクションに行を追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルを行名で参照できます。これは、シェイプシートウィンドウに赤いテキストで表示されます。 わかりやすい名前をユーザーに割り当てることができます。 [*名前*] 行をクリックし、「 *offset* 」などの名前を入力します。たとえば、行名のユーザーオフセットを作成します。 その後、ユーザーの Offset を使用して [prompt] セルを参照することができます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

