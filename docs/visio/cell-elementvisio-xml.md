---
title: セル要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3131bfbb-9bf6-d15d-c6ca-2f15bd038f39
description: DocumentSheet、スタイル シート、PageSheet、または [シェイプ シート内に組み込むことができるセル要素を指定します。
ms.openlocfilehash: fb983b31dc69741b12c27f47833213f7b5c3ba2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805041"
---
# <a name="cell-element-visio-xml"></a>セル要素 ' Visio XML (')

DocumentSheet、スタイル シート、PageSheet、または [シェイプ シート内に組み込むことができるセル要素を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml、pages.xml、masters.xml、マスターの # .xml、ページ番号の .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形の定義に関する情報を提供するセル要素を指定します。  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |DocumentSheet 構造体を定義します。  <br/> |
|[スタイル シート](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |図面で定義されているスタイルを表します。  <br/> |
|[PageSheet (Master_Type の複合型)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |マスターに関連付けられている図面ページのプロパティを指定します。  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面ページに関連付けられている図面ページのプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーが発生することを示します。 **E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラー メッセージの文字列です。  <br/> |
|ExternalTaskProject 要素  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の式を表します。 この属性は、次の文字列のいずれかを含めることができます。  <br/>  '(いくつかの数式)' の数式がローカルに存在する場合  <br/>  `No Formula`数式がローカルで削除されるか、ブロックされている場合  <br/>  `Inh`場合は、数式が継承されます。  <br/> |数式です。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |**シェイプ シート**セルの名前を表します。  <br/> |**シェイプ シート**セルの名前です。  <br/> 以下の「解説」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |既定の測定単位を表しますが、DL です。  <br/> |セルの単位です。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |**シェイプ シート**セルの値です。  <br/> |
   
## <a name="remarks"></a>注釈

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|[Addmarkup]  <br/> |図面が校正履歴用にチェックされているかどうかを示します。  <br/> |[[AddMarkup] セル ([Document Properties] セクション)](addmarkup-cell-document-properties-section.md) <br/> |
|(下揃え)  <br/> |親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。  <br/> |[[AlignBottom] セル ([Alignment] セクション)](alignbottom-cell-alignment-section.md) <br/> |
|AlignCenter  <br/> |親図形の原点を基準として、図形の水平方向の中心を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。  <br/> |[[AlignCenter] セル ([Alignment] セクション)](aligncenter-cell-alignment-section.md) <br/> |
|[Alignleft]  <br/> |親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。  <br/> |[[AlignLeft] セル ([Alignment] セクション)](alignleft-cell-alignment-section.md) <br/> |
|AlignMiddle  <br/> |親図形の原点を基準として、図形の垂直方向の中心を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。  <br/> |[[AlignMiddle] セル ([Alignment] セクション)](alignmiddle-cell-alignment-section.md) <br/> |
|AlignRight  <br/> |親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。  <br/> |[[AlignRight] セル ([Alignment] セクション)](alignright-cell-alignment-section.md) <br/> |
|[Aligntop]  <br/> |親図形の原点を基準として、図形の上部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。  <br/> |[[AlignTop] セル ([Alignment] セクション)](aligntop-cell-alignment-section.md) <br/> |
|角度  <br/> |親図形を基準としたときの、図形の現在の回転角度を表します。1-D 図形の回転角度を決定する既定の数式は =ATAN2(EndY-BeginY,EndX-BeginX) です。  <br/> |[[Angle] セル ([Shape Transform] セクション)](angle-cell-shape-transform-section.md) <br/> |
|[Avenuesizex]  <br/> |レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の水平方向のスペースの量を決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。  <br/> |[[AvenueSizeX] セル ([Page Layout] セクション)](avenuesizex-cell-page-layout-section.md) <br/> |
|[Avenuesizey]  <br/> |レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。 レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。  <br/> |[[AvenueSizeY] セル ([Page Layout] セクション)](avenuesizey-cell-page-layout-section.md) <br/> |
|AvoidPageBreaks  <br/> |図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。  <br/> |[[AvoidPageBreaks] セル ([ページ レイアウト] セクション)](avoidpagebreaks-cell-page-layout-section.md) <br/> |
|BeginArrow  <br/> |線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。[線] ダイアログ ボックスを使用することもできます。  <br/> |[[BeginArrow] セル ([Line Format] セクション)](beginarrow-cell-line-format-section.md) <br/> |
|BeginArrowSize  <br/> |線の開始位置にある矢印のサイズを指定します。  <br/> |[[BeginArrowSiz] セル ([Line Format] セクション)](beginarrowsize-cell-line-format-section.md) <br/> |
|[Beginx]  <br/> |親図形の原点を基準としたときの 1 次元図形の始点の x 座標を表します。 親図形の原点を基準としたときの 1 次元図形の始点の x 座標を表します。  <br/> |[[BeginX] セル ([1-D Endpoints] セクション)](beginx-cell-1-d-endpoints-section.md) <br/> |
|[Beginy]  <br/> |親図形の原点を基準としたときの 1-D 図形の始点の y 座標を表します。  <br/> |[[BeginY] セル ([1-D Endpoints] セクション)](beginy-cell-1-d-endpoints-section.md) <br/> |
|BegTrigger  <br/> |アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の始点を移動するときに別の図形に対する接続を維持するかどうかを指定します。  <br/> |[[BegTrigger] セル ([Glue Info] セクション)](begtrigger-cell-glue-info-section.md) <br/> |
|BevelBottomHeight  <br/> |ポイント単位での図形の下の面取りの高さを決定します。  <br/> |[[BevelBottomHeight] セル ([ベベルのプロパティ] セクション)](bevelbottomheight-cell-bevel-properties-section.md) <br/> |
|BevelBottomType  <br/> |図形の傾斜面の下の面取りの種類を指定します。  <br/> |[[BevelBottomType] セル ([ベベルのプロパティ] セクション)](bevelbottomtype-cell-bevel-properties-section.md) <br/> |
|BevelBottomWidth  <br/> |ポイントの下の面取りの幅を決定します。  <br/> |[[BevelBottomWidth] セル ([ベベルのプロパティ] セクション)](bevelbottomwidth-cell-bevel-properties-section.md) <br/> |
|BevelContourColor  <br/> |ベベルの RGB 値の配分やテーマによって、決められた色を決定します。  <br/> |[[BevelContourColor] セル ([ベベルのプロパティ] セクション)](bevelcontourcolor-cell-bevel-properties-section.md) <br/> |
|BevelContourSize  <br/> |傾斜面の輪郭をポイント単位でのサイズを決定します。  <br/> |[[BevelContourSize] セル ([ベベルのプロパティ] セクション)](bevelcontoursize-cell-bevel-properties-section.md) <br/> |
|BevelDepthColor  <br/> |RGB 値として、またはアクティブなテーマでの面取りの奥行、色を決定します。  <br/> |[[BevelDepthColor] セル ([ベベルのプロパティ] セクション)](beveldepthcolor-cell-bevel-properties-section.md) <br/> |
|BevelDepthSize  <br/> |傾斜面の深さをポイント単位でのサイズを決定します。  <br/> |[[BevelDepthSize] セル ([ベベルのプロパティ] セクション)](beveldepthsize-cell-bevel-properties-section.md) <br/> |
|BevelLightingAngle  <br/> |度の傾斜面を基準にして稲妻の角度を決定します。  <br/> |[[BevelLightingAngle] セル ([ベベルのプロパティ] セクション)](bevellightingangle-cell-bevel-properties-section.md) <br/> |
|BevelLightingType  <br/> |ベベル効果に使用する光源の種類を決定します。  <br/> |[[BevelLightingType] セル ([ベベルのプロパティ] セクション)](bevellightingtype-cell-bevel-properties-section.md) <br/> |
|BevelMaterialType  <br/> |傾斜面で構成する材料のタイプを決定します。  <br/> |[[BevelMaterialType] セル ([ベベルのプロパティ] セクション)](bevelmaterialtype-cell-bevel-properties-section.md) <br/> |
|BevelTopHeight  <br/> |ポイントで図形の上の面取りの高さを決定します。  <br/> |[[BevelTopHeight] セル ([ベベルのプロパティ] セクション)](beveltopheight-cell-bevel-properties-section.md) <br/> |
|BevelTopType  <br/> |図形の上端の面取りの種類を決定します。  <br/> |[[BevelTopType] セル ([ベベルのプロパティ] セクション)](beveltoptype-cell-bevel-properties-section.md) <br/> |
|BevelTopWidth  <br/> |ポイントの上の面取りの幅を決定します。  <br/> |[[BevelTopWidth] セル ([ベベルのプロパティ] セクション)](beveltopwidth-cell-bevel-properties-section.md) <br/> |
|BlockSizeX  <br/> |領域で、図形の各収まる必要があります図面ページで、[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、水平方向のブロック サイズを決定します。  <br/> |[[BlockSizeX] セル ([Page Layout] セクション)](blocksizex-cell-page-layout-section.md) <br/> |
|BlockSizeY  <br/> |領域でそれぞれの図形の収まる必要があります、図面ページでレイアウトの構成] ダイアログを使用して図形をレイアウトするときに、垂直方向のブロック ・ サイズを決定します。  <br/> |[[BlockSizeY] セル ([Page Layout] セクション)](blocksizey-cell-page-layout-section.md) <br/> |
|Blur  <br/> |ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。  <br/> |[[Blur] セル ([Image Properties] セクション)](blur-cell-image-properties-section.md) <br/> |
|BottomMargin  <br/> |テキスト ブロックの下枠とそれに含まれるテキストの最後の行の間の距離を決定します。  <br/> |[[BottomMargin] セル ([Text Block Format] セクション)](bottommargin-cell-text-block-format-section.md) <br/> |
|Brightness  <br/> |ビットマップ イメージの明るさを調整します。  <br/> |[明るさのセル (イメージのプロパティ] セクション](brightness-cell-image-properties-section.md) <br/> |
|予定表  <br/> |セル数式が Date 情報を含むときに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Miscellaneous] セクション)](calendar-cell-miscellaneous-section.md) <br/> |
|予定表  <br/> |データ型が Date のとき図形データに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Shape Data] セクション)](calendar-cell-shape-data-section.md) <br/> |
|予定表  <br/> |データ型が Date のときに、テキスト フィールドに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Text Fields] セクション)](calendar-cell-text-fields-section.md) <br/> |
|[Centerx]  <br/> |図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。  <br/> |[[CenterX] セル ([Print Properties] セクション)](centerx-cell-print-properties-section.md) <br/> |
|CenterY  <br/> |図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。  <br/> |[[CenterY] セル ([Print Properties] セクション)](centery-cell-print-properties-section.md) <br/> |
|ClippingPath  <br/> |イメージを限定しているパスの図形座標への参照を格納します。  <br/> |[[ClippingPath] セル ([外部画像情報] セクション)](clippingpath-cell-foreign-image-info-section.md) <br/> |
|ColorSchemeIndex  <br/> |整数値で、図形に適用されているテーマの配色パターンを決定します。  <br/> |[[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)](colorschemeindex-cell-theme-properties-section.md) <br/> |
|Comment  <br/> |コメント内に表示されるテキストが含まれます。  <br/> |[[Comment] セル ([Annotation] セクション)](comment-cell-annotation-section.md) <br/> |
|Comment  <br/> |図形のコメント テキストを文字列形式で格納します。  <br/> |[[Comment] セル ([Miscellaneous] セクション)](comment-cell-miscellaneous-section.md) <br/> |
|CompoundType  <br/> |複合図形の線の種類を決定します。  <br/> |[[CompoundType] セル ([線の書式設定] セクション)](compoundtype-cell-line-format-section.md) <br/> |
|ConFixedCode  <br/> |コネクタの経路の変更方法を指定します。  <br/> |[[ConFixedCode] セル ([Shape Layout] セクション)](confixedcode-cell-shape-layout-section.md) <br/> |
|ConLineJumpCode  <br/> |コネクタの飛び越し点の表示方法を指定します。  <br/> |[[ConLineJumpCode] セル ([Shape Layout] セクション)](conlinejumpcode-cell-shape-layout-section.md) <br/> |
|ConLineJumpDirX  <br/> |図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。  <br/> |[[ConLineJumpDirX] セル ([Shape Layout] セクション)](conlinejumpdirx-cell-shape-layout-section.md) <br/> |
|ConLineJumpDirY  <br/> |図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。  <br/> |[[ConLineJumpDirY] セル ([Shape Layout] セクション)](conlinejumpdiry-cell-shape-layout-section.md) <br/> |
|ConLineJumpStyle  <br/> |動的コネクタの飛び越し点のスタイルを指定します。  <br/> |[[ConLineJumpStyle] セル ([Shape Layout] セクション)](conlinejumpstyle-cell-shape-layout-section.md) <br/> |
|ConLineRouteExt  <br/> |コネクタの外観を指定します。  <br/> |[[ConLineRouteExt] セル ([Shape Layout] セクション)](conlinerouteext-cell-shape-layout-section.md) <br/> |
|ConnectorSchemeIndex  <br/> |整数値で、図形に適用されているテーマのコネクタの設定を決定します。  <br/> |[[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)](connectorschemeindex-cell-theme-properties-section.md) <br/> |
|Contrast  <br/> |ビットマップ イメージのコントラストを調整します。  <br/> |[[Contrast] セル ([Image Properties] セクション)](contrast-cell-image-properties-section.md) <br/> |
|著作権  <br/> |人間が読める形式の著作権表記を表す文字列が含まれています  <br/> ||
|CtrlAsInput  <br/> |コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。  <br/> |[[CtrlAsInput] セル ([Page Layout] セクション)](ctrlasinput-cell-page-layout-section.md) <br/> |
|DefaultTabStop  <br/> |テキスト ブロックの既定のタブ位置の間隔を指定します。  <br/> |[[DefaultTabstop] セル ([Text Block Format] セクション)](defaulttabstop-cell-text-block-format-section.md) <br/> |
|Denoise  <br/> |ビットマップ画像からノイズをランダムにさまざまな色) を削除します。  <br/> |[[Denoise] セル ([Image Properties] セクション)](denoise-cell-image-properties-section.md) <br/> |
|DisplayLevel  <br/> |図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。  <br/> |[[DisplayLevel] セル ([図形レイアウト] セクション)](displaylevel-cell-shape-layout-section.md) <br/> |
|DisplayMode  <br/> |グループ図形とそのメンバーの表示方法を指定します。  <br/> |[[DisplayMode] セル ([Group Properties] セクション)](displaymode-cell-group-properties-section.md) <br/> |
|DisplayMode  <br/> |アクションのタグには、ユーザーがタグの上、ポインターを移動すると、図形が選択されている場合、またはすべての時間が表示されるかどうかを決定します。  <br/> |[DisplayMode セル ([Smart Tags] セクション)](displaymode-cell-action-tags-section.md) <br/> |
|DistanceFromGround  <br/> |オブジェクトに 3-D の回転時に地面から発生する距離を指定します。  <br/> |[[DistanceFromGround] セル ([3-D 回転のプロパティ] セクション)](distancefromground-cell-3-d-rotation-properties.md) <br/> |
|[Doclangid]  <br/> |図面の既定の言語を示します。  <br/> |[[DocLangID] セル ([Document Properties] セクション)](doclangid-cell-document-properties-section.md) <br/> |
|DocLockDuplicatePage  <br/> |ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。  <br/> |[[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)](doclockduplicatepage-cell-document-properties-section.md) <br/> |
|DocLockReplace  <br/> |置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。  <br/> |[[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)](doclockreplace-cell-document-properties-section.md) <br/> |
|DontMoveChildren  <br/> |グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。  <br/> |[[DontMoveChildren] セル ([Group Properties] セクション)](dontmovechildren-cell-group-properties-section.md) <br/> |
|DrawingResizeType  <br/> |図に合わせて、図面ページが自動的にサイズ変更するかどうかを決定します。  <br/> |[[DrawingResizeType] セル ([ページのプロパティ] セクション)](drawingresizetype-cell-page-properties-section.md) <br/> |
|DrawingScale  <br/> |現在の図面縮尺で、図面単位の値を表します。  <br/> |[[DrawingScale] セル ([Page Properties] セクション)](drawingscale-cell-page-properties-section.md) <br/> |
|DrawingScaleType  <br/> |[ページ設定] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[ホーム] タブで [ページ設定] 矢印をクリックします)。  <br/> |[[DrawingScaleType] セル ([Page Properties] セクション)](drawingscaletype-cell-page-properties-section.md) <br/> |
|DrawingSizeType  <br/> |図面のサイズを指定します。  <br/> |[[DrawingSizeType] セル ([Page Properties] セクション)](drawingsizetype-cell-page-properties-section.md) <br/> |
|DropOnPageScale  <br/> |図形を図面ページにドロップしたときの縮尺のパーセント値が含まれます。  <br/> |[[DropOnPageScale] セル ([Miscellaneous] セクション)](droponpagescale-cell-miscellaneous-section.md) <br/> |
|DynamicsOff  <br/> |図面ページ上にある他の図形やコネクタに合わせて、配置可能な図形を移動したり、コネクタを迂回させるかどうかを指定します。  <br/> |[[DynamicsOff] セル ([Page Layout] セクション)](dynamicsoff-cell-page-layout-section.md) <br/> |
|DynFeedback  <br/> |コネクタをドラッグしたときにユーザーに提供される視覚的なフィードバックの種類を変更します。  <br/> |[[DynFeedback] セル ([Miscellaneous] セクション)](dynfeedback-cell-miscellaneous-section.md) <br/> |
|EffectSchemeIndex  <br/> |整数値で、図形に適用するテーマの効果設定を決定します。  <br/> |[[EffectSchemeIndex] セル ([テーマのプロパティ] セクション)](effectschemeindex-cell-theme-properties-section.md) <br/> |
|EmbellishmentIndex  <br/> |コールアウト、コンテナー、タイムライン、および組織図の図形の外観と動作 (装飾) を変更します。  <br/> |[[EmbellishmentIndex] セル ([テーマのプロパティ] セクション)](embellishmentindex-cell-theme-properties-section.md) <br/> |
|EnableFillProps  <br/> |スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。  <br/> |[[EnableFillProps] セル ([Style Properties] セクション)](enablefillprops-cell-style-properties-section.md) <br/> |
|EnableGrid  <br/> |非表示、内部ページ グリッド ベースのレイアウトの構成] ダイアログ ボックスでレイアウトを構成するときの図形をレイアウトするかどうかを決定します。  <br/> |[[EnableGrid] セル ([Page Layout] セクション)](enablegrid-cell-page-layout-section.md) <br/> |
|EnableLineProps  <br/> |スタイルに線のプロパティを含めるかどうかを指定します。  <br/> |[[EnableLineProps] セル ([Style Properties] セクション)](enablelineprops-cell-style-properties-section.md) <br/> |
|EnableTextProps  <br/> |スタイルにテキストのプロパティを含めるかどうかを指定します。  <br/> |[[EnableTextProps] セル ([Style Properties] セクション)](enabletextprops-cell-style-properties-section.md) <br/> |
|[Endarrow]  <br/> |線の最後の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。  <br/> |[[EndArrow] セル ([Line Format] セクション)](endarrow-cell-line-format-section.md) <br/> |
|EndArrowSize  <br/> |線の終端にある矢印のサイズを指定します。  <br/> |[[EndArrowSize] セル ([Line Format] セクション)](endarrowsize-cell-line-format-section.md) <br/> |
|EndTrigger  <br/> |アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の終点を移動するときに別の図形に対する接続を維持するかどうかを指定します。  <br/> |[[EndTrigger] セル ([Glue Info] セクション)](endtrigger-cell-glue-info-section.md) <br/> |
|[Endx]  <br/> |親図形の原点を基準としたときの、1-D 図形の終点の x 座標を表します。  <br/> |[[EndX] セル ([1-D Endpoints] セクション)](endx-cell-1-d-endpoints-section.md) <br/> |
|[Endy]  <br/> |親図形の原点を基準としたときの、1-D 図形の終点の y 座標を表します。  <br/> |[[EndY] セル ([1-D Endpoints] セクション)](http://msdn.microsoft.com/library/3fbfa4bc-7792-b6d9-d549-4602d252c293"%28Office.15%29.aspx) <br/> |
|EventDblClick  <br/> |図形をダブルクリックしたときに評価されるイベント セルです。  <br/> |[[EventDblClick] セル ([Events] セクション)](eventdblclick-cell-events-section.md) <br/> |
|[Eventdrop]  <br/> |図面ページに図形をインスタンスとしてドロップしたとき、または図形を複製したり貼り付けたときに評価されるイベント セルです。  <br/> |[[EventDrop] セル ([Events] セクション)](eventdrop-cell-events-section.md) <br/> |
|EventMultiDrop  <br/> |インスタンスまたはシェイプを複製したり貼り付けたときに、図面ページに複数の図形をドロップしたときに評価されるイベント セルです。  <br/> |[[EventMultiDrop] セル ([イベント] セクション)](eventmultidrop-cell-events-section.md) <br/> |
|[Eventxfmod]  <br/> |ページ上で、図形の位置または向きの変更 ("XF") が行われたときに評価されるイベント セルです。  <br/> |[[EventXFMod] セル ([Events] セクション)](eventxfmod-cell-events-section.md) <br/> |
|[Fillbkgnd]  <br/> |図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。  <br/> |[[FillBkgnd] セル ([Fill Format] セクション)](fillbkgnd-cell-fill-format-section.md) <br/> |
|FillBkgndTrans  <br/> |図形の塗りつぶしのパターンに対して、背景 (塗りつぶし部分) に適用される透過性レベルを指定します。  <br/> |[[FillBkgndTrans] セル ([Fill Format] セクション)](fillbkgndtrans-cell-fill-format-section.md) <br/> |
|FillForegnd  <br/> |図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。  <br/> |[[FillForegnd] セル ([Fill Format] セクション)](fillforegnd-cell-fill-format-section.md) <br/> |
|FillForegndTrans  <br/> |図形の塗りつぶしのパターンに対して、背景 (塗りつぶし部分) に適用される透過性レベルを指定します。  <br/> |[[FillForegndTrans] セル ([Fill Format] セクション)](fillforegndtrans-cell-fill-format-section.md) <br/> |
|FillGradientAngle  <br/> |角度の直線の方向にグラデーションの塗りつぶしのグラデーションの角度を決定します。  <br/> |[[FillGradientAngle] セル ([グラデーションのプロパティ] セクション)](fillgradientangle-cell-gradient-properties-section.md) <br/> |
|FillGradientDir  <br/> |塗りつぶしのグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。  <br/> |[[FillGradientDir] セル ([グラデーションのプロパティ] セクション)](fillgradientdir-cell-gradient-properties-section.md) <br/> |
|FillGradientEnabled  <br/> |この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。  <br/> |[[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)](fillgradientenabled-cell-gradient-properties-section.md) <br/> |
|FillPattern  <br/> |図形の塗りつぶしのパターンを指定します。ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。  <br/> |[[FillPattern] セル ([Fill Format] セクション)](fillpattern-cell-fill-format-section.md) <br/> |
|[Flipx]  <br/> |図形が左右反転されているかを示します。  <br/> |[[FlipX] セル ([Shape Transform] セクション)](flipx-cell-shape-transform-section.md) <br/> |
|[Flipy]  <br/> |図形が上下反転されているかを示します。  <br/> |[[FlipY] セル ([Shape Transform] セクション)](flipy-cell-shape-transform-section.md) <br/> |
|FontSchemeIndex  <br/> |整数値で、図形に適用されているテーマのフォント パターンを決定します。  <br/> |[[FontSchemeIndex] セル ([テーマのプロパティ] セクション)](fontschemeindex-cell-theme-properties-section.md) <br/> |
|Gamma  <br/> |モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。  <br/> |[[Gamma] セル ([Image Properties] セクション)](gamma-cell-image-properties-section.md) <br/> |
|GlowColor  <br/> |図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。  <br/> |[[GlowColor] セル ([追加効果のプロパティ] セクション)](glowcolor-cell-additional-effect-properties-section.md) <br/> |
|GlowColorTrans  <br/> |パーセントでの図形の光彩、線の色の透過性レベルを決定します。  <br/> |[[GlowColorTrans] セル ([追加効果のプロパティ] セクション)](glowcolortrans-cell-additional-effect-properties-section.md) <br/> |
|GlowSize  <br/> |ポイントで図形の外部の光彩のサイズを決定します。  <br/> |[[GlowSize] セル ([追加効果のプロパティ] セクション)](http://msdn.microsoft.com/library/2ddc7a08-25b8-4903-b0dd-be72d1fa8075"%28Office.15%29.aspx) <br/> |
|[Gluetype]  <br/> |1-D 図形を別の図形に接着するときに静的接着 (点から点) と動的接着 (図形から図形) のどちらを使用するかを指定します。  <br/> |[[GlueType] セル ([Glue Info] セクション)](gluetype-cell-glue-info-section.md) <br/> |
|Height  <br/> |図形の高さを図面単位で指定します。  <br/> |[[Height] セル ([Shape Transform] セクション)](height-cell-shape-transform-section.md) <br/> |
|HelpTopic  <br/> |図形のヘルプ トピックの ID を指定します。  <br/> ||
|HideForApply  <br/> |Microsoft Visio ユーザー インターフェイスのスタイルを表示する場所を決定します。  <br/> |[[HideForApply] セル ([Style Properties] セクション)](hideforapply-cell-style-properties-section.md) <br/> |
|HideText  <br/> |図形のテキストを非表示にします。  <br/> |[[HideText] セル ([Miscellaneous] セクション)](hidetext-cell-miscellaneous-section.md) <br/> |
|[Imgheight]  <br/> |枠内におけるオブジェクトのイメージの高さを決定します。  <br/> |[[ImgHeight] セル ([Foreign Image Info] セクション)](imgheight-cell-foreign-image-info-section.md) <br/> |
|ImgOffsetX  <br/> |オブジェクトの距離は、オブジェクトの枠の原点から水平方向にオフセットを決定します。  <br/> |[[ImgOffsetX] セル ([Foreign Image Info] セクション)](imgoffsetx-cell-foreign-image-info-section.md) <br/> |
|ImgOffsetY  <br/> |オブジェクトの枠の原点からの距離、オブジェクトが垂直方向にオフセットを決定します。  <br/> |[[ImgOffsetY] セル ([Foreign Image Info] セクション)](imgoffsety-cell-foreign-image-info-section.md) <br/> |
|[Imgwidth]  <br/> |枠内におけるオブジェクトのイメージの幅を決定します。  <br/> |[[ImgWidth] セル ([Foreign Image Info] セクション)](imgwidth-cell-foreign-image-info-section.md) <br/> |
|InhibitSnap  <br/> |前景ページ上の図形を、同じページにある他のオブジェクトや背景ページ上の図形にスナップするかどうかを指定します。  <br/> |[[InhibitSnap] セル ([Page Properties] セクション)](inhibitsnap-cell-page-properties-section.md) <br/> |
|IsDropSource  <br/> |図形をドロップしてグループに追加できるかどうかを指定します。  <br/> |[[IsDropSource] セル ([Miscellaneous] セクション)](isdropsource-cell-miscellaneous-section.md) <br/> |
|IsDropTarget  <br/> |グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。  <br/> |[[IsDropTarget] セル ([Group Properties] セクション)](isdroptarget-cell-group-properties-section.md) <br/> |
|IsSnapTarget  <br/> |グループにスナップするかグループ内の図形にスナップするかを指定します。  <br/> |[[IsSnapTarget] セル ([Group Properties] セクション)](issnaptarget-cell-group-properties-section.md) <br/> |
|IsTextEditTarget  <br/> |グループに対するテキストの割り当て方を指定します。  <br/> |[[IsTextEditTarget] セル ([Group Properties] セクション)](istextedittarget-cell-group-properties-section.md) <br/> |
|KeepTextFlat  <br/> |図形のテキストが 3-d 図形の回転を無視するかどうかを示します。 2 次元の回転には適用されません。  <br/> |[[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)](keeptextflat-cell-3-d-rotation-properties-section.md) <br/> |
|LangID  <br/> |コメントの記入に使用した言語を示します。  <br/> |[[LangID] セル ([Annotation] セクション)](langid-cell-annotation-section.md) <br/> |
|LangID  <br/> |テキストの記入に使用した言語を示します。  <br/> |[[LangID] セル ([Character] セクション)](langid-cell-character-section.md) <br/> |
|LangID  <br/> |セル数式の作成に使用した言語を示します。  <br/> |[[LangID] セル ([Miscellaneous] セクション)](langid-cell-miscellaneous-section.md) <br/> |
|LangID  <br/> |図形データ値の記入に使用した言語を示します。  <br/> |[[LangID] セル ([Shape Data] セクション)](langid-cell-shape-data-section.md) <br/> |
|LayerMember  <br/> |ページのレイヤーのゼロから始まるインデックスに基づいて、図形のレイヤーのメンバーシップを指定します。 図形は、複数のレイヤーに割り当てられているが、セミコロンで区切られた各レイヤーのインデックスが表示されます。  <br/> ||
|LeftMargin  <br/> |テキスト ブロックの左枠とテキストの間の距離を決定します。  <br/> |[[LeftMargin] セル ([Text Block Format] セクション)](leftmargin-cell-text-block-format-section.md) <br/> |
|LineAdjustFrom  <br/> |複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。  <br/> |[[LineAdjustFrom] セル ([Page Layout] セクション)](lineadjustfrom-cell-page-layout-section.md) <br/> |
|LineAdjustTo  <br/> |線を束ねるときに対象とする動的コネクタを指定します。  <br/> |[[LineAdjustTo] セル ([Page Layout] セクション)](lineadjustto-cell-page-layout-section.md) <br/> |
|[Linecap]  <br/> |線の端点を丸、四角形、または拡張のどれにするかを指定します。  <br/> |[[LineCap] セル ([Line Format] セクション)](linecap-cell-line-format-section.md) <br/> |
|線の色  <br/> |図形の線の色を指定します。  <br/> |[[LineColor] セル ([Line Format] セクション)](linecolor-cell-line-format-section.md) <br/> |
|LineColorTrans  <br/> |図形の線の色の透過性レベルを指定します。  <br/> |[[LineColorTrans] セル ([Line Format] セクション)](linecolortrans-cell-line-format-section.md) <br/> |
|LineGradientAngle  <br/> |359.9 に 0 からの線形のグラデーションの線のグラデーションの角度を決定します。  <br/> |[[LineGradientAngle] セル ([グラデーションのプロパティ] セクション)](linegradientangle-cell-gradient-properties-section.md) <br/> |
|LineGradientDir  <br/> |線のグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。  <br/> |[[LineGradientDir] セル ([グラデーションのプロパティ] セクション)](linegradientdir-cell-gradient-properties-section.md) <br/> |
|LineGradientEnabled  <br/> |線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。  <br/> |[[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)](linegradientenabled-cell-gradient-properties-section.md) <br/> |
|LineJumpCode  <br/> |飛び越し点を表示するコネクタを指定します。  <br/> ||
|LineJumpFactorX  <br/> |[LineToLineX] セルの値を基準にして、ページ上にある水平方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。  <br/> |[[LineJumpFactorX] セル ([Page Layout] セクション)](linejumpfactorx-cell-page-layout-section.md) <br/> |
|LineJumpFactorY  <br/> |[LineToLineY] セルの値を基準にして、ページ上にある垂直方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。  <br/> |[[LineJumpFactorY] セル ([Page Layout] セクション)](linejumpfactory-cell-page-layout-section.md) <br/> |
|LineJumpStyle  <br/> |ローカルな飛び越し点のスタイルを持たない図面ページ上のすべてのコネクタに対して、飛び越し点のスタイルを指定します。  <br/> |[[LineJumpStyle] セル ([Page Layout] セクション)](linejumpstyle-cell-page-layout-section.md) <br/> |
|LinePattern  <br/> |図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。  <br/> |[[LinePattern] セル ([Line Format] セクション)](linepattern-cell-line-format-section.md) <br/> |
|LineRouteExt  <br/> |図面ページにあるすべてのコネクタの既定の外観を指定します。  <br/> |[[LineRouteExt] セル ([Page Layout] セクション)](linerouteext-cell-page-layout-section.md) <br/> |
|[Linetolinex]  <br/> |図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。  <br/> |[[LineToLineX] セル ([Page Layout] セクション)](linetolinex-cell-page-layout-section.md) <br/> |
|[Linetoliney]  <br/> |図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。  <br/> |[[LineToLineY] セル ([Page Layout] セクション)](linetoliney-cell-page-layout-section.md) <br/> |
|LineToNodeX  <br/> |図面ページにあるすべてのコネクタと図形間の水平方向のクリアランスを指定します。  <br/> |[[LineToNodeX] セル ([Page Layout] セクション)](linetonodex-cell-page-layout-section.md) <br/> |
|LineToNodeY  <br/> |図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。  <br/> |[[LineToNodeY] セル ([Page Layout] セクション)](linetonodey-cell-page-layout-section.md) <br/> |
|LineWeight  <br/> |図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。  <br/> |[[LineWeight] セル ([Line Format] セクション)](lineweight-cell-line-format-section.md) <br/> |
|LocalizeMerge  <br/> |図形を図面間でコピーするときにローカライズするかどうかを指定します。  <br/> |[[LocalizeMerge] セル ([Miscellaneous] セクション)](localizemerge-cell-miscellaneous-section.md) <br/> |
|LockAspect  <br/> |図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。  <br/> |[[LockAspect] セル ([Protection] セクション)](lockaspect-cell-protection-section.md) <br/> |
|[Lockbegin]  <br/> |1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。  <br/> |[[LockBegin] セル ([Protection] セクション)](lockbegin-cell-protection-section.md) <br/> |
|LockCalcWH  <br/> |図形の選択範囲をロックして、頂点を編集した場合や、行の種類を [Geometry] セクションで変更した場合に再計算できないようにします。  <br/> |[[LockCalcWH] セル ([Protection] セクション)](lockcalcwh-cell-protection-section.md) <br/> |
|[Lockcrop]  <br/> |別のプログラムのオブジェクトをロックして、[トリミング ツール] を使用したトリミングができないようにします。  <br/> |[[LockCrop] セル ([Protection] セクション)](lockcrop-cell-protection-section.md) <br/> |
|LockCustProp  <br/> |[図形データの定義] ダイアログ ボックス、または [図形データ] ウィンドウのショートカット メニューを使用して、ユーザー インターフェイス (UI) の図形データを追加、削除、または修正できるかどうかを判別します。  <br/> |[[LockCustProp] セル ([Protection] セクション)](lockcustprop-cell-protection-section.md) <br/> |
|LockDelete  <br/> |図形をロックして、削除できないようにします。  <br/> |[[LockDelete] セル ([Protection] セクション)](lockdelete-cell-protection-section.md) <br/> |
|[Lockend]  <br/> |1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。  <br/> |[[LockEnd] セル ([Protection] セクション)](lockend-cell-protection-section.md) <br/> |
|LockFormat  <br/> |図形の書式設定をロックして、変更できないようにします。  <br/> |[[LockFormat] セル ([Protection] セクション)](lockformat-cell-protection-section.md) <br/> |
|LockFromGroupFormat  <br/> |フォーマットを変更してグループ図形を直接選択したサブ図形の書式を設定するユーザーを許可する一方、サブ図形に反映されません。 [LockFromGroupFormat] セルの値は、[保護] ダイアログ ボックスにある [グループ書式設定を適用不可にする] チェック ボックスの設定に対応します。  <br/> |[[LockFromGroupFormat] セル ([保護] セクション)](lockfromgroupformat-cell-protection-section.md) <br/> |
|[Lockgroup]  <br/> |グループをロックして、グループを解除できないようにします。  <br/> |[[LockGroup] セル ([Protection] セクション)](lockgroup-cell-protection-section.md) <br/> |
|LockHeight  <br/> |図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。  <br/> |[[LockHeight] セル ([Protection] セクション)](lockheight-cell-protection-section.md) <br/> |
|[Lockmovex]  <br/> |図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。  <br/> |[[LockMoveX] セル ([Protection] セクション)](lockmovex-cell-protection-section.md) <br/> |
|[Lockmovey]  <br/> |図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。  <br/> |[[LockMoveY] セル ([Protection] セクション)](http://msdn.microsoft.com/library/4ed8cab4-112a-e96a-f4e3-02490a6f87fa"%28Office.15%29.aspx) <br/> |
|LockPreview  <br/> |図面を保存するたびにプレビューを保存するかどうかを指定します。  <br/> |[[LockPreview] セル ([Document Properties] セクション)](lockpreview-cell-document-properties-section.md) <br/> |
|LockReplace  <br/> |図形を置換操作に使用できるかどうか (ターゲット図形または置換後の図形のいずれかとして) を示します。  <br/> |[[LockReplace] セル ([保護] セクション)](lockreplace-cell-protection-section.md) <br/> |
|LockRotate  <br/> |2 次元図形をロックして、回転ハンドル、[左へ 90 度回転] コマンド、[右へ 90 度回転] コマンドによる回転操作ができないようにします。  <br/> |[[LockRotate] セル ([Protection] セクション)](lockrotate-cell-protection-section.md) <br/> |
|Lockselect] を有効  <br/> |図形の選択操作ができないようにします。  <br/> |[[LockSelect] セル ([Protection] セクション)](lockselect-cell-protection-section.md) <br/> |
|LockTextEdit  <br/> |図形のテキストをロックして、編集できないようにします。  <br/> |[[LockTextEdit] セル ([Protection] セクション)](locktextedit-cell-protection-section.md) <br/> |
|LockThemeColors  <br/> |図形には、テーマの色のアプリケーションを防止します。 [LockThemeColors] セルの値は、[保護] ダイアログ ボックスの [テーマの色を適用不可にする] チェックボックスの設定に対応します。  <br/> |[[LockThemeColors] セル ([保護] セクション)](lockthemecolors-cell-protection-section.md) <br/> |
|LockThemeConnectors  <br/> |[テーマのプロパティ] 行の [ConnectorsSchemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。  <br/> |[[LockThemeConnectors] セル ([保護] セクション)](lockthemeconnectors-cell-protection-section.md) <br/> |
|LockThemeEffects  <br/> |保護] ダイアログ ボックスでのテーマの効果のチェック ボックスの設定に対応します。  <br/> |[[LockThemeEffects] セル ([保護] セクション)](lockthemeeffects-cell-protection-section.md) <br/> |
|LockThemeFonts  <br/> |新しいテーマを適用することで、[Theme Properties] 行の [FontIndex] セルが変更されないようにします。ユーザーが手動でシェイプシートのこの値を編集することは防げません。  <br/> |[[LockThemeFonts] セル ([保護] セクション)](lockthemefonts-cell-protection-section.md) <br/> |
|LockThemeIndex  <br/> |[テーマのプロパティ] 行の [ThemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。  <br/> |[[LockThemeIndex] セル ([保護] セクション)](lockthemeindex-cell-protection-section.md) <br/> |
|LockVariation  <br/> |ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。  <br/> |[[LockVariation] セル ([保護] セクション)](lockvariation-cell-protection-section.md) <br/> |
|LockVtxEdit  <br/> |図形の頂点をロックします。ロックすると、頂点を編集できなくなります。  <br/> |[[LockVtxEdit] セル ([Protection] セクション)](lockvtxedit-cell-protection-section.md) <br/> |
|[Lockwidth]  <br/> |図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。  <br/> |[[LockWidth] セル ([Protection] セクション)](lockwidth-cell-protection-section.md) <br/> |
|[Locpinx]  <br/> |図形の原点を基準として、図形の pin (回転の中心) の x 座標を表します。 [Locpinx] を決定するための既定の数式は: 幅を = \* 0.5 です。  <br/> |[[LocPinX] セル ([Shape Transform] セクション)](locpinx-cell-shape-transform-section.md) <br/> |
|LockPinY  <br/> |図形の原点を基準として、図形の pin (回転の中心) の y 座標を表します。 [Locpiny] を決定するための既定の数式は: = 高さ\*0.5 です。  <br/> |[[LocPinY] セル ([Shape Transform] セクション)](locpiny-cell-shape-transform-section.md) <br/> |
|NoAlignBox  <br/> |選択した図形の選択範囲の表示/非表示を切り替えます。  <br/> |[[NoAlignBox] セル ([Miscellaneous] セクション)](noalignbox-cell-miscellaneous-section.md) <br/> |
|NoCoauth  <br/> |SharePoint 2013 のサーバー上、またはマイクロソフトの OneDrive に保存されたドキュメントにことができます coauthoring のセッションで同時に複数の作成者によって編集かどうかを設定します。  <br/> |[[NoCoauth] セル ([ドキュメントのプロパティ] セクション)](nocoauth-cell-document-properties-section.md) <br/> |
|NoCtlHandles  <br/> |コントロール ハンドル、図形を選択するときに表示されません。  <br/> |[[NoCtlHandles] セル ([Miscellaneous] セクション)](noctlhandles-cell-miscellaneous-section.md) <br/> |
|NoLiveDynamics  <br/> |図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。  <br/> |[[NoLiveDynamics] セル ([Miscellaneous] セクション)](nolivedynamics-cell-miscellaneous-section.md) <br/> |
|印刷できません。  <br/> |選択した図形の印刷のオン/オフを切り替えます。  <br/> |[[NonPrinting] セル ([Miscellaneous] セクション)](nonprinting-cell-miscellaneous-section.md) <br/> |
|NoObjHandles  <br/> |選択した図形の選択ハンドルの表示/非表示を切り替えます。  <br/> |[[NoObjHandles] セル ([Miscellaneous] セクション)](noobjhandles-cell-miscellaneous-section.md) <br/> |
|NoProofing  <br/> |スペル チェックを自動的に修正されるかどうかと、選択した図形のスペル チェックのエラーが表示されるかどうかを決定します。  <br/> ||
|[Objtype]  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図面上のオブジェクトが配置可能かどうか、または迂回可能かどうかを指定します。  <br/> |[[ObjType] セル ([Miscellaneous] セクション)](objtype-cell-miscellaneous-section.md) <br/> |
|OnPage  <br/> |特定のプリンター ページ番号に図面を印刷するかどうかを示します。  <br/> |[[OnPage] セル ([Print Properties] セクション)](onpage-cell-print-properties-section.md) <br/> |
|OutputFormat  <br/> |図面の出力形式を指定します。図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。  <br/> |[[OutputFormat] セル ([Document Properties] セクション)](outputformat-cell-document-properties-section.md) <br/> |
|PageBottomMargin  <br/> |印刷ページの下余白を指定します。  <br/> |[[PageBottomMargin] セル ([Print Properties] セクション)](pagebottommargin-cell-print-properties-section.md) <br/> |
|PageHeight  <br/> |図面単位で表した印刷ページの高さを指定します。  <br/> |[[PageHeight] セル ([Page Properties] セクション)](pageheight-cell-page-properties-section.md) <br/> |
|PageLeftMargin  <br/> |印刷ページの左余白を指定します。  <br/> |[[PageLeftMargin] セル ([Print Properties] セクション)](pageleftmargin-cell-print-properties-section.md) <br/> |
|PageLineJumpDirX  <br/> |図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。  <br/> |[[PageLineJumpDirX] セル ([Page Layout] セクション)](pagelinejumpdirx-cell-page-layout-section.md) <br/> |
|PageLineJumpDirY  <br/> |図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。  <br/> |[[PageLineJumpDirY] セル ([Page Layout] セクション)](pagelinejumpdiry-cell-page-layout-section.md) <br/> |
|PageLockDuplicate  <br/> |ページを複製できるかどうかを、ブール演算型で決定します。  <br/> |[[PageLockDuplicate] セル ([ページのプロパティ] セクション)](pagelockduplicate-cell-page-properties-section.md) <br/> |
|PageLockReplace  <br/> |このページで [図形の置換] ボタンを無効にするかどうかを示します。  <br/> |[[PageLockReplace] セル ([ページのプロパティ] セクション)](pagelockreplace-cell-page-properties-section.md) <br/> |
|PageRightMargin  <br/> |印刷ページの右余白を指定します。  <br/> |[[PageRightMargin] セル ([Print Properties] セクション)](pagerightmargin-cell-print-properties-section.md) <br/> |
|[Pagescale]  <br/> |現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。  <br/> |[[PageScale] セル ([Page Properties] セクション)](pagescale-cell-page-properties-section.md) <br/> |
|PageShapeSplit  <br/> |ページの図形が自動的に分割されるかどうかを示します。  <br/> |[[PageShapeSplit] セル ([Page Layout] セクション)](pageshapesplit-cell-page-layout-section.md) <br/> |
|[Pagesx]  <br/> |図面ページに左右を揃えるプリンター ページの番号を指定します。  <br/> |[[PagesX] セル ([Print Properties] セクション)](pagesx-cell-print-properties-section.md) <br/> |
|[Pagesy]  <br/> |図面ページに上下を揃えるプリンター ページの番号を指定します。  <br/> |[[PagesY] セル ([Print Properties] セクション)](pagesy-cell-print-properties-section.md) <br/> |
|PageTopMargin  <br/> |印刷ページの上余白を指定します。  <br/> |[[PageTopMargin] セル ([Print Properties] セクション)](pagetopmargin-cell-print-properties-section.md) <br/> |
|[Pagewidth]  <br/> |印刷ページの幅を図面単位で指定します。  <br/> |[[PageWidth] セル ([Page Properties] セクション)](pagewidth-cell-page-properties-section.md) <br/> |
|PaperKind  <br/> |ページを印刷する用紙の種類を指定します。  <br/> |[[PaperKind] セル ([Print Properties] セクション)](paperkind-cell-print-properties-section.md) <br/> |
|PaperSource  <br/> |用紙の給紙方法を指定します。  <br/> |[[PaperSource] セル ([PrintProperties] セクション)](papersource-cell-printproperties-section.md) <br/> |
|パースペクティブ  <br/> |度 (0 359.9) で、面内の回転の遠近の角度を決定します。  <br/> |[[Perspective] セル ([3-D 回転のプロパティ] セクション)](perspective-cell-3-d-rotation-properties-section.md) <br/> |
|[Pinx]  <br/> |親図形の原点を基準にしたときの、図形の Pin (回転の中心) の x 座標を表します。  <br/> |[[PinX] セル ([Shape Transform] セクション)](pinx-cell-shape-transform-section.md) <br/> |
|[Piny]  <br/> |親図形の原点を基準にしたときの、図形の Pin (回転の中心) の y 座標を表します。  <br/> |[[PinY] セル ([Shape Transform] セクション)](piny-cell-shape-transform-section.md) <br/> |
|PlaceDepth  <br/> |レイアウトを作成する前に図面を分析する方法を指定します。また、レイアウトの種類も指定します。  <br/> |[[PlaceDepth] セル ([Page Layout] セクション)](placedepth-cell-page-layout-section.md) <br/> |
|PlaceFlip  <br/> |[レイアウトの構成] ダイアログ ボックスを使用するときに、配置可能な図形をページ上で反転または回転する方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[PlaceFlip] セル ([Page Layout] セクション)](placeflip-cell-page-layout-section.md) <br/> |
|PlaceStyle  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[PlaceStyle] セル ([ページ レイアウト] セクション)](placestyle-cell-page-layout-section.md) <br/> |
|[Plowcode]  <br/> |図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。  <br/> |[[PlowCode] セル ([Page Layout] セクション)](plowcode-cell-page-layout-section.md) <br/> |
|PreviewQuality  <br/> |図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。  <br/> |[[PreviewQuality] セル ([Document Properties] セクション)](previewquality-cell-document-properties-section.md) <br/> |
|PreviewScope  <br/> |図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。  <br/> |[[PreviewScope] セル ([Document Properties] セクション)](previewscope-cell-document-properties-section.md) <br/> |
|[Printgrid]  <br/> |図面ページの印刷時にグリッドを印刷するかどうかを指定します。  <br/> |[[PrintGrid] セル ([Print Properties] セクション)](printgrid-cell-print-properties-section.md) <br/> |
|PrintPageOrientation  <br/> |ページの印刷方向を、縦向きにするか横向きにするかを指定します。  <br/> |[[PrintPageOrientation] セル ([Print Properties] セクション)](printpageorientation-cell-print-properties-section.md) <br/> |
|QuickStyleEffectsMatrix  <br/> |アクティブなテーマから図形を継承するクイック スタイル効果を、0 から 6 の整数で決定します。  <br/> ||
|QuickStyleFillColor  <br/> |0 ~ 7 の整数として、図形の塗りつぶしを使用するテーマの色を決定します。  <br/> |[[QuickStyleFillColor] セル ([クイック スタイル] セクション)](quickstylefillcolor-cell-quick-style-section.md) <br/> |
|QuickStyleFillMatrix  <br/> |使用中のテーマから図形を継承したスタイルをクイックスタイルで塗りつぶすかどうかを、0 から 6 の整数で決定します。  <br/> |[[QuickStyleFillMatrix] セル ([クイック スタイル] セクション)](quickstylefillmatrix-cell-quick-style-section.md) <br/> |
|QuickStyleFontColor  <br/> |図形のテキストが 0-1 整数値で、作業中のテーマから継承したクイック スタイルからフォントの色を決定します。  <br/> |[[QuickStyleFontColor] セル ([クイック スタイル] セクション)](quickstylefontcolor-cell-quick-style-section.md) <br/> |
|QuickStyleFontMatrix  <br/> |1 ~ 6 の整数として各クイック スタイル、フォントのスタイルを決定します。  <br/> |[[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)](quickstylefontmatrix-cell-quick-style-section.md) <br/> |
|QuickStyleLineColor  <br/> |0 ~ 7 の整数として、図形の線を使用するテーマの色を決定します。  <br/> |[[QuickStyleLineColor] セル ([クイック スタイル] セクション)](quickstylelinecolor-cell-quick-style-section.md) <br/> |
|QuickStyleLineMatrix  <br/> |0-6 の整数として、図形を継承するクイック スタイルのスタイルを指定します。  <br/> |[[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)](quickstylelinematrix-cell-quick-style-section.md) <br/> |
|QuickStyleShadowColor  <br/> |0 ~ 7 の整数として、図形の影を使用するテーマの色を決定します。  <br/> |[[QuickStyleShadowColor] セル ([クイック スタイル] セクション)](quickstyleshadowcolor-cell-quick-style-section.md) <br/> |
|QuickStyleType  <br/> |クイック スタイルの種類を決定 (2 次元、1 次元、またはコネクタ)、図形を継承します。  <br/> |[[QuickStyleType] セル ([クイック スタイル] セクション)](quickstyletype-cell-quick-style-section.md) <br/> |
|QuickStyleVariation  <br/> |テキスト、線、およびテーマが適用された図の背景の図形に塗りつぶしの色の可視性を保証します。  <br/> ||
|ReflectionBlur  <br/> |0.0 から 100.0 までのポイント単位で、図形上の反射のぼかしの量を決定します。  <br/> |[[ReflectionBlur] セル ([追加効果のプロパティ] セクション)](reflectionblur-cell-additional-effect-properties-section.md) <br/> |
|ReflectionDist  <br/> |距離の決定に 100.0 0.0 からポイントに、図形から反射をオフセットします。  <br/> |[[ReflectionDist] セル ([追加効果のプロパティ] セクション)](reflectiondist-cell-additional-effect-properties-section.md) <br/> |
|ReflectionSize  <br/> |図形と相対する反射のサイズを、0.0 から 100.0% までのパーセンテージとして決定します。[ReflectionSize] セルに 0% の値を設定した図形には反射がありません。100% の値を設定すると、図形の完全な鏡像が表示されます。  <br/> |[[ReflectionSize] セル ([追加効果のプロパティ] セクション)](reflectionsize-cell-additional-effect-properties-section.md) <br/> |
|ReflectionTrans  <br/> |0 から 100% の割合として、反射の透明度を決定します。  <br/> |[[ReflectionTrans] セル ([追加効果のプロパティ] セクション)](reflectiontrans-cell-additional-effect-properties-section.md) <br/> |
|リレーションシップ  <br/> |コンテナー、リスト、引き出し、および図形どうしの関係を格納します。  <br/> |[[Relationships] セル ([図形レイアウト] セクション)](relationships-cell-shape-layout-section.md) <br/> |
|ReplaceCopyCells  <br/> |図形の置換操作中に、古い図形から置換後の図形にコピーされるシェイプシート内のセル一覧を示します。  <br/> |[[ReplaceCopyCells] セル ([図形動作の変更] セクション)](replacecopycells-cell-change-shape-behavior-section.md) <br/> |
|ReplaceLockFormat  <br/> |マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。マスター シェイプの [ReplaceLockFormat] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。  <br/> |[[ReplaceLockFormat] セル ([図形動作の変更] セクション)](replacelockformat-cell-change-shape-behavior-section.md) <br/> |
|ReplaceLockShapeData  <br/> |マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。ReplaceLockShapeData は、マスター シェイプの図形データが、置換される図形の図形データすべてに優先するかどうかを決定します。  <br/> |[[ReplaceLockShapeData] セル ([図形動作の変更] セクション)](replacelockshapedata-cell-change-shape-behavior-section.md) <br/> |
|ReplaceLockText  <br/> |マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。ReplaceLockText は、マスターに表示されるテキストが、置換される図形のテキストに優先するかを決定します。  <br/> |[[ReplaceLockText] セル ([図形動作の変更] セクション)](replacelocktext-cell-change-shape-behavior-section.md) <br/> |
|ResizeMode  <br/> |図形に対して現在設定されているサイズ変更の動作の方法を示します。  <br/> |[[ResizeMode] セル ([Shape Transform] セクション)](resizemode-cell-shape-transform-section.md) <br/> |
|ResizePage  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトした後で、図面が中心に位置するようにページを拡大するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[ResizePage] セル ([Page Layout] セクション)](resizepage-cell-page-layout-section.md) <br/> |
|RightMargin  <br/> |テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。  <br/> |[[RightMargin] セル ([Text Block Format] セクション)](rightmargin-cell-text-block-format-section.md) <br/> |
|RotateGradientWithShape  <br/> |塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。  <br/> |[[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)](rotategradientwithshape-cell-gradient-properties-section.md) <br/> |
|RotationType  <br/> |図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。  <br/> |[[RotationType] セル ([3-D 回転のプロパティ] セクション)](rotationtype-cell-3-d-rotation-properties-section.md) <br/> |
|RotationXAngle  <br/> |度単位で、x 軸方向の回転の角度を設定 (0.0 から 359.9)。  <br/> |[[RotationXAngle] セル ([3-D 回転のプロパティ] セクション)](rotationxangle-cell-3-d-rotation-properties-section.md) <br/> |
|RotationYAngle  <br/> |度単位で、y 軸方向の回転の角度を設定 (0.0 から 359.9)。  <br/> |[[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)](rotationyangle-cell-3-d-rotation-properties-section.md) <br/> |
|RotationZAngle  <br/> |度で、z 軸に沿った回転の角度を設定 (0.0 から 359.9)。  <br/> |[[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)](rotationzangle-cell-3-d-rotation-properties-section.md) <br/> |
|丸めの方法  <br/> |1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。  <br/> |[[Rounding] セル ([Line Format] セクション)](rounding-cell-line-format-section.md) <br/> |
|RouteStyle  <br/> |ローカルな迂回方法を持たない図面ページ上のすべてのコネクタに対して、迂回方法と方向を指定します。  <br/> |[[RouteStyle] セル ([Page Layout] セクション)](routestyle-cell-page-layout-section.md) <br/> |
|[Scalex]  <br/> |[プリンター] ページで、図面ページの表示倍率の割合を指定します。  <br/> |[[ScaleX] セル ([Print Properties] セクション)](scalex-cell-print-properties-section.md) <br/> |
|Scaley]  <br/> |[プリンター] ページで、図面ページの表示倍率の割合を指定します。  <br/> |[[ScaleY] セル ([Print Properties] セクション)](scaley-cell-print-properties-section.md) <br/> |
|SelectMode  <br/> |グループ図形とそのメンバーを選択する方法を指定します。  <br/> |[[SelectMode] セル ([Group Properties] セクション)](selectmode-cell-group-properties-section.md) <br/> |
|ShapeFixedCode セル  <br/> |配置可能な図形について、配置時の動作を指定します。  <br/> |[[ShapeFixedCode] セル ([Shape Layout] セクション)](shapefixedcode-cell-shape-layout-section.md) <br/> |
|ShapeKeywords  <br/> |マスター シェイプに割り当てられている検索キーワードが含まれています。  <br/> ||
|ShapePermeablePlace  <br/> |[レイアウトの構成] ダイアログ ボックスで図形をレイアウトするときに、配置可能な図形を図形の上部に配置するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[ShapePermeablePlace] セル ([Shape Layout] セクション)](shapepermeableplace-cell-shape-layout-section.md) <br/> |
|ShapePermeableX  <br/> |コネクタの接続経路が、配置可能な図形上を水平方向に通過するかどうかを指定します。  <br/> |[[ShapePermeableX] セル ([Shape Layout] セクション)](shapepermeablex-cell-shape-layout-section.md) <br/> |
|ShapePermeableY  <br/> |コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。  <br/> |[[ShapePermeableY] セル ([Shape Layout] セクション)](shapepermeabley-cell-shape-layout-section.md) <br/> |
|ShapePlaceFlip  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[ShapePlaceFlip] セル ([Shape Layout] セクション)](shapeplaceflip-cell-shape-layout-section.md) <br/> |
|ShapePlaceStyle  <br/> |図形の配置方法のページで、[レイアウトの構成] ダイアログ ボックスをオンにして図形をレイアウトするときを指定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。 VisCellIndices からレイアウト スタイルと整列の値を格納します。  <br/> |[[ShapePlaceStyle] セル ([図形レイアウト] セクション)](shapeplacestyle-cell-shape-layout-section.md) <br/> |
|ShapePlowCode  <br/> |図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。  <br/> |[[ShapePlowCode] セル ([Shape Layout] セクション)](shapeplowcode-cell-shape-layout-section.md) <br/> |
|ShapeRouteStyle  <br/> |図面ページ上にある選択したコネクタの迂回方法と方向を指定します。  <br/> |[[ShapeRouteStyle] セル ([Shape Layout] セクション)](shaperoutestyle-cell-shape-layout-section.md) <br/> |
|ShapeShdwBlur  <br/> |(0.00 ~ 100.00 の範囲) をポイント単位での図形の影のぼかしのサイズを決定します。  <br/> |[[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)](shapeshdwblur-cell-fill-format-section.md) <br/> |
|ShapeShdwObliqueAngle  <br/> |図形の斜体の影に角度を指定します。  <br/> |[[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)](shapeshdwobliqueangle-cell-fill-format-section.md) <br/> |
|ShapeShdwOffsetX  <br/> |図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。  <br/> |[[ShapeShdwOffsetX] セル ([Fill Format] セクション)](shapeshdwoffsetx-cell-fill-format-section.md) <br/> |
|ShapeShdwOffsetY  <br/> |図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。  <br/> |[[ShapeShdwOffsetY] セル ([Fill Format] セクション)](shapeshdwoffsety-cell-fill-format-section.md) <br/> |
|ShapeShdwScaleFactor  <br/> |図形の影を拡大または縮小できる割合を、パーセントで指定します。  <br/> |[[ShapeShdwScaleFactor] セル ([Fill Format] セクション)](shapeshdwscalefactor-cell-fill-format-section.md) <br/> |
|ShapeShdwShow  <br/> |図形に影を表示するかどうかを、0 から 2 の整数で決定します。  <br/> |[[ShapeShdwShow] セル ([塗りつぶしの書式設定] セクション)](shapeshdwshow-cell-fill-format-section.md) <br/> |
|ShapeShdwType  <br/> |図形の影の種類を指定します。  <br/> |[[ShapeShdwType] セル ([Fill Format] セクション)](shapeshdwtype-cell-fill-format-section.md) <br/> |
|[Shapesplit]  <br/> |この図形が、分割可能な図形を分割できるかどうかを示します。  <br/> |[[ShapeSplit] セル ([Shape Layout] セクション)](shapesplit-cell-shape-layout-section.md) <br/> |
|ShapeSplittable  <br/> |この 1 次元図形が分割可能かどうかを示します。  <br/> |[[ShapeSplittable] セル ([Shape Layout] セクション)](shapesplittable-cell-shape-layout-section.md) <br/> |
|Sharpen  <br/> |ビットマップ イメージを鮮明にします。既定値は 0% です。イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。  <br/> |[[Sharpen] セル ([Image Properties] セクション)](sharpen-cell-image-properties-section.md) <br/> |
|ShdwForegnd  <br/> |図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。  <br/> |[[ShdwForegnd] セル ([Fill Format] セクション)](shdwforegnd-cell-fill-format-section.md) <br/> |
|ShdwForegndTrans  <br/> |図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。  <br/> |[[ShdwForegndTrans] セル ([Fill Format] セクション)](shdwforegndtrans-cell-fill-format-section.md) <br/> |
|ShdwObliqueAngle  <br/> |既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。  <br/> |[[ShdwObliqueAngle] セル ([Page Properties] セクション)](shdwobliqueangle-cell-page-properties-section.md) <br/> |
|ShdwOffsetX  <br/> |図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。  <br/> |[[ShdwOffsetX] セル ([Page Properties] セクション)](shdwoffsetx-cell-page-properties-section.md) <br/> |
|ShdwOffsetY  <br/> |図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。  <br/> |[[ShdwOffsetY] セル ([Page Properties] セクション)](shdwoffsety-cell-page-properties-section.md) <br/> |
|ShdwPattern  <br/> |図形の影の塗りつぶしパターンを指定します。  <br/> |[[ShdwPattern] セル ([Fill Format] セクション)](shdwpattern-cell-fill-format-section.md) <br/> |
|ShdwScaleFactor  <br/> |図形の影を拡大または縮小する割合を、パーセントで指定します。  <br/> |[[ShdwScaleFactor] セル ([Page Properties] セクション)](shdwscalefactor-cell-page-properties-section.md) <br/> |
|[Shdwtype]  <br/> |ページの既定の影の種類を指定します。  <br/> |[[ShdwType] セル ([Page Properties] セクション)](shdwtype-cell-page-properties-section.md) <br/> |
|SketchAmount  <br/> |スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。  <br/> |[[SketchAmount] セル ([追加効果のプロパティ] セクション)](sketchamount-cell-additional-effect-properties-section.md) <br/> |
|SketchEnabled  <br/> |図形の上またはブール値としてではなく、スケッチ効果が表示されるかどうかを決定します。  <br/> |[[SketchEnabled] セル ([追加効果のプロパティ] セクション)](sketchenabled-cell-additional-effect-properties-section.md) <br/> |
|SketchFillChange  <br/> |セクションの長さの割合として、スケッチ効果を使用する場合は、図形の塗りつぶしを図形の座標からのランダム化の量を決定します。 SketchFillChange セルの値を 0% に設定すると、図形の塗りつぶしの境界のジオメトリは、図形の座標を一致します。 値が 100% の場合は、図形の塗りつぶしの境界のジオメトリは、図形のジオメトリを従っていません。  <br/> |[[SketchFillChange] セル ([追加効果のプロパティ] セクション)](sketchfillchange-cell-additional-effect-properties-section.md) <br/> |
|SketchLineChange  <br/> |セクションの長さの割合として、スケッチ効果を使用する場合は、図形の線を図形の座標からのランダム化の量を決定します。 SketchLineChange セルの値を 0% に設定すると、図形の線のジオメトリは、図形の座標を一致します。 値が 100% の場合は、図形の線のジオメトリは、図形のジオメトリを従っていません。  <br/> |[[SketchLineChange] セル ([追加効果のプロパティ] セクション)](sketchlinechange-cell-additional-effect-properties-section.md) <br/> |
|SketchLineWeight  <br/> |0 から 50 までのポイントで、スケッチ効果の結果として、線の太さに追加されたその他の太さを決定します。 セルが増加する SketchLineWeight の値として図形の線の太さが大きくなります。  <br/> |[[SketchLineWeight] セル ([追加効果のプロパティ] セクション)](sketchlineweight-cell-additional-effect-properties-section.md) <br/> |
|SketchSeed  <br/> |スケッチ効果の図形座標を決定するために使用されるランダム化の値を、正の整数で表します。[SketchSeed] セルの値は、スケッチ効果を図形に適用するとき、ランダムで作成されます。  <br/> |[[SketchSeed] セル ([追加効果のプロパティ] セクション)](sketchseed-cell-additional-effect-properties-section.md) <br/> |
|SoftEdgesSize  <br/> |ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。[SoftEdgesSize] セルの値が 0 の場合、図形にソフト エッジは適用されません。  <br/> |[[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)](softedgessize-cell-additional-effect-properties-section.md) <br/> |
|[Textbkgnd]  <br/> |図形のテキストの背景色を指定します。  <br/> |[[TextBkgnd] セル ([Text Block Format] セクション)](textbkgnd-cell-text-block-format-section.md) <br/> |
|TextBkgndTrans  <br/> |図形のテキスト ブロックの背景色に適用される透過性レベルを指定します。  <br/> |[[TextBkgndTrans] セル ([Text Block Format] セクション)](textbkgndtrans-cell-text-block-format-section.md) <br/> |
|TextDirection  <br/> |テキスト ブロック内にある文字の方向を指定します。  <br/> |[[TextDirection] セル ([Text Block Format] セクション)](textdirection-cell-text-block-format-section.md) <br/> |
|データ  <br/> |将来の使用のために予約されています。  <br/> |[[TheData] セル ([Events] セクション)](thedata-cell-events-section.md) <br/> |
|ThemeIndex  <br/> |整数として、ドキュメントに適用される組み込みの Microsoft Visio のテーマの列挙体を格納します。 ドキュメントの新しいテーマを選択すると、組み込みのテーマのインデックスを使用してドキュメントとすべてのページと図形が含まれているの ThemeIndex のセルが更新されます。  <br/> |[[ThemeIndex] セル ([テーマのプロパティ] セクション)](themeindex-cell-theme-properties-section.md) <br/> |
|テキスト  <br/> |図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。  <br/> |[[TheText] セル ([Events] セクション)](thetext-cell-events-section.md) <br/> |
|TopMargin  <br/> |テキスト ブロックの上の枠線から、そのブロックに含まれるテキストの最初の行までの間隔を指定します。既定値は 4.0000 ポイントです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、上余白の長さは変わりません。  <br/> |[[TopMargin] セル ([Text Block Format] セクション)](topmargin-cell-text-block-format-section.md) <br/> |
|Transparency  <br/> |図形のテキストの色に適用される透過性レベルを指定します。  <br/> |[[Transparency] セル ([Character] セクション)](transparency-cell-character-section.md) <br/> |
|Transparency  <br/> |レイヤーの色の透過性レベルを指定します。  <br/> |[[Transparency] セル ([Image Properties] セクション)](transparency-cell-image-properties-section.md) <br/> |
|Transparency  <br/> |レイヤーの色の透過性レベルを指定します。  <br/> |[[Transparency] セル ([Layers] セクション)](transparency-cell-layers-section.md) <br/> |
|[Txtangle]  <br/> |図形の x 軸を基準としたときの、テキスト ブロックの現在の回転角度を指定します。既定値は 0°です。  <br/> |[[TxtAngle] セル ([Text Transform] セクション)](txtangle-cell-text-transform-section.md) <br/> |
|[Txtheight]  <br/> |テキスト ブロックの高さを決定します。 既定の数式は: = 高さ\*1  <br/> |[[TxtHeight] セル ([Text Transform] セクション)](txtheight-cell-text-transform-section.md) <br/> |
|TxtLocPinX  <br/> |テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の x 座標を指定します。 既定の数式は: = [txtwidth] \* 0.5This 数式では、テキスト ブロックの水平方向の中央にします。  <br/> |[[TxtLocPinX] セル ([Text Transform] セクション)](txtlocpinx-cell-text-transform-section.md) <br/> |
|TxtLocPinY  <br/> |テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の y 座標を指定します。 既定の数式は: = [txtheight] \* 0.5  <br/> |[[TxtLocPinY] セル ([Text Transform] セクション)](txtlocpiny-cell-text-transform-section.md) <br/> |
|[Txtpinx]  <br/> |図形の原点を基準として回転のテキスト ブロックの中心の x 座標を指定します。 既定の数式は: 幅を = \* 0.5  <br/> |[[TxtPinX] セル ([Text Transform] セクション)](txtpinx-cell-text-transform-section.md) <br/> |
|[Txtpiny]  <br/> |図形の原点を基準として回転のテキスト ブロックの中心の y 座標を指定します。 既定の数式は: = 高さ\*0.5  <br/> |[[TxtPinY] セル ([Text Transform] セクション)](txtpiny-cell-text-transform-section.md) <br/> |
|[Txtwidth]  <br/> |テキスト ブロックの幅を決定します。 既定の数式は: 幅を = \* 1  <br/> |[[TxtWidth] セル ([Text Transform] セクション)](txtwidth-cell-text-transform-section.md) <br/> |
|UIVisibility  <br/> |ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。  <br/> |[[UIVisibility] セル ([Page Properties] セクション)](uivisibility-cell-page-properties-section.md) <br/> |
|UpdateAlignBox  <br/> |コントロール ハンドルを移動するたびに選択範囲を再計算します。  <br/> |[[UpdateAlignBox] セル ([Miscellaneous] セクション)](updatealignbox-cell-miscellaneous-section.md) <br/> |
|UseGroupGradient  <br/> |図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。[UseGroupGradient] セルの値が影響するのは、図形の塗りつぶしのみです。  <br/> |[[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)](usegroupgradient-cell-gradient-properties-section.md) <br/> |
|VariationColorIndex  <br/> |整数値としてページで、アクティブなテーマのバリエーションの色のインデックスを決定します。  <br/> |[[VariationColorIndex] セル ([テーマのプロパティ] セクション)](variationcolorindex-cell-theme-properties-section.md) <br/> |
|VariationStyleIndex  <br/> |整数値としてページで、アクティブなテーマのバリエーションのスタイルのインデックスを決定します。  <br/> |[[VariationStyleIndex] セル ([テーマのプロパティ] セクション)](variationstyleindex-cell-theme-properties-section.md) <br/> |
|VerticalAlign  <br/> |テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。  <br/> |[[VerticalAlign] セル ([Text Block Format] セクション)](verticalalign-cell-text-block-format-section.md) <br/> |
|ViewMarkup  <br/> |図面ウィンドウに校正履歴を表示するかどうかを指定します。  <br/> |[[ViewMarkup] セル ([Document Properties] セクション](viewmarkup-cell-document-properties-section.md) <br/> |
|WalkPreference  <br/> |1-D 図形をあいまいな位置に移動したときに、その図形の端点が、動的接着によって接着先の図形にある水平方向の接続ポイントに移動するのか、または垂直方向の接続ポイントに移動するのかを指定します。既定では、1-D 図形の始点と終点の両方とも水平方向の接続ポイントに移動します。  <br/> |[[WalkPreference] セル ([Glue Info] セクション)](walkpreference-cell-glue-info-section.md) <br/> |
|Width  <br/> |図面の単位で選択した図形の幅が含まれています。 1-d 図形の幅を決定するための既定の数式は: = SQRT ((EndX-BeginX) ^2 + ([endy] - [beginy]) ^2)  <br/> |[[Width] セル ([Shape Transform] セクション)](width-cell-shape-transform-section.md) <br/> |
|XGridDensity  <br/> |使用する水平方向のグリッドの種類を指定します。  <br/> |[XGridDensity セル (ルーラー&amp;グリッド セクション)](xgriddensity-cell-rulergrid-section.md) <br/> |
|XGridOrigin  <br/> |グリッド原点の水平方向の座標を指定します。  <br/> |[XGridOrigin セル (ルーラー&amp;グリッド セクション)](xgridorigin-cell-rulergrid-section.md) <br/> |
|XGridSpacing  <br/> |固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。  <br/> |[XGridSpacing セル (ルーラー&amp;グリッド セクション)](xgridspacing-cell-rulergrid-section.md) <br/> |
|XRulerDensity  <br/> |ページのルーラーに対して、水平方向の小区分を指定します。  <br/> |[XRulerDensity セル (ルーラー&amp;グリッド セクション)](xrulerdensity-cell-rulergrid-section.md) <br/> |
|XRulerOrigin  <br/> |ページの x 軸のルーラーに対して、ゼロ点を指定します。  <br/> |[XRulerOrigin セル (ルーラー&amp;グリッド セクション)](xrulerorigin-cell-rulergrid-section.md) <br/> |
|YGridDensity  <br/> |使用する垂直方向のグリッドの種類を指定します。  <br/> |[YGridDensity セル (ルーラー&amp;グリッド セクション)](ygriddensity-cell-rulergrid-section.md) <br/> |
|YGridOrigin  <br/> |グリッド原点の垂直方向の座標を指定します。  <br/> |[YGridOrigin セル (ルーラー&amp;グリッド セクション)](ygridorigin-cell-rulergrid-section.md) <br/> |
|YGridSpacing  <br/> |固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。  <br/> |[YGridSpacing セル (ルーラー&amp;グリッド セクション)](ygridspacing-cell-rulergrid-section.md) <br/> |
|YRulerDensity  <br/> |ページのルーラーに対して、垂直方向の小区分を指定します。  <br/> |[YRulerDensity セル (ルーラー&amp;グリッド セクション)](yrulerdensity-cell-rulergrid-section.md) <br/> |
|YRulerOrigin  <br/> |ページの y 軸のルーラーに対して、ゼロ点を指定します。  <br/> |[YRulerOrigin セル (ルーラー&amp;グリッド セクション)](yrulerorigin-cell-rulergrid-section.md) <br/> |
   

