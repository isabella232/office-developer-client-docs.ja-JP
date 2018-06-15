---
title: HYPERLINK 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: ファイル、UNC、または URL にすることができますが、指定したアドレスに移動したパスです。
ms.openlocfilehash: 4e86fd3682d5d9e26c52839e76d2016d654b3141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805540"
---
# <a name="hyperlink-function"></a>HYPERLINK 関数

ファイル、UNC、または URL にすることができますが、指定したアドレスに移動したパスです。
  
## <a name="syntax"></a>構文

ハイパーリンク ("* **アドレス** *」[」* **サブアドレス** *「,」* * *extrainfo* * *」、* **ウィンドウ** *、"* **フレーム** *"]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _アドレス_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |完全パスまたは相対パスを指定します。  <br/> |
| _サブアドレス_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |リンク先のアドレス内の場所を指定します。 たとえば、アドレスが、Microsoft Visio ファイルの場合は、サブアドレスは、ページの名前です。サブアドレスは、ワークシートまたは範囲は、ワークシート内で場合は、Microsoft Excel のファイルでは、します。場合は HTML ページの URL、サブアドレスのアンカーを使用できます。  <br/> |
| _extrainfo_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |イメージ マップの座標など、URL の判別に使用する情報を渡します。  <br/> |
| _ウィンドウ_ <br/> |省略可能  <br/> |**ブール型 (Boolean)** <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。既定値は FALSE です。  <br/> |
| _フレーム_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | Microsoft Internet Explorer 3.0 以降などの ActiveX ブラウザーで、ActiveX の図面として Visio の図面を開く場合に、ターゲットとするフレームの名前を指定します。既定では、空の文字列です。  <br/> |
   
## <a name="remarks"></a>注釈

図面にベース パスがない場合、図面のパスに従ってリンク先まで移動します。図面が保存されないと、ハイパーリンクは未定義になります。 
  
相対パスは、 **Visio のプロパティ**] ダイアログ ボックスで指定されている**ハイパーリンクの基点**] のフィールドに基づいています。 
  
図面のページに移動するには、GOTOPAGE 関数を使用します。 
  
## <a name="example-1"></a>例 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>例 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>例 3

 `HYPERLINK("http://www.microsoft.com")`
  
## <a name="example-4"></a>例 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

