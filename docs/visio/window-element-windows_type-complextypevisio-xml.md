---
title: Window 要素 (Windows_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Microsoft Visio インスタンスで開いているウィンドウを表します。 この要素には、ファイルが Visio によって最初に開かれたときに、アプリケーションワークスペースでユーザーインターフェイスウィンドウを正確に再作成するために必要な情報が含まれています。
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339901"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Window 要素 (Windows_Type complexType) (' Visio XML ')

Microsoft Visio インスタンスで開いているウィンドウを表します。 この要素には、ファイルが Visio によって最初に開かれたときに、アプリケーションワークスペースでユーザーインターフェイスウィンドウを正確に再作成するために必要な情報が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |windows .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |文書の**ウィンドウ**要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |ドキュメントまたはウィンドウに対して動的グリッド機能を有効にするかどうかを指定します。  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |図面で接着が有効になっている場合に、図形を接着するオブジェクトを指定します。  <br/> |
|[showconnectionpoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |接続ポイントをウィンドウに表示するかどうかを指定します。  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |図面ウィンドウにグリッドを表示するかどうかを指定します。  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |図面ウィンドウにガイドを表示するかどうかを指定します。  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |ウィンドウに改ページを表示するかどうかを指定します。  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |ルーラーを図面ウィンドウに表示するかどうかを指定します。  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |**snapangle**要素のコレクションを格納します。  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |ウィンドウがメンバーである、結合されたステンシルウィンドウのグループを指定します。  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |ウィンドウ内のグループ内のステンシルの相対位置を指定する整数型 (integer) の値を格納します。  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |図面ウィンドウのページタブコントロールの幅を指定します (図面ウィンドウの合計幅に対する比率)。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |コンテナーの ID: Page、Sheet、または Master。 **ContainerType**が指定されている場合にのみ、関連する必要があります。  <br/> |xsd:/signedint 型の値。  <br/> |
|ContainerType  <br/> |xsd: token  <br/> |省略可能  <br/> |次の値のいずれかを指定できます: ドキュメント、ページ、またはマスター。 **WindowType**が Drawing または Sheet として指定されている場合にのみ関連します。  <br/> |xsd: token 型の値。  <br/> |
|Document  <br/> |xsd: string  <br/> |省略可能  <br/> |このウィンドウに表示される文書のファイルパスを示します。  <br/> |xsd: string 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |親要素内の要素の一意の ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|Master  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |このウィンドウにマスターシェイプが表示されている場合は、マスター ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|ページ  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |このウィンドウにページが表示されている場合のページ ID。 **WindowType**が Drawing として指定されており、 **ContainerType**が Page として指定されている場合にのみ関連します。  <br/> |xsd:/signedint 型の値。  <br/> |
|ParentWindow  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |このステンシルウィンドウが含まれているウィンドウの ID です。 **WindowType**がステンシルとして指定されている場合にのみ関連します。  <br/> |xsd:/signedint 型の値。  <br/> |
|該当  <br/> |xsd: boolean  <br/> |省略可能  <br/> |このステンシルが図面ステンシルではない場合は、読み取り専用フラグです。  <br/> |xsd: boolean 型の値。  <br/> |
|Sheet  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |コンテナー内のシートの ID。 Container が Sheet として指定されている場合にのみ関連します。  <br/> |xsd:/signedint 型の値。  <br/> |
|ViewCenterX  <br/> |xsd: double  <br/> |省略可能  <br/> |**ViewCenterX**および**viewcenter y**では、最初に開いたときに新しいビュー (ウィンドウ) が想定するページ上の中心点を指定します。  <br/> |xsd: double 型の値。  <br/> |
|view中央 y  <br/> |xsd: double  <br/> |省略可能  <br/> |**ViewCenterX**および**viewcenter y**では、最初に開いたときに新しいビュー (ウィンドウ) が想定するページ上の中心点を指定します。  <br/> |xsd: double 型の値。  <br/> |
|viewscale  <br/> |xsd: double  <br/> |省略可能  <br/> |ページの新しいビュー (ウィンドウ) を開くときに使用する既定の拡大率を設定します。 たとえば、1 = 100% のようにします。1.5 = 150% など。  <br/> |xsd: double 型の値。  <br/> |
|WindowHeight  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |ウィンドウの四角形の高さを示します。  <br/> |xsd:/signedint 型の値。  <br/> |
|WindowLeft  <br/> |xsd: short  <br/> |省略可能  <br/> |ウィンドウの四角形の左端の座標を示します。  <br/> |xsd: short 型の値。  <br/> |
|WindowState  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |ビットフラグを指定する整数。  <br/> |xsd:/signedint 型の値。  <br/> |
|WindowTop  <br/> |xsd: short  <br/> |省略可能  <br/> |ウィンドウの四角形の上端の座標です。  <br/> |xsd: short 型の値。  <br/> |
|WindowType  <br/> |xsd: token  <br/> |必須  <br/> |次のいずれかの列挙値。図面、シート、ステンシル、アイコン。  <br/> |xsd: token 型の値。  <br/> |
|WindowWidth  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |ウィンドウの四角形の幅を示します。  <br/> |xsd:/signedint 型の値。  <br/> |
   

