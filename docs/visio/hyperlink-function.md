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
description: 指定したアドレス (ファイル、UNC、または URL パス) に移動します。
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329947"
---
# <a name="hyperlink-function"></a>HYPERLINK 関数

指定したアドレス (ファイル、UNC、または URL パス) に移動します。
  
## <a name="syntax"></a>構文

HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |必須  <br/> |**String** <br/> |完全パスまたは相対パスを指定します。  <br/> |
| _subaddress_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |リンク先の address 内の位置を指定します。たとえば、address が、Microsoft Visio ファイルの場合は subaddress にページ名を、Microsoft Excel ファイルの場合は subaddress にワークシートまたはワークシート内の範囲を、HTML ページの URL の場合は subaddress にアンカーを指定できます。  <br/> |
| _extrainfo_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |イメージ マップの座標など、URL の判別に使用する情報を渡します。  <br/> |
| _ウィンドウ_ <br/> |省略可能  <br/> |**Boolean** <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。既定値は FALSE です。  <br/> |
| _フレーム_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | Microsoft Internet Explorer 3.0 以降などの ActiveX ブラウザーで、ActiveX の図面として Visio の図面を開く場合に、ターゲットとするフレームの名前を指定します。既定では、空の文字列です。  <br/> |
   
## <a name="remarks"></a>注釈

図面にベース パスがない場合、図面のパスに従ってリンク先まで移動します。図面が保存されないと、ハイパーリンクは未定義になります。 
  
[**Visio のプロパティ**] ダイアログ ボックスで指定されている [**ハイパーリンクの基点**] フィールドに基づいて、相対パスが指定されます。 
  
図面のページに移動するには、GOTOPAGE 関数を使用します。 
  
## <a name="example-1"></a>例 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>例 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>例 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>例 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

