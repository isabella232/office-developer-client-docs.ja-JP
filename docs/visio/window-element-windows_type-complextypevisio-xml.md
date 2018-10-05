---
title: ウィンドウの要素 (Windows_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: >-
  Microsoft Visio インスタンスで開いているウィンドウを表します。
   この要素には、正確に、ファイルは Visio で最初に開いたときにアプリケーション ワークスペース内のユーザー インターフェイスのウィンドウを再作成に必要な情報が含まれています。
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385348"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>ウィンドウの要素 (Windows_Type complexType)'Visio XML (')

Microsoft Visio インスタンスで開いているウィンドウを表します。
 この要素には、正確に、ファイルは Visio で最初に開いたときにアプリケーション ワークスペース内のユーザー インターフェイスのウィンドウを再作成に必要な情報が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |ドキュメントの**ウィンドウ**の要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |ドキュメントまたはウィンドウのダイナミック グリッド機能が有効になっているかどうかを指定します。  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |ドキュメントで接着が有効になっているときに図形が接着するオブジェクトを指定します。  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |接続ポイントがウィンドウに表示するかどうかを指定します。  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |図面ウィンドウで、グリッドが表示されているかどうかを指定します。  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |ガイドが図面ウィンドウに表示されるかどうかを指定します。  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |ウィンドウに改ページを表示するかどうかを指定します。  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |ルーラーが図面ウィンドウに表示されるかどうかを指定します。  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |**SnapAngle**要素のコレクションが含まれています。  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |差し込み印刷のステンシル ウィンドウのうち、ウィンドウは、メンバーのグループを指定します。  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |ウィンドウで、グループ内のステンシルの相対位置を指定する整数が含まれています。  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |(図面ウィンドウの幅の合計の割合) としては、図面ウィンドウのページのタブ コントロールの幅を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |コンテナーの ID: ページ、シート、またはマスター シェイプです。 のみ関連し、**コンテナー**が指定されている場合に必要です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |省略可能  <br/> |次のいずれかの場合があります: ドキュメント、ページ、またはマスター シェイプです。 図面またはシートとして**ゼロ**を指定するときにのみ関連します。  <br/> |Xsd:token の値を入力します。  <br/> |
|ドキュメント  <br/> |xsd:string  <br/> |省略可能  <br/> |このウィンドウに表示されるドキュメントのファイル パス。  <br/> |Xsd:string の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |マスター ID がこのウィンドウには、マスター シェイプが表示されている場合です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|Page オブジェクト  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このウィンドウは、ページを表示する場合のページの ID です。 関連のページとして指定された図面と**コンテナー**として**ゼロ**を指定した場合だけです。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このステンシル ウィンドウが含まれているウィンドウの ID。 関連の**サービス クラス**は、ステンシルとして指定されている場合のみです。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ReadOnly  <br/> |xsd:boolean  <br/> |省略可能  <br/> |読み取り専用フラグ場合は、このステンシルは図面ステンシルではありません。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|シート  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |コンテナー内のシートの ID です。 関連のシートとしてコンテナーが指定されたときだけです。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX**と**ViewCenterY**は、新しいビュー (ウィンドウ) には、最初に開いたときのページで中心点を指定します。  <br/> |Xsd:double 型の値です。  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX**と**ViewCenterY**は、新しいビュー (ウィンドウ) には、最初に開いたときのページで中心点を指定します。  <br/> |Xsd:double 型の値です。  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |省略可能  <br/> |ページの新しいビュー (ウィンドウ) を開くときに使用する既定の拡大率。 たとえば、1 は 100% です。1.5 = 150% というようにします。  <br/> |Xsd:double 型の値です。  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ウィンドウの四角形の高さです。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |省略可能  <br/> |ウィンドウの四角形の左端の座標です。  <br/> |Xsd:short の値を入力します。  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ビット フラグを指定する整数です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |省略可能  <br/> |ウィンドウの四角形の上端の座標。  <br/> |Xsd:short の値を入力します。  <br/> |
|WindowType  <br/> |xsd:token  <br/> |必須  <br/> |可能性のある次のいずれかの列挙値: 図面、シート、ステンシル、またはアイコンです。  <br/> |Xsd:token の値を入力します。  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ウィンドウの四角形の幅です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

