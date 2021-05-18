---
title: '[Smart Tags] 行 ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026926
localization_priority: Normal
ms.assetid: 065c6977-c737-a4f4-effa-0fd2c98e8bbf
description: 図形またはページに関連付けられた、単一のアクション タグの情報を格納します。 図形またはページには、各アクション タグに対して 1 つの [Smart Tags] 行があります。
ms.openlocfilehash: 1c1591fd2d2cacfbfb350a542e6601cb2f6fbfd6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404709"
---
# <a name="smart-tags-row-action-tags-section"></a>[Smart Tags] 行 ([Action Tags] セクション)

図形またはページに関連付けられた、単一のアクション タグの情報を格納します。 図形またはページには、各アクション タグに対して 1 つの [Smart Tags] 行があります。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
[Smart Tags] 行の名前は Smart Tags. *名前*  を指定し、次のセルを含む。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-action-tags-section.md) <br/> |アクション  *タグ*  ボタンを配置する図形のローカル座標内のポイントの x 座標位置。  <br/> |
|[Y](y-cell-action-tags-section.md) <br/> |アクション タグ ボタンを配置する図形のローカル座標内のポイントの  *y*  座標位置。  <br/> |
|[TagName](tagname-cell-action-tags-section.md) <br/> |アクション タグの論理名です。  <br/> |
|[X Justify](x-justify-cell-action-tags-section.md) <br/> |X  *セル*  と Y セルで定義されたポイントを基準にしたアクション タグ ボタンの x -offset。  <br/> |
|[Y Justify](y-justify-cell-action-tags-section.md) <br/> |X  *セルと Y*  セルで定義されたポイントを基準にしたアクション タグ ボタンの y オフセット。  <br/> |
|[DisplayMode](displaymode-cell-action-tags-section.md) <br/> |どのようなときにアクション タグを表示するかを指定します。  <br/> |
|[ButtonFace](buttonface-cell-action-tags-section.md) <br/> |アクション タグ ボタンの表面に表示する画像の ID です。  <br/> |
|[説明](description-cell-action-tags-section.md) <br/> |アクション タグを説明する文字列です。  <br/> |
|[Disabled](disabled-cell-action-tags-section.md) <br/> |アクション タグが無効かどうかを示します。  <br/> |
   
## <a name="remarks"></a>注釈

 必要に応じて [SmartTags.  *必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。 既存の [Smart Tags] セクションにアクション タグを追加するには、行を右クリックして、ショートカット メニューの [**行の挿入**] をクリックします。 
  
これらのセルは行名で参照できます。これは、赤いテキストの ShapeSheet ウィンドウに表示されます。 スマート タグにわかりやすい名前を割り当てるには。 *名前*  の行をクリックし、その行をクリックし、  *たとえば Size*  などの名前を入力して、行名 Smart Tags.Size を作成します。 [説明] セルは、Smart Tags.Size.Description を使用して参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

