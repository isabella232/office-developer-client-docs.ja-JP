---
title: Windows 要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: ドキュメントのウィンドウの要素が含まれています。
ms.openlocfilehash: 70746ccfa2d99a9fdd5b3a91320c9372aa233c7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806788"
---
# <a name="windows-element-visio-xml"></a>Windows 要素 ' Visio XML (')

ドキュメントの**ウィンドウ**の要素が含まれています。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio のインスタンスで開いているウィンドウを表します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |表示領域の高さを表します  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|ClientWidth  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |表示領域の幅の寸法を表す  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
   

