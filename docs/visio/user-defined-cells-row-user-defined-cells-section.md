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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420690"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>[User-defined Cells] 行 ([User-defined Cells] セクション)

ソリューションでのユーザー定義のセルに関する、値と説明プロンプトを格納します。図形には、ユーザー定義の [Value]/[Prompt] セルの各組み合わせに対して 1 つの [User-defined Cells] 行があります。
  
[User-defined Cells] 行の名前は User. *名前*  を指定し、次のセルを含む。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[値](value-cell-user-defined-cells-section.md) <br/> |対応するユーザー定義のセルの値を指定します。  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

ユーザー定義のセルは、他のセルやアドオンによって参照される、数式または定数の入力に使用できます。ユーザー定義のセルの値には可搬性があります。たとえば、ある図形が持つユーザー定義のセルを別の図形が参照していて、その図形を、同じユーザー定義のセルを持たない図形にコピーした場合、ユーザー定義のセルがコピー先の図形に追加されます。
  
 必要に応じて [User.  *必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。 既存の [User-defined Cells] セクションに行を追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルは行名で参照できます。これは、赤いテキストの ShapeSheet ウィンドウに表示されます。 意味のある名前を User に割り当てる。 *行*  名を指定し、行をクリックし  *、Offset*  などの名前を入力して、たとえば、行名 User.Offset を作成します。 その後、User.Offset.Prompt を使用して [プロンプト] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

