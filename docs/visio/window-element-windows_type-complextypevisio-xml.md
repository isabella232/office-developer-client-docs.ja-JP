---
title: Window 要素 (Windows_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Microsoft Visio インスタンスで開いているウィンドウを表します。 この要素には、Visio でファイルを最初に開いたときにアプリケーション ワークスペースでユーザー インターフェイス ウィンドウを正確に再作成するために必要な情報が含まれています。
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339901"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Window 要素 (Windows_Type complexType) ('Visio XML')

Microsoft Visio インスタンスで開いているウィンドウを表します。 この要素には、Visio でファイルを最初に開いたときにアプリケーション ワークスペースでユーザー インターフェイス ウィンドウを正確に再作成するために必要な情報が含まれています。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |ドキュメントに **Window** の要素が含まれます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |ドキュメントまたはウィンドウのダイナミック グリッド機能を有効にするかどうかを指定します。  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |図面で接着が有効な場合に、図形が接着するオブジェクトを指定します。  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |接続ポイントがウィンドウに表示されるかどうかを指定します。  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |図面ウィンドウにグリッドを表示するかどうかを指定します。  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |図面ウィンドウにガイドを表示するかどうかを指定します。  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |ページ区切り線がウィンドウに表示されるかどうかを指定します。  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |ルーラーが図面ウィンドウで表示されるかどうかを指定します。  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |**SnapAngle** 要素のコレクションが含まれます。  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |ウィンドウが属する、マージされたステンシル ウィンドウのグループを指定します。  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |ウィンドウのグループ内にあるステンシルの相対位置を指定する整数を含みます。  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |図面ウィンドウのページ タブ コントロールの幅を指定します (図面ウィンドウ全体の幅の一部として)。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |コンテナーの ID: Page、Sheet、Master など。 **ContainerType** が指定されている場合にのみ該当し、必要になります。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |省略可能  <br/> |次のいずれかの値になります: Document、Page、Master。 **WindowType** が Drawing または Sheet として指定されている場合にのみ該当します。  <br/> |xsd:token 型の値。  <br/> |
|Document  <br/> |xsd:string  <br/> |省略可能  <br/> |このウィンドウに表示されるドキュメントのファイル パス。  <br/> |xsd:string 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親要素内の要素の一意の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このウィンドウにマスターが表示されている場合は、マスター ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Page  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このウィンドウにページが表示されている場合は、ページ ID です。 **WindowType** が Drawing として指定され、**ContainerType** が Page として指定されている場合にのみ該当します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このステンシル ウィンドウが含まれるウィンドウの ID です。 **WindowType** が Stencil として指定されている場合にのみ該当します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ReadOnly  <br/> |xsd:boolean  <br/> |省略可能  <br/> |このステンシルがドキュメント ステンシルではない場合は、読み取り専用フラグです。  <br/> |xsd:boolean 型の値。  <br/> |
|Sheet  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |コンテナー内のシートの ID です。 Container が Sheet として指定されている場合にのみ該当します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX** および **ViewCenterY** では、新しいビュー (ウィンドウ) が最初に開いたときに想定されるページ上の中心点を指定します。  <br/> |xsd:double 型の値。  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX** および **ViewCenterY** では、新しいビュー (ウィンドウ) が最初に開いたときに想定されるページ上の中心点を指定します。  <br/> |xsd:double 型の値。  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |省略可能  <br/> |ページの新しいビュー (ウィンドウ) を開くときに使用する既定の拡大率です。 たとえば、1 = 100%、1.5 = 150% などです。  <br/> |xsd:double 型の値。  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ウィンドウの四角形の高さです。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |省略可能  <br/> |ウィンドウの四角形の左座標です。  <br/> |xsd:short 型の値。  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ビット フラグを指定する整数です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |省略可能  <br/> |ウィンドウの四角形の上部の座標です。  <br/> |xsd:short 型の値。  <br/> |
|WindowType  <br/> |xsd:token  <br/> |必須  <br/> |列挙値には、次のいずれかを指定できます。Drawing、Sheet、Stencil、Icon。  <br/> |xsd:token 型の値。  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ウィンドウの四角形の幅です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

